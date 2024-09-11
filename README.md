# ESP FreeFire

<div style="text-align: center;">
<b>ESP source code for Free Fire (iOS jailbreak, Free Fire version: 1.93.1).</b><br><br>

<img src="https://raw.githubusercontent.com/34306/ESP_FreeFire/main/Preview.PNG">
</div>

___
<br>

### This source is for learning purpose only, please do not use it for commercial purpose!
- Known issue: Maybe it's laggy when play on Survival Mode, you can fix it yourself by limit the distance that draw the ESP.
### Many thanks to
- [Kitty Memory](https://github.com/MJx0/KittyMemory) by [MJx0](https://github.com/MJx0)
- [Ted 2 Template menu](https://github.com/joeyjurjens/iOS-Mod-Menu-Template-for-Theos) by [joeyjurjens](https://github.com/joeyjurjens)
- And Zeus from [iOSGods](https://iosgods.com)
pip install paypalrestsdk
import paypalrestsdk
import logging

# إعداد إعدادات PayPal
paypalrestsdk.configure({
  "mode": "live",  # استخدم "sandbox KTK7S3XAQ6LNW
  للاختبار
  "client_id": "YOUR_CLIENT_ID",
  "client_secret": "YOUR_CLIENT_SECRET"
})

logging.basicConfig(level=logging.INFO)
payment = paypalrestsdk.Payment({
    "intent": "sale",
    "payer": {
        "payment_method": "paypal"},
    "transactions": [{
        "amount": {
            "total": "5.00",
            "currency": "USD"},
        "description": "دفع 5 دولارات لتفعيل التطبيق أو الموقع"}],
    "redirect_urls": {
        "return_url": "https://example.com/payment/execute",
        "cancel_url": "https://example.com/payment/cancel"}})

if payment.create():
    print("Payment created successfully")
    for link in payment.links:
        if link.rel == "approval_url":
            approval_url = str(link.href)
            print("Redirect for approval: %s" % (approval_url))
else:
    print(payment.error)
  "mode": "live",  # استخدم "sandbox KTK7S3XAQ6LNW
payment_id = "PAYMENT_ID_FROM_PAYPAl
  "mode": "live",  # استخدم "sandbox KTK7S3XAQ6LNW"

payer_id = "PAYER_ID_FROM_PAYPAL"

payment = paypalrestsdk.Payment.find(payment_id)

if payment.execute({"payer_id": payer_id}):
    print("Payment executed successfully")
    # هنا يمكنك فتح الموقع أو التطبيق للمستخدم بعد الدفع
else:
    print(payment.error)
payment_id = "PAYMENT_ID_FROM_PAYPAL"
payer_id = "PAYER_ID_FROM_PAYPAL"

payment = paypalrestsdk.Payment.find(payment_id  "mode": "live",  # استخدم "sandbox KTK7S3XAQ6LNW)


