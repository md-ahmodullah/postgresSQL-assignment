### What is PostgreSQL?

**PostgreSQL হলো বর্তমান সময়ের সবচেয়ে এডভান্স রিলেশনাল ডেটাবেজ ম্যানেজমেন্ট সিস্টেম।**

- **কেন PostgreSQL শিখব? কারণঃ-**

- Open Source
- ACID Compliance
- Indexing

- RDBMS
- Advanced Data Types
- Community Support

- Modern
- Scalability

- **Download & Installation -** *https://www.postgresql.org/download/*

### Role of PostgreSQL : Data FLow in an Application

![dataFlow.png](https://i.ibb.co/v4XppLhm/dataFlow.png)

কোনো এপ্লিকেশনে ইউজার কোনো এক্টিভিটি করতে চাইলে, যেমন কোনো বাটনে ক্লিক করে কোনো ডেটা এক্সেস করতে চাইলে সেটা প্রথমে ব্যাকেন্ড সার্ভারে যায়। সার্ভার তখন ডেটাবেজে রিকুয়েস্ট করে প্রয়োজনীয় ডেটা সরবরাহ করে। সার্ভার থেকে ডেটাবেজের মধ্যে ডেটাবেজের কমিউনিকেশন হ্যান্ডেল করে একটি DBMS; এখানেই ইন্ট্রোডিউস হচ্ছে বর্তমান সময়ের সবচেয়ে জনপ্রিয় DBMS - PostgreSQL. তবে যে কেউ চাইলেই ডেটাবেজে এক্সেস করতে পারে না। এজন্য একটি অথেন্টিকেশন প্রসেসের মধ্য দিয়ে যেতে হয়। সার্ভার ও DBMS এর মাঝে বিভিন্ন ORM ব্যবহার করা হয়। যেমনঃ Prisma.
