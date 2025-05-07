## 🔑 What is the `keyof` keyword used for in TypeScript?

The `keyof` keyword in TypeScript is a powerful utility that lets you work with the property names of an object type. When you use `keyof`, it returns a union of all the keys within that object. This helps ensure that you’re only accessing valid properties, which leads to safer and more predictable code.

### ✅ Example:

``` ts
type Product = {
  id: number;
  name: string;
  price: number;
};

type ProductKeys = keyof Product; // "id" | "name" | "price"

function logProperty(obj: Product, key: ProductKeys) {
  console.log(obj[key]);
}

const item: Product = { id: 1, name: "Notebook", price: 50 };
logProperty(item, "price"); // Output: 50
```

In the example above, `keyof Product` ensures that the `key` parameter must match one of the defined keys in the `Product` type. If you try to use a key that doesn’t exist, TypeScript will raise a compile-time error—preventing bugs before they happen.

---

## 🛠️ How does TypeScript improve code quality and project maintainability?

TypeScript enhances JavaScript with static typing, which allows developers to catch errors early, right during development. By clearly defining the data structure, TypeScript makes your codebase more self-explanatory and easier to understand.

This has several long-term benefits:
- 🔍 **Fewer runtime errors**: Mistakes are caught before the code even runs.
- 📚 **Better documentation**: Types act as documentation for other developers (or your future self).
- 🧩 **Easier refactoring**: When changing your code, TypeScript shows you exactly where adjustments are needed.
- 💼 **Improved collaboration**: On team projects, it ensures everyone follows consistent data structures and contracts.

In short, TypeScript not only improves the reliability of your code but also makes it easier to scale and maintain, especially in larger projects.