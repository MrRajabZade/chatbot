# ChatBot
به چت بات آموزش دهید و چت بات خود را بسازید.

## آموزش چت بات
چت بات برای پاسخ گویی به کاربر از الگویی استفاده میکند که شما باید این الگو ها را تعیین کنید. برای تعیین الگوی چت بات به فایل rulse.txt بروید و با توجه به ویژگی ها الگو مناسب را برای چت بات خود بنویسید.

در هر الگو متن قبل از دو نقطه نشانگر الگویی از سوی کاربر و متن بعد از دو نقطه نشانگر الگویی پاسخی از سوی ربات است.
```
سلام : سلام چطوری؟
```
### ویژگی ها:

- حذف کلمات قبل از پردازش:

میتوانید بعضی کلمات رو از متن کاربر حذف کنید تا پردازش نشود برای مثال:
```
stopwords = [از، با، در]
```
- استفاده از متغیر برای پاسخ گویی:

میتوانید برای سهولت در پاسخ گویی از متغیر استفاده کنید. برای مثال:
```
iran = eeee 
Irani = p
+ 
iran? : #iran #Irani
```

۱- استفاده از متغیر ها محدودیت نداره

۲- باید بین وارد کردن متغییر ها و متن ها همیشه کلمه + باشد حتی اگر متغیری وجود نداشته باشد مانند مثال بالا.

۳- اگر اسم دو متغیر شبیه به هم است با بزرگ و کوچک کردن کلمات آن را شباهت خارج کنید تا مشکلی پیش نیاید مانند مثال بالا.

- پارامتر *:

پارامتر * مثل یک متغییر عمل میکند که میتوانید از آن برای استفاده در متن پاسخ استفاده کنید. برای مثال:
```
اسم من * است : سلام * عزیز.
```
- بخاطر سپردن اطلاعات:

اگر بخواهید یه اطلاعاتی مانند اسم کاربر و .. را در ربات دخیره کنید میتوانید از این ویژگی استفاده کنید. برای مثال:
```
پایتون چیست؟ : #پایتون (موضوع = پایتون)
```
- پردازش تو در تو:

برای زمان هایی که دارید از کاربر سوالاتی رو میپرسید و باید نسبت به پاسخ اون سوال پاسخ جدیدی به او بدهید میتوانید از این ویژگی استفاده کنید. برای مثال: 
```
حالم بده : بیماری؟ (بله : متاسفم (چه کار کنم؟ : برو بخواب (بخوابم؟ : آره (وای سرگیجه دارم : حالت خوبه؟))))
```

- استفاده از پاسخ های احتمالی:

از این ویژگی می‌شود در زمان هایی که ممکن است کاربر پاسخ احتمالی دهد استفاده کنید. برای مثال:
```
خوبی {فلانی، داداش} : آره
```
- پاسخ های تصادفی:

شما به عنوان یک برنامه شاید بخواهید ربات در صورت دریافت متنی از کاربر به آن پاسخ های احتمالی دهد. برای مثال:
```
چطوری : خوبم [مرسی,تشکر]
```

## تست چت بات

بعد از نوشتن الگو برای چت بات نوبت تست آن است که برای این کار فایل main.py رو اجرا کنید و از قبل باید پایتون نسخه 3 به بالا و کتابخانه tkinter را نصب داشته باشید.

حال براساس الگویی که نوشتید میتوانید از چت بات سوال بپرسید و پاسخ دریافت کنید.
