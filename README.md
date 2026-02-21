# Backpropagation Fundamentals: Scratch Implementation Guide

এই রিপোজিটরিতে আমি ব্যাকপ্রোপাগেশন এবং নিউরাল নেটওয়ার্কের একদম বেসিক থেকে এডভান্সড কনসেপ্টগুলো 
আমার নিজের হাতের লেখা নোটের মাধ্যমে ব্যাখ্যা করেছি। এখানে রিগ্রেশন প্রবলেমকে 
ফোকাস করে স্ক্র্যাচ থেকে কোডিং লজিক ডেভেলপ করা হয়েছে।


---

## Overvie
ডিপ লার্নিংয়ের মূল ইঞ্জিন হলো **Backpropagation**। এই প্রোজেক্টের উদ্দেশ্য হলো কোনো লাইব্রেরি (যেমন TensorFlow বা PyTorch) ছাড়াই কীভাবে চেইন রুল (Chain Rule) ব্যবহার করে একটি নিউরাল নেটওয়ার্ক ট্রেইন করা যায়, তার গাণিতিক ও কোডিং লজিক বোঝা।



---

## Contents & Summary

### 1. Fundamentals of Training (Page 1-3)
* **Training Definition:** ওয়েট ($W$) এবং বায়াস ($b$) এর অপ্টিমাম মান খুঁজে বের করা।
* **Architecture Design:** রিগ্রেশন সমস্যার জন্য ইনপুট, হিডেন এবং আউটপুট লেয়ার সেটআপ।
* **Initialization:** কেন ছোট র‍্যান্ডম ভ্যালু দিয়ে ওয়েট শুরু করতে হয়।

### 2. Forward Propagation (Page 4-7)
* **Linear Combination:** প্রতিটি নোডের জন্য $Z = W \cdot X + b$ ক্যালকুলেশন।
* **Activation Functions:** কেন সিগময়েড  প্রয়োজন এবং তাদের গাণিতিক প্রভাব।
* **Layer-wise Flow:** এক লেয়ারের আউটপুট কীভাবে অন্য লেয়ারের ইনপুট হয়।



### 3. The Mathematics of Backpropagation (Page 8-11)
* **Loss Function:** MSE (Mean Squared Error) ব্যবহার করে এরর ক্যালকুলেশন।
* **Chain Rule:** আউটপুট থেকে ইনপুটের দিকে ডেরিভেটিভ পাস করার গাণিতিক ব্যাখ্যা।
* **Gradient Calculation:** লস কমানোর জন্য $\frac{\partial L}{\partial w}$ বের করার পদ্ধতি।



### 4. Parameter Update & Implementation (Page 12-14)
* **Gradient Descent:** ওয়েট আপডেট করার মূল সূত্র: $w = w - \eta \cdot dw$।
* **Scratch Code Logic:** লুপ ব্যবহার করে কীভাবে প্রতি ইপোক-এ (Epoch) ওয়েট আপডেট হয়।
* **Result Analysis:** আপডেট করার পর লস কীভাবে কমছে তা পর্যবেক্ষণ।

---
