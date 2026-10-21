# Blood Bond Bangladesh — অনলাইন ডেটাবেসসহ ওয়েবসাইট

এই ফোল্ডারে আছে:
- `index.html` — ওয়েবসাইট
- `config.js` — Supabase সংযোগের সেটিংস
- `schema.sql` — ডেটাবেস টেবিল ও নিরাপত্তা নীতির প্রাথমিক সেটআপ

## গুরুত্বপূর্ণ সীমাবদ্ধতা
আমি এখানে আপনার হয়ে Supabase বা GitHub অ্যাকাউন্ট তৈরি/প্রকাশ করতে পারি না। নিচের ফ্রি সেটআপ করলে ওয়েবসাইটটি অনলাইন ডেটাবেসের সঙ্গে কাজ করবে। ফ্রি প্ল্যানের শর্ত ও সীমা সেবাদাতার নিয়ম অনুযায়ী বদলাতে পারে।

## ধাপ ১ — Supabase ডেটাবেস তৈরি
1. https://supabase.com/ খুলে অ্যাকাউন্ট তৈরি করুন।
2. New project তৈরি করুন।
3. Project-এর SQL Editor খুলুন।
4. `schema.sql` ফাইলের সব SQL কপি করে SQL Editor-এ চালান।
5. Project Settings → API থেকে Project URL এবং anon/publishable key কপি করুন।

## ধাপ ২ — config.js সেট করুন
`config.js` ফাইল খুলে:
- `PASTE_YOUR_SUPABASE_PROJECT_URL_HERE`-এর জায়গায় Project URL
- `PASTE_YOUR_SUPABASE_ANON_OR_PUBLISHABLE_KEY_HERE`-এর জায়গায় anon/publishable key

**কখনো `service_role` বা secret key ওয়েবসাইটে রাখবেন না।** `config.js`-এর পরিবর্তন সংরক্ষণ করুন।

## ধাপ ৩ — GitHub Pages-এ ফ্রি প্রকাশ
1. https://github.com/ এ নতুন Public repository তৈরি করুন।
2. এই ফোল্ডারের `index.html`, `config.js` ও `schema.sql` আপলোড করুন।
3. Repository → Settings → Pages-এ যান।
4. Deploy from a branch নির্বাচন করে `main` এবং `/(root)` বেছে Save করুন।
5. GitHub প্রদত্ত ওয়েব ঠিকানা খুলুন। Supabase সেটআপ করা থাকলে রেজিস্ট্রেশন ও সার্চ অনলাইন ডেটাবেসে কাজ করবে।

## নিরাপত্তা ও গোপনীয়তা
- ফোন নম্বর প্রকাশ্যে দেখানোর আগে দাতার স্পষ্ট সম্মতি নিন।
- এই starter-এ public visitor donor registration ও blood request জমা দিতে পারে; তাই spam/CAPTCHA ও admin moderation যোগ না করে বড় পরিসরে চালু করবেন না।
- blood_requests টেবিল public read-এর জন্য খোলা নেই; জমা হওয়া অনুরোধ দেখতে authenticated/admin workflow যোগ করতে হবে।
- বাস্তব ব্যবহারের আগে donor data edit/delete, admin approval, privacy policy, data retention ও abuse reporting ব্যবস্থা যোগ করুন।
- ডেটাবেস policy-গুলো শুরুর জন্য; production ব্যবহারের আগে নিরাপত্তা পর্যালোচনা প্রয়োজন।

## স্থানীয়ভাবে পরীক্ষা
ফাইলগুলো একই ফোল্ডারে রাখুন। `config.js` সেটআপ না করলে সাইটে সংযোগ না থাকার বার্তা দেখাবে; অনলাইন ফিচার কাজ করবে না।
