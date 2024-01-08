---
layout: page
title: DRF Basic Authetication
date: 
thumbnail: images/raspberrypi-thumb.png
permalink: drf-basic-auth-notes
showAuthor: true
showDate: true
showReadingTime: true
showTableOfContents: true
showSummary: true
showComments: true
tags:
  - DRF
  - Django
  - Authentication
  - BAsic
  - Basic-Athentication
---
আজকে আমরা ব্যাসিক Authentication implementation করবো । তার জন্য প্রথমে আমাদের আমাদের ডিজ্যাঙ্গু এপ এর ==settings.py== ফাইল এর মধ্যে আমাদের Rest Framework এর কিছু সেটিংস ইম্পর্ট করে নিতে হবে । 

```python
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework.authentication.BasicAuthentication',
    ]
}
```

উপরের কোড গুলো আমরা আগে ইম্পর্ট করে নিব । 
তবে যদি আগে থেকেই আমাদের অন্য কোন সেটিংস আগে থেকে ইম্পোর্ট করা থাকে তাহলে এইটি নতুন করে ইম্পর্ট করার দরকার নেই  শুধু মাত্র ক্লাসটি ইম্পর্ট করলেই কাজ হয়ে যাবে । 



![[Pasted image 20240108194807.png]]![[Pasted image 20240108194934.png]]

তবে মনে রাখবেন আপনি কোনভাবেই সেটিংস দুইবার ইম্পোর্ট করবেন ২য়টি প্রথমটির উপর ওভাররাইড করবে ফলে প্রথম সেটিংসটি কাজ করবে না । 
