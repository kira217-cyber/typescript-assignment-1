# any vs unknown — কেন unknown বেশি safe?

## ভূমিকা
অনেক সময় আমরা any ব্যবহার করি, যা পুরো type checking system কে ভেঙে দেয়। এই blog-এ আমরা বুঝবো কেন any dangerous এবং কেন unknown বেশি safe।

------

## any কী সমস্যা তৈরি করে?

any মানে TypeScript আর কিছু check করে না।


let data: any = "Hello";

data.toUpperCase(); // OK
data.toFixed(); // runtime error ❌


## unknown কেন safe?

unknown মানে value আছে, কিন্তু আমরা জানি না সেটা কী type। তাই TypeScript সরাসরি unsafe operation allow করে না।


let data: unknown = "Hello";

// data.toUpperCase(); ❌ Error