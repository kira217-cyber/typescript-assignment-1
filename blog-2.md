# Generics কীভাবে Reusable এবং Type-Safe Code তৈরি করা যায়

## ভূমিকা
এটি আমাদের এমন functions এবং components তৈরি করতে সাহায্য করে, যেগুলো বিভিন্ন ধরনের data structure-এর সাথে কাজ করতে পারে, কিন্তু type safety বজায় রাখে।

----

## Generics কী সমস্যা solve করে?

Generics ছাড়া সাধারণভাবে আমরা `any` ব্যবহার করি:

function identity(value: any) {
  return value;
}

let result = identity("Hello");


## Generics এর ব্যবহার (Real Use Case)

Generics ব্যবহার করলে আমরা একই function বিভিন্ন type-এর data-এর জন্য reuse করতে পারি ।

function identity<T>(value: T): T {
  return value;
}  