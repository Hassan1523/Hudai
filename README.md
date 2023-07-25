# ক্যালকুলেটর ফাংশন ডেফাইন করুন
def calculator():
    print("স্বাগতম ক্যালকুলেটরে!")
    while True:
        try:
            # সংখ্যা ইনপুট গ্রহণ করুন
            num1 = float(input("প্রথম সংখ্যা প্রবেশ করুন: "))
            operator = input("গণিতিক অপারেশন (+, -, *, /) নির্বাচন করুন: ")
            num2 = float(input("দ্বিতীয় সংখ্যা প্রবেশ করুন: "))

            # গণিতিক অপারেশন প্রয়োগ এবং ফলাফল প্রদর্শন করুন
            if operator == '+':
                result = num1 + num2
            elif operator == '-':
                result = num1 - num2
            elif operator == '*':
                result = num1 * num2
            elif operator == '/':
                result = num1 / num2
            else:
                print("অপরিচিত গণিতিক অপারেশন! আবার চেষ্টা করুন।")
                continue

            print("ফলাফল: ", result)

            # আরও কাজ করতে চাইলে প্রয়োজনীয়ভাবে প্রকারন করুন
            another_calculation = input("আরেকটি ক্যালকুলেশন করতে চান? (হ্যা/না): ")
            if another_calculation.lower() == 'না':
                print("ক্যালকুলেটর থেমে গেছে।")
                break

        except ValueError:
            print("ভুল ইনপুট! দয়া করে সঠিক সংখ্যা প্রবেশ করুন।")

# ক্যালকুলেটর কল করুন
calculator()
