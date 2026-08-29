📱 iOS APN Profile Generator | سازنده پروفایل APN برای آیفون

English | فارسی

⸻

<div dir="rtl">

فارسی

🌐 ابزار آنلاین ساخت پروفایل APN
[![Live Demo](https://img.shields.io/badge/Launch-iOS_APN_Generator-0A84FF?style=for-the-badge&logo=apple&logoColor=white)](https://soroushse7o.github.io/iOS-APN-Profile-Generator/)

iOS APN Profile Generator یک ابزار آنلاین، ساده، سریع و کاملاً سمت کاربر (Client-Side) برای ساخت پروفایل‌های تنظیمات APN با فرمت .mobileconfig برای iPhone و iPad است.

با استفاده از این ابزار می‌توانید بدون نصب نرم‌افزار اضافی، تنظیمات APN اپراتور خود را وارد کرده و یک پروفایل پیکربندی قابل نصب روی iOS / iPadOS ایجاد کنید.

> ### 🌐 [ورود به ابزار آنلاین iOS APN Profile Generator](https://soroushse7o.github.io/iOS-APN-Profile-Generator/)
> برای ساخت آسان و مستقیم پروفایل‌های تنظیمات APN در iOS روی لینک بالا کلیک کنید.

⸻

✨ ویژگی‌ها

* 🔒 کاملاً سمت کاربر (Client-Side): تمام فرآیند ساخت پروفایل داخل مرورگر انجام می‌شود و برای تولید فایل نیازی به سرور Backend نیست.
* 🛡️ بدون نیاز به ذخیره اطلاعات: اطلاعات واردشده برای تولید پروفایل در یک سرور خارجی ذخیره نمی‌شوند.
* 📱 مخصوص iOS و iPadOS: خروجی با فرمت استاندارد Apple Configuration Profile یعنی .mobileconfig تولید می‌شود.
* 🍎 پشتیبانی از MIME Type اپل: فایل با MIME Type application/x-apple-aspen-config تولید می‌شود تا Safari بتواند آن را به‌عنوان Configuration Profile شناسایی کند.
* ⚡ سریع و سبک: بدون نیاز به نصب نرم‌افزار یا اجرای Backend.
* 🌐 سازگار با Static Hosting: قابل میزبانی روی GitHub Pages، Cloudflare Pages و سایر سرویس‌های میزبانی استاتیک.
* 🔧 پشتیبانی از Payloadهای مختلف APN: شامل Payloadهای مدرن Cellular و Payloadهای Legacy APN.
* 🔐 پشتیبانی از احراز هویت: امکان استفاده از روش‌های PAP و CHAP.
* 🌍 پشتیبانی از IPv4 و IPv6: امکان تنظیم پروتکل‌های شبکه در پروفایل.
* 🌐 پشتیبانی از Proxy: امکان واردکردن Proxy و Port در صورت نیاز اپراتور.
* 💾 تولید مستقیم فایل: پروفایل .mobileconfig مستقیماً توسط مرورگر ایجاد می‌شود.

⸻

📲 نحوه استفاده از ابزار

1️⃣ ورود به ابزار

با Safari در iPhone یا iPad وارد ابزار آنلاین شوید:

🚀 iOS APN Profile Generator

2️⃣ وارد کردن اطلاعات APN

اطلاعات موردنیاز اپراتور خود را در فیلدهای مربوطه وارد کنید.

بسته به تنظیمات ابزار، می‌توانید مواردی مانند موارد زیر را مشخص کنید:

* APN
* Username
* Password
* Authentication Type
* Proxy
* Proxy Port
* IP Protocol

3️⃣ ساخت پروفایل

پس از واردکردن اطلاعات، روی دکمه:

«دانلود و ساخت پروفایل»

بزنید.

ابزار فایل .mobileconfig را در مرورگر ایجاد می‌کند.

⸻

📲 نحوه نصب پروفایل در آیفون

پس از ساخت پروفایل:

1. ابزار را با Safari باز کنید.
2. اطلاعات APN را وارد کنید.
3. روی دانلود و ساخت پروفایل بزنید.
4. در پیام Safari گزینه Allow را انتخاب کنید.
5. وارد Settings شوید.
6. در بالای صفحه گزینه Profile Downloaded را انتخاب کنید.
7. روی Install بزنید.
8. در صورت درخواست، Passcode دستگاه را وارد کنید.
9. مراحل نصب را تا پایان ادامه دهید.

⚠️ توجه: استفاده از APN یا تنظیمات نادرست می‌تواند باعث اختلال یا قطع اتصال اینترنت همراه شود. همیشه مقادیر صحیح APN را از اپراتور خود دریافت کنید.

⸻

📊 مراحل تست و نتایج اتصال IPv6 / Dual-Stack

یکی از سناریوهای آزمایش این پروژه، بررسی تأثیر تنظیمات سفارشی APN بر فعال‌شدن IPv4/IPv6 Dual-Stack و اتصال سرویس‌هایی مانند Cloudflare WARP بوده است.

۱. تنظیمات پیش‌فرض سیستم	۲. اعمال پروفایل سفارشی	۳. اتصال Cloudflare WARP
IPv6 غیرفعال	فعال‌سازی Dual-Stack	برقراری اتصال WARP
		
تست IPv6 ناموفق	دریافت IPv6 از شبکه اپراتور	برقراری اتصال WARP

🔬 توضیحات فنی مراحل آزمایش

تصویر اول — Default Settings

در تنظیمات پیش‌فرض این سناریو، اتصال IPv6 برقرار نشده و تست با خطای:

IPv6 test not reachable

مواجه شد.

تصویر دوم — Custom Profile

با اعمال مقدار:

AllowedProtocolMask = 3

پروتکل‌های IPv4 و IPv6 در پروفایل مجاز شدند و در صورت پشتیبانی شبکه اپراتور، دستگاه توانست اتصال Dual-Stack برقرار کرده و یک آدرس IPv6 دریافت کند.

تصویر سوم — WARP Established

پس از برقرارشدن اتصال IPv6، کلاینت Cloudflare WARP توانست ارتباط خود را برقرار کرده و تونل WARP ایجاد کند.

ℹ️ نکته: این نتیجه به اپراتور، شبکه، مدل دستگاه، نسخه iOS و تنظیمات شبکه بستگی دارد. فعال‌کردن IPv6 در پروفایل به‌تنهایی تضمین نمی‌کند که دستگاه حتماً IPv6 دریافت کند یا Cloudflare WARP متصل شود.

⸻

🌐 استفاده آنلاین

اگر فقط می‌خواهید پروفایل APN خود را بسازید، نیازی به دریافت یا نصب سورس پروژه ندارید.

👉 🚀 ورود مستقیم به ابزار آنلاین

ابزار مستقیماً در مرورگر اجرا می‌شود و می‌توانید پروفایل .mobileconfig موردنظر خود را ایجاد کنید.

⸻

📱 Cloudflare WARP

برای استفاده از Cloudflare WARP می‌توانید برنامه رسمی 1.1.1.1: Faster Internet را از App Store دریافت کنید.

<a href="https://apps.apple.com/us/app/1-1-1-1-faster-internet/id1423538627" target="_blank">
  <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83" alt="Download on the App Store" width="160">
</a>

⸻

🛠️ استقرار پروژه

این پروژه برای اجرا به Backend یا Database نیاز ندارد و می‌توان آن را به‌صورت یک وب‌سایت استاتیک میزبانی کرد.

سرویس‌های مناسب برای میزبانی

* GitHub Pages
* Cloudflare Pages
* سایر Static Hostingها

ساختار پروژه

iOS-APN-Profile-Generator/
├── index.html
├── screenshot/
│   ├── 1-before.png
│   ├── 2-after.png
│   └── warp.png
└── README.md

⸻

🔐 حریم خصوصی

این پروژه با رویکرد Client-Side طراحی شده است.

اطلاعاتی مانند:

* APN
* Username
* Password
* Proxy
* Proxy Port
* سایر تنظیمات واردشده

برای تولید پروفایل در مرورگر پردازش می‌شوند و برای ساخت فایل .mobileconfig به Backend نیاز نیست.

⚠️ حریم خصوصی نهایی وب‌سایت می‌تواند به تنظیمات سرویس میزبانی و کدهای اضافه‌شده به پروژه نیز وابسته باشد.

⸻

📄 مجوز

این پروژه تحت MIT License منتشر شده است.

استفاده، کپی، تغییر و انتشار مجدد پروژه مطابق شرایط مجوز MIT آزاد است.

</div>

⸻

English

🌐 Online APN Profile Generator

iOS APN Profile Generator is a simple, fast, fully client-side online tool for creating custom APN configuration profiles in the .mobileconfig format for iPhone and iPad.

The tool allows you to enter your carrier’s APN settings and generate an Apple Configuration Profile directly in your browser without installing additional software or using a backend server.

🚀 Launch the Online Tool

📱 Open iOS APN Profile Generator

Click the link above to open the online generator and create an APN profile.

The tool runs directly in your browser and does not require an account or additional software.

⸻

✨ Features

* 🔒 Fully Client-Side: The profile is generated directly in the browser without requiring a backend server.
* 🛡️ No Profile Data Storage: User-provided values are not sent to an external server for profile generation.
* 📱 Built for iOS / iPadOS: Generates Apple Configuration Profiles using the .mobileconfig format.
* 🍎 Apple Configuration MIME Type: Uses application/x-apple-aspen-config so Safari can recognize the file as an Apple Configuration Profile.
* ⚡ Fast and Lightweight: No additional software or backend infrastructure is required.
* 🌐 Static Hosting Compatible: Can be hosted on GitHub Pages, Cloudflare Pages, or other static hosting services.
* 🔧 APN Payload Support: Supports modern Cellular payloads as well as legacy APN payloads.
* 🔐 Authentication Support: Supports PAP and CHAP authentication.
* 🌍 IPv4 / IPv6 Support: Allows IPv4 and IPv6 protocol configuration.
* 🌐 Proxy Support: Allows custom proxy and port configuration when required.
* 💾 Direct Profile Generation: The .mobileconfig file is generated directly by the browser.

⸻

📲 How to Use the Online Tool

1️⃣ Open the Generator

Open the online generator using Safari on your iPhone or iPad:

🚀 iOS APN Profile Generator

2️⃣ Enter Your APN Information

Enter the APN information provided by your mobile carrier.

Depending on the available options, you can configure:

* APN
* Username
* Password
* Authentication Type
* Proxy
* Proxy Port
* IP Protocol

3️⃣ Generate the Profile

After entering the required information, tap:

Generate Profile / دانلود و ساخت پروفایل

The .mobileconfig file will be generated directly in your browser.

⸻

📲 How to Install the Profile on iPhone

After generating the profile:

1. Open the generator using Safari.
2. Enter your APN information.
3. Tap Generate Profile.
4. Select Allow when Safari asks to download the configuration profile.
5. Open Settings.
6. Tap Profile Downloaded near the top of the page.
7. Tap Install.
8. Enter your device passcode if requested.
9. Follow the remaining installation steps.

⚠️ Important: Incorrect APN or network settings may cause cellular data connectivity problems. Always use the correct APN values provided by your mobile carrier.

⸻

📊 IPv6 / Dual-Stack Connectivity Test

One of the project’s test scenarios examines the effect of custom APN configuration on IPv4/IPv6 Dual-Stack connectivity and services such as Cloudflare WARP.

1. Default System Configuration	2. Custom Profile Applied	3. Cloudflare WARP Connection
IPv6 Disabled	Dual-Stack Enabled	WARP Connection Established
		
IPv6 connectivity test failed	IPv6 address assigned by carrier	WARP connection established

🔬 Technical Test Details

Image 1 — Default Settings

In the default configuration used in this test scenario, IPv6 connectivity was unavailable and the test returned:

IPv6 test not reachable

Image 2 — Custom Profile

The custom profile enabled IPv4 and IPv6 by setting:

AllowedProtocolMask = 3

When supported by the carrier network, the device was able to establish Dual-Stack connectivity and obtain an IPv6 address.

Image 3 — WARP Established

After IPv6 connectivity became available, the Cloudflare WARP client was able to establish its connection and create the WARP tunnel.

ℹ️ Note: Results may vary depending on the carrier, network, device model, iOS version, and network configuration. Enabling IPv6 in a configuration profile alone does not guarantee IPv6 connectivity or Cloudflare WARP functionality.

⸻

🌐 Use the Online Generator

If you only want to create an APN profile, you do not need to download or install the project source code.

👉 🚀 Open the Online APN Profile Generator

The tool runs directly in your browser and allows you to generate your .mobileconfig profile online.

⸻

📱 Cloudflare WARP

You can install the official 1.1.1.1: Faster Internet application from the App Store if you want to use Cloudflare WARP.

<a href="https://apps.apple.com/us/app/1-1-1-1-faster-internet/id1423538627" target="_blank">
  <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83" alt="Download on the App Store" width="160">
</a>

⸻

🛠️ Deployment

The project does not require a backend server or database and can be hosted as a static website.

Recommended Hosting

* GitHub Pages
* Cloudflare Pages
* Other static hosting services

Project Structure

iOS-APN-Profile-Generator/
├── index.html
├── screenshot/
│   ├── 1-before.png
│   ├── 2-after.png
│   └── warp.png
└── README.md

⸻

🔐 Privacy

This project is designed to operate entirely on the client side.

Information such as:

* APN
* Username
* Password
* Proxy
* Proxy Port
* Other configuration values

is processed in the browser and does not require a backend server to generate the .mobileconfig file.

⚠️ The overall privacy of the website may also depend on the hosting configuration and any additional code integrated into the project.

⸻

📄 License

This project is released under the MIT License.

You are free to use, copy, modify, and redistribute the project according to the terms of the MIT License.