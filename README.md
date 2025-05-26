## What is PostgreSQL?

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

![Postgres Visualization - source: Programming Hero (Next Level Development)](https://i.ibb.co/Dg9BZzV8/postgres-In-Visaul.png)

Postgres Visualization - source: Programming Hero (Next Level Development)

কোনো এপ্লিকেশনে ইউজার কোনো এক্টিভিটি করতে চাইলে, যেমন কোনো বাটনে ক্লিক করে কোনো ডেটা এক্সেস করতে চাইলে সেটা প্রথমে ব্যাকেন্ড সার্ভারে যায়। সার্ভার তখন ডেটাবেজে রিকুয়েস্ট করে প্রয়োজনীয় ডেটা সরবরাহ করে। সার্ভার থেকে ডেটাবেজের মধ্যে ডেটাবেজের কমিউনিকেশন হ্যান্ডেল করে একটি DBMS; এখানেই ইন্ট্রোডিউস হচ্ছে বর্তমান সময়ের সবচেয়ে জনপ্রিয় DBMS - PostgreSQL. তবে যে কেউ চাইলেই ডেটাবেজে এক্সেস করতে পারে না। এজন্য একটি অথেন্টিকেশন প্রসেসের মধ্য দিয়ে যেতে হয়। সার্ভার ও DBMS এর মাঝে বিভিন্ন ORM ব্যবহার করা হয়। যেমনঃ Prisma.

## Primary Key Vs Foreign Key

- **PRIMARY KEY** : এটি মূলত NOT NULL ও UNIQUE এর কম্বিনেশন; অর্থাৎ Primary Key একই সাথে Null হতে পারবে না এবং Unique হতে হবে। যেমনঃ একটি ইউজারে id.
- **FOREIGN KEY** : কোনো একটি টেবিলের Primary Key কে যখন আমরা অন্য একটি টেবিলে রাখি তখন যেই constraints তৈরি হয় তাই মূলত Foreign Key. এটি কীভাবে ভ্যালিডেশন এড করে?

![Postgres Visualization - source: Programming Hero (Next Level Development)](https://i.ibb.co/rRwtqpC0/foreign-key-constraints.png)

Postgres Visualization - source: Programming Hero (Next Level Development)

Order টেবিলে order_id এর সাথে Product টেবিলের prod_id কে Foreign Key হিসেবে ব্যবহার করা হয়েছে, ফলে যেই ভ্যালিডেশন এড হয়েছে তা হলঃ এখানে Product টেবিলের সাথে Order টেবিলের একটা ইন্টিগ্রিট তৈরি হয়েছে। প্রতিটা order_id এর জন্য অবশ্যই একটি prod_id থাকতে হবে। চাইলেই Product টেবিল থেকে একটি প্রোডাক্ট ডিলিট করা যাবে না।

## The purpose of the WHERE clause in a SELECT statement.

**নির্দিষ্ট কোনো শর্তের ভিত্তিতে ডেটা ফিল্টার করতে WHERE clause ব্যবহার করা হয়। বিভিন্ন অপারেটর দিয়ে শর্তযুক্ত করে দেখানো হলো। যেমনঃ**

- **IN & NOT IN :** Logical OR opeartor দিয়ে অনেক সময় ক্যুয়েরি লিখতে গেলে সিনট্যাক্স বড় হয়ে যায়। এটি Shorthand এ লিখতে হলে IN & NOT IN অপারেটর ব্যবহার করা যেতে পারে। যেমনঃ

```sql
-- Using Logical OR Operator
SELECT * FROM students
    WHERE country = 'USA' OR country = 'Canada' OR country = 'UK'
-- Using IN/NOT IN Operator
SELECT * FROM students
		WHERE country IN('USA', 'Canada', 'UK')
SELECT * FROM students
		WHERE country NOT IN('USA', 'Canada', 'UK')
```

- **BETWEEN** : Between Operator ব্যবহার করে দুই ডেটার মধ্যবর্তী ডেটা দেখানো যায়। যেমনঃ

```sql
-- Data between two dates
SELECT * FROM students
    WHERE dob BETWEEN '2003-12-21' AND '2004-06-30'
```

##
