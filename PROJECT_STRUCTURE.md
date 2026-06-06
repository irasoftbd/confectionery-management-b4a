# Confectionery Management System - B4A Project Structure

এই ডকুমেন্ট প্রজেক্টের সম্পূর্ণ ফাইল সংগঠন এবং প্রতিটি ফাইলের উদ্দেশ্য ব্যাখ্যা করে।

## 📁 সম্পূর্ণ ডিরেক্টরি স্ট্রাকচার

```
confectionery-management-b4a/
│
├── 📁 Code/                          # সকল B4A প্রোগ্রামিং কোড
│   ├── Main.b4a                     # প্রধান UI এবং নেভিগেশন
│   ├── DatabaseManager.bas          # SQLite ডেটাবেস পরিচালনা
│   ├── InventoryModule.bas          # ইনভেন্টরি লজিক
│   ├── SalesModule.bas              # বিক্রয় লজিক
│   ├── ReportsModule.bas            # রিপোর্টিং সিস্টেম
│   └── Globals.bas                  # গ্লোবাল ভেরিয়েবল
│
├── 📁 Database/                     # ডেটাবেস সম্পর্কিত ফাইল
│   ├── schema.sql                   # ডেটাবেস টেবিল স্কিমা
│   └── sample_data.sql              # টেস্টিংয়ের জন্য স্যাম্পল ডেটা
│
├── 📁 Documentation/                # বিস্তারিত ডকুমেন্টেশন
│   ├── INSTALLATION.md              # B4A ইনস্টলেশন নির্দেশনা
│   ├── FEATURES.md                  # সকল ফিচারের বিবরণ
│   ├── USAGE_GUIDE.md               # অ্যাপ ব্যবহারের গাইড
│   ├── API.md                       # API রেফারেন্স
│   └── TROUBLESHOOTING.md           # সমস্যা সমাধান
│
├── 📁 Assets/                       # মিডিয়া এবং রিসোর্স ফাইল
│   ├── 📁 icons/                    # অ্যাপ আইকন এবং লোগো
│   │   ├── app_icon.png            # অ্যাপ্লিকেশন আইকন
│   │   ├── ic_inventory.png        # ইনভেন্টরি আইকন
│   │   ├── ic_sales.png            # বিক্রয় আইকন
│   │   ├── ic_reports.png          # রিপোর্ট আইকন
│   │   └── ic_settings.png         # সেটিংস আইকন
│   │
│   ├── 📁 images/                   # স্ক্রিনশট এবং ডেমো ছবি
│   │   ├── dashboard_demo.png
│   │   ├── inventory_demo.png
│   │   ├── sales_demo.png
│   │   └── reports_demo.png
│   │
│   └── 📁 colors/                   # কালার প্যালেট এবং থিম
│       └── color_scheme.txt
│
├── 📁 Config/                       # কনফিগারেশন ফাইল
│   ├── app_config.txt               # অ্যাপ কনফিগারেশন
│   ├── database_config.txt          # ডেটাবেস সেটিংস
│   └── feature_flags.txt            # ফিচার এনেবল/ডিসেবল
│
├── 🔗 .gitignore                    # Git এ অন্তর্ভুক্ত না করার ফাইল
├── 📄 README.md                     # প্রধান ডকুমেন্টেশন
├── 📄 SETUP_GUIDE.md                # সেটআপ এবং ইনস্টলেশন
├── 📄 PROJECT_STRUCTURE.md          # এই ফাইল
├── 📄 LICENSE                       # MIT লাইসেন্স
├── 📄 CHANGELOG.md                  # সংস্করণ ইতিহাস
└── 📄 CONTRIBUTING.md               # অবদান নির্দেশিকা

```

---

## 📂 প্রতিটি ফোল্ডার এবং ফাইলের বিবরণ

### 🔵 `Code/` ফোল্ডার

এখানে সকল B4A প্রোগ্রামিং কোড থাকে।

#### **Main.b4a** (প্রধান ফাইল)
```
উদ্দেশ্য: অ্যাপ্লিকেশনের প্রধান মডিউল এবং UI স্ক্রিন
অন্তর্ভুক্ত:
- স্প্ল্যাশ স্ক্রিন
- ড্যাশবোর্ড
- নেভিগেশন মেনু
- প্রধান কার্যকলাপ (Activity)
```

#### **DatabaseManager.bas** (ডেটাবেস ম্যানেজার)
```
উদ্দেশ্য: সকল ডেটাবেস অপারেশন পরিচালনা
অন্তর্ভুক্ত:
- SQLite সংযোগ স্থাপন
- টেবিল তৈরি
- ডেটা ইনসার্ট, আপডেট, ডিলিট
- ডেটা কোয়েরি এবং রিট্রিভ
- ডেটা ভ্যালিডেশন
```

#### **InventoryModule.bas** (ইনভেন্টরি মডিউল)
```
উদ্দেশ্য: ইনভেন্টরি ম্যানেজমেন্ট সংক্রান্ত সকল লজিক
অন্তর্ভুক্ত:
- পণ্য যোগ করা
- পণ্য সম্পাদনা
- পণ্য মুছে ফেলা
- স্টক আপডেট
- পণ্য তালিকা প্রদর্শন
- স্টক অ্যালার্ট
```

#### **SalesModule.bas** (বিক্রয় মডিউল)
```
উদ্দেশ্য: বিক্রয় অর্ডার এবং গ্রাহক ম্যানেজমেন্ট
অন্তর্ভুক্ত:
- নতুন বিক্রয় অর্ডার তৈরি
- গ্রাহক তথ্য সংরক্ষণ
- পেমেন্ট প্রক্রিয়াকরণ
- অর্ডার ট্র্যাকিং
- বিক্রয় ইতিহাস রিট্রিভ
```

#### **ReportsModule.bas** (রিপোর্ট মডিউল)
```
উদ্দেশ্য: রিপোর্ট এবং বিশ্লেষণ তৈরি
অন্তর্ভুক্ত:
- দৈনিক বিক্রয় রিপোর্ট
- মাসিক বিক্রয় সংক্ষিপ্ত
- স্টক রিপোর্ট
- লাভজনকতা বিশ্লেষণ
- চার্ট এবং গ্রাফ
```

#### **Globals.bas** (গ্লোবাল ভেরিয়েবল)
```
উদ্দেশ্য: সম্পূর্ণ অ্যাপ জুড়ে ব্যবহৃত গ্লোবাল ভেরিয়েবল এবং কনফিগারেশন
অন্তর্ভুক্ত:
- অ্যাপ সেটিংস
- ডেটাবেস পাথ
- ডিফল্ট মান
- ডিফল্ট পণ্য ক্যাটাগরি
- মুদ্রা সিম্বল
```

---

### 🔵 `Database/` ফোল্ডার

ডেটাবেস স্কিমা এবং স্যাম্পল ডেটা থাকে এখানে।

#### **schema.sql**
```sql
SQL স্ক্রিপ্ট যা নিম্নলিখিত টেবিল তৈরি করে:

1. Products (পণ্য)
   - id, name, category, price, cost, stock, unit, description

2. Categories (বিভাগ)
   - id, name, description

3. Sales (বিক্রয়)
   - id, date, customer_name, total_amount, payment_method

4. SalesDetails (বিক্রয় বিবরণী)
   - id, sale_id, product_id, quantity, price, total

5. Customers (গ্রাহক)
   - id, name, phone, email, address, total_spent

6. Settings (সেটিংস)
   - key, value
```

#### **sample_data.sql**
```sql
পরীক্ষার জন্য স্যাম্পল ডেটা ইনসার্ট করে।
```

---

### 🔵 `Documentation/` ফোল্ডার

বিস্তারিত ডকুমেন্টেশন ফাইল।

#### **INSTALLATION.md**
B4A IDE ইনস্টলেশন এবং সেটআপের ধাপে ধাপে নির্দেশনা।

#### **FEATURES.md**
সকল ফিচারের বিস্তারিত বর্ণনা এবং ব্যবহার পদ্ধতি।

#### **USAGE_GUIDE.md**
অ্যাপ্লিকেশন ব্যবহারের সম্পূর্ণ গাইড (ব্যবহারকারী দৃষ্টিকোণ)।

#### **API.md**
B4A কোড API রেফারেন্স এবং ফাংশন ডকুমেন্টেশন (ডেভেলপার দৃষ্টিকোণ)।

#### **TROUBLESHOOTING.md**
সাধারণ সমস্যা এবং তাদের সমাধান।

---

### 🔵 `Assets/` ফোল্ডার

ছবি এবং অন্যান্য মিডিয়া রিসোর্স।

#### **icons/**
- অ্যাপ্লিকেশন আইকন
- মেনু আইকন
- বোতাম আইকন

#### **images/**
- স্ক্রিনশট
- ডেমো ছবি
- টিউটোরিয়াল ছবি

#### **colors/**
- কালার প্যালেট
- থিম সংজ্ঞা

---

### 🔵 `Config/` ফোল্ডার

অ্যাপ্লিকেশন কনফিগারেশন ফাইল।

#### **app_config.txt**
```
অ্যাপ্লিকেশন সাধারণ সেটিংস:
- অ্যাপ নাম
- ভার্সন নম্বর
- ডেভেলপার তথ্য
- লোগো পাথ
```

#### **database_config.txt**
```
ডেটাবেস সংক্রান্ত সেটিংস:
- ডেটাবেস ফাইল নাম
- ডেটাবেস পাথ
- ব্যাকআপ ফোল্ডার
```

#### **feature_flags.txt**
```
ফিচার এনেবল/ডিসেবল:
- ইনভেন্টরি ম্যানেজমেন্ট: ON/OFF
- বিক্রয় ম্যানেজমেন্ট: ON/OFF
- রিপোর্টিং: ON/OFF
- ডার্ক মোড: ON/OFF
```

---

## 📊 ডেটা মডেল এবং সম্পর্ক

```
┌─────────────┐         ┌──────────────┐
│  Categories │◄────────┤   Products   │
└─────────────┘         └──────────────┘
                              ▲
                              │
                         ┌────┴─────┐
                         │           │
                    ┌────────┐  ┌─────────────┐
                    │  Sales │  │ SalesDetail │
                    └────┬───┘  └─────────────┘
                         │           ▲
                         │           │
                    ┌────▼───────────┴────┐
                    │   Customers         │
                    └─────────────────────┘
```

### টেবিল সম্পর্ক:
- **Products** ← **Categories**: একটি ক্যাটাগরিতে অনেক পণ্য
- **SalesDetails** ← **Sales**: একটি বিক্রয়ে অনেক বিবরণী
- **SalesDetails** ← **Products**: একটি পণ্য অনেক বিক্রয় বিবরণীতে
- **Sales** ← **Customers**: একজন গ্রাহক অনেক বিক্রয় করতে পারে

---

## 🔄 ফাইল ডিপেন্ডেন্সি

```
Main.b4a
  ├── Globals.bas (গ্লোবাল ভেরিয়েবল)
  ├── DatabaseManager.bas (ডেটাবেস)
  ├── InventoryModule.bas (ইনভেন্টরি)
  ├── SalesModule.bas (বিক্রয়)
  └── ReportsModule.bas (রিপোর্ট)

DatabaseManager.bas
  └── Globals.bas

InventoryModule.bas
  ├── DatabaseManager.bas
  └── Globals.bas

SalesModule.bas
  ├── DatabaseManager.bas
  ├── InventoryModule.bas (স্টক আপডেটের জন্য)
  └── Globals.bas

ReportsModule.bas
  ├── DatabaseManager.bas
  └── Globals.bas
```

---

## 📋 নাম দেওয়ার নিয়ম (Naming Conventions)

### ভেরিয়েবল নাম:
```
- অ্যারে: arr + নাম (arrProducts)
- বুলিয়ান: is + নাম (isLoggedIn)
- সংখ্যা: num + নাম (numItems)
- স্ট্রিং: str + নাম (strProductName)
```

### ফাংশন নাম:
```
- যা কিছু পায়: Get + নাম (GetProductById)
- যা কিছু সেট করে: Set + নাম (SetProductPrice)
- যা তৈরি করে: Create + নাম (CreateNewSale)
- যা চেক করে: Is/Check + নাম (IsStockAvailable)
```

### ডেটাবেস নাম:
```
- টেবিল: একবচন, বড় অক্ষর দিয়ে শুরু (Products, Sales)
- কলাম: ছোট অক্ষর, আন্ডারস্কোর (product_name, created_at)
- ফরেন কি: table_id (product_id, category_id)
```

---

## 🔐 ফাইল অনুমতি এবং এক্সেস

| ফাইল | পড়া | লেখা | এক্সিকিউট |
|------|------|------|----------|
| Code/* | ✅ | ✅ | ✅ |
| Database/* | ✅ | ✅ | ❌ |
| Documentation/* | ✅ | ✅ | ❌ |
| Assets/* | ✅ | ✅ | ❌ |
| Config/* | ✅ | ✅ | ❌ |

---

## 💾 স্টোরেজ প্রয়োজনীয়তা

```
ফাইলের আকার অনুমান:

- Code/ ফোল্ডার: ~2-3 MB
- Database/ (খালি): ~1 KB
- Database/ (100 পণ্য): ~500 KB
- Database/ (1000 বিক্রয়): ~5-10 MB
- Documentation/: ~500 KB
- Assets/: ~2-5 MB

মোট প্রজেক্ট সাইজ: ~10-15 MB
```

---

## 🚀 বিল্ড এবং ডিস্ট্রিবিউশন

```
confectionery-management-b4a/
  └── B4A কম্পাইল করলে:
      └── confectionery-management-b4a.apk (রিলিজ)
      └── debug ফোল্ডার (ডিবাগিং ফাইল)
```

---

## 📝 কমিট স্ট্রাকচার

প্রতিটি গিট কমিটের সময় মেসেজ ফরম্যাট:

```
[TYPE] Short description

Optional detailed description

- Change 1
- Change 2
- Change 3

Types:
feat:     নতুন ফিচার
fix:      বাগ ফিক্স
docs:     ডকুমেন্টেশন
refactor: কোড পুনর্গঠন
style:    কোড স্টাইল পরিবর্তন
test:     টেস্টিং
chore:    রক্ষণাবেক্ষণ
```

---

## ✅ চেকলিস্ট: নতুন ফিচার যোগ করার সময়

1. ✅ ফিচার নাম এবং উদ্দেশ্য স্পষ্ট করুন
2. ✅ প্রয়োজনীয় ডেটাবেস টেবিল/কলাম যোগ করুন
3. ✅ অনুযায়ী B4A কোড ফাইল তৈরি করুন
4. ✅ Globals.bas এ কনফিগারেশন যোগ করুন
5. ✅ ডকুমেন্টেশন আপডেট করুন
6. ✅ স্যাম্পল ডেটা যোগ করুন (যদি প্রয়োজন)
7. ✅ টেস্টিং করুন
8. ✅ গিট কমিট করুন
9. ✅ README আপডেট করুন

---

## 📚 সম্পর্কিত ফাইল

এই স্ট্রাকচার সম্পর্কে আরও জানুন:
- [README.md](README.md) - প্রধান ডকুমেন্টেশন
- [SETUP_GUIDE.md](SETUP_GUIDE.md) - সেটআপ নির্দেশনা
- [FEATURES.md](Documentation/FEATURES.md) - ফিচার বিবরণ
- [API.md](Documentation/API.md) - API রেফারেন্স

---

*সর্বশেষ আপডেট: জুন ২০২৬*
