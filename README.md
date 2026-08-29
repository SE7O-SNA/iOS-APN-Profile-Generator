📱 iOS APN Profile Generator | سازنده پروفایل APN برای آیفون

فارسی | English

⸻

<div dir="rtl">

فارسی

iOS APN Profile Generator یک ابزار تحت وب سبک، سریع و کاملاً سمت کاربر (Client-Side) برای ساخت پروفایل‌های پیکربندی Apple با فرمت .mobileconfig است.

این ابزار به شما امکان می‌دهد تنظیمات سفارشی APN (Access Point Name) را برای دستگاه‌های iPhone و iPad ایجاد و به‌صورت مستقیم روی iOS / iPadOS نصب کنید.

تمام فرآیند تولید پروفایل در مرورگر انجام می‌شود و اطلاعات واردشده برای ساخت پروفایل به سرور ارسال نمی‌شوند.

✨ ویژگی‌ها

* 🔒 کاملاً Client-Side — پروفایل مستقیماً داخل مرورگر تولید می‌شود و نیازی به سرور یا پایگاه داده ندارد.
* 📱 مخصوص iOS / iPadOS — خروجی در قالب استاندارد Apple Configuration Profile با پسوند .mobileconfig تولید می‌شود.
* 🌐 سازگار با هاست‌های استاتیک — قابل اجرا روی GitHub Pages، Cloudflare Pages و سایر سرویس‌های Static Hosting.
* ⚡ بدون نیاز به Build یا Backend — پروژه به‌صورت ساده و سبک اجرا می‌شود.
* 🍎 پشتیبانی از MIME Type اپل — فایل با MIME Type استاندارد application/x-apple-aspen-config تولید می‌شود.
* 🔧 پشتیبانی از Payloadهای APN — امکان تولید Payloadهای مدرن Cellular و Payloadهای Legacy APN.
* 🔐 احراز هویت — پشتیبانی از روش‌های PAP و CHAP.
* 🌍 پشتیبانی از IPv4 و IPv6 — امکان تنظیم پروتکل‌های شبکه در صورت پشتیبانی اپراتور و دستگاه.
* 🌐 تنظیم Proxy — امکان تعریف Proxy و Port در پروفایل.
* 💾 بدون ذخیره‌سازی اطلاعات — اطلاعات واردشده برای تولید پروفایل در سرویس خارجی ذخیره نمی‌شوند.

📲 نحوه ساخت و نصب پروفایل در آیفون

1. با مرورگر Safari در iPhone یا iPad وارد ابزار شوید.
2. اطلاعات APN موردنظر خود را وارد کنید.
3. روی دانلود و ساخت پروفایل بزنید.
4. در پیام نمایش‌داده‌شده توسط Safari، گزینه Allow را انتخاب کنید.
5. وارد Settings شوید.
6. گزینه Profile Downloaded را انتخاب کنید.
7. روی Install بزنید و مراحل نصب را ادامه دهید.

⚠️ توجه: استفاده از APN یا تنظیمات نادرست ممکن است باعث قطع اتصال اینترنت یا اختلال در اتصال داده همراه شود. مقادیر APN باید مطابق اطلاعات ارائه‌شده توسط اپراتور شما باشند.

🌐 ابزار آنلاین

🚀 ورود به iOS APN Profile Generator

برای ساخت پروفایل APN به‌صورت آنلاین و مستقیم روی iPhone یا iPad از ابزار بالا استفاده کنید.

⸻

📊 تست و بررسی اتصال IPv6 / Dual-Stack

در این پروژه، تأثیر اعمال تنظیمات سفارشی APN بر فعال‌شدن IPv4/IPv6 Dual-Stack نیز بررسی شده است.

۱. تنظیمات پیش‌فرض	۲. اعمال پروفایل سفارشی	۳. بررسی اتصال WARP
IPv6 غیرفعال	فعال‌شدن Dual-Stack	اتصال از طریق IPv6
		
تست ناموفق IPv6	دریافت IPv6 از شبکه اپراتور	برقراری اتصال WARP

🔬 توضیح فنی

تصویر اول — Default Settings

در این آزمایش، تنظیمات پیش‌فرض APN روی دستگاه باعث شد اتصال IPv6 برقرار نشود و تست IPv6 با خطای IPv6 test not reachable مواجه شود.

تصویر دوم — Custom Profile

با اعمال مقدار:

AllowedProtocolMask = 3

پروتکل‌های IPv4 و IPv6 در پروفایل مجاز شدند و دستگاه، در صورت پشتیبانی شبکه اپراتور، امکان دریافت آدرس IPv6 را پیدا کرد.

تصویر سوم — WARP

پس از فراهم‌شدن اتصال IPv6، کلاینت Cloudflare WARP توانست ارتباط خود را برقرار کند و تونل شبکه ایجاد شود.

ℹ️ نتیجه این آزمایش به تنظیمات اپراتور، شبکه، دستگاه و نسخه iOS وابسته است و فعال‌کردن IPv6 در پروفایل به‌تنهایی تضمین‌کننده دریافت IPv6 یا برقراری WARP نیست.

📱 Cloudflare 1.1.1.1 / WARP

<a href="https://apps.apple.com/us/app/1-1-1-1-faster-internet/id1423538627" target="_blank">
  <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83" alt="Download on the App Store" width="160">
</a>

⸻

🛠️ اجرا و استفاده

این پروژه برای اجرا به Backend یا Database نیاز ندارد.

کافی است فایل‌های پروژه را روی یک سرویس Static Hosting مانند GitHub Pages یا Cloudflare Pages قرار دهید.

ساختار کلی پروژه

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
* سایر مقادیر واردشده

برای تولید پروفایل در مرورگر پردازش می‌شوند و پروژه برای تولید فایل .mobileconfig به Backend نیاز ندارد.

با این حال، حریم خصوصی نهایی به سرویس Hosting و نحوه استفاده از وب‌سایت نیز وابسته است.

⸻

📄 مجوز

این پروژه تحت MIT License منتشر شده است.

استفاده، کپی، تغییر و انتشار مجدد پروژه مطابق شرایط مجوز MIT آزاد است.

</div>

⸻

English

iOS APN Profile Generator is a lightweight, fast, fully client-side web utility for generating Apple Configuration Profiles (.mobileconfig) with custom APN (Access Point Name) settings.

The tool is designed for iPhone and iPad devices running iOS / iPadOS and allows users to generate and install custom cellular configuration profiles directly from Safari.

The profile is generated locally in the browser, without requiring a backend server or database.

✨ Features

* 🔒 Fully Client-Side — Profiles are generated directly in the browser without requiring a backend.
* 📱 Designed for iOS / iPadOS — Generates Apple Configuration Profiles using the .mobileconfig format.
* 🌐 Static Hosting Compatible — Works with GitHub Pages, Cloudflare Pages, and other static hosting services.
* ⚡ No Build or Backend Required — Lightweight and simple to deploy.
* 🍎 Apple Configuration MIME Type — Uses the standard application/x-apple-aspen-config MIME type.
* 🔧 APN Payload Support — Supports modern Cellular payloads as well as legacy APN payloads.
* 🔐 Authentication Support — Supports PAP and CHAP authentication.
* 🌍 IPv4 / IPv6 Support — Allows network protocol configuration where supported by the carrier and device.
* 🌐 Proxy Configuration — Supports custom proxy and port settings.
* 💾 No Profile Data Storage — User-provided values are not stored on an external server for profile generation.

📲 How to Generate and Install a Profile on iOS

1. Open the tool in Safari on your iPhone or iPad.
2. Enter the required APN information.
3. Tap Generate Profile / دانلود و ساخت پروفایل.
4. When Safari displays the download prompt, tap Allow.
5. Open Settings.
6. Tap Profile Downloaded.
7. Tap Install and follow the on-screen instructions.

⚠️ Important: Incorrect APN or network settings may cause cellular data connectivity issues. Always use APN values provided or recommended by your mobile carrier.

🌐 Online Tool

🚀 Launch iOS APN Profile Generator

Use the online tool to generate custom APN configuration profiles directly from your iPhone or iPad.

⸻

📊 IPv6 / Dual-Stack Connectivity Test

The project also includes an experimental test demonstrating the effect of custom APN configuration on IPv4/IPv6 Dual-Stack connectivity.

1. Default Configuration	2. Custom Profile	3. WARP Connectivity
IPv6 Disabled	Dual-Stack Enabled	IPv6 Connectivity
		
IPv6 test failure	IPv6 address assigned by carrier	WARP connection established

🔬 Technical Details

Image 1 — Default Settings

In the test scenario, the device did not establish IPv6 connectivity using the default APN configuration, resulting in an IPv6 test not reachable error.

Image 2 — Custom Profile

The custom profile enabled both IPv4 and IPv6 by setting:

AllowedProtocolMask = 3

When supported by the carrier and device, this allowed the cellular connection to operate using IPv4/IPv6 Dual-Stack networking.

Image 3 — WARP

After IPv6 connectivity became available, the Cloudflare WARP client was able to establish its network connection and create the WARP tunnel.

ℹ️ The result of this test depends on the carrier network, device, iOS version, and network configuration. Enabling IPv6 in a configuration profile does not by itself guarantee IPv6 connectivity or WARP functionality.

📱 Cloudflare 1.1.1.1 / WARP

<a href="https://apps.apple.com/us/app/1-1-1-1-faster-internet/id1423538627" target="_blank">
  <img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83" alt="Download on the App Store" width="160">
</a>

⸻

🛠️ Deployment

The project does not require a backend server or database.

Simply host the project files on a static hosting service such as GitHub Pages or Cloudflare Pages.

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

Values such as:

* APN
* Username
* Password
* Proxy settings
* Other configuration values

are processed locally in the browser. The project does not require a backend server to generate the .mobileconfig file.

However, overall privacy may also depend on the hosting provider and how the website is configured.

⸻

📄 License

This project is released under the MIT License.

You are free to use, modify, copy, and redistribute the project according to the terms of the MIT License.