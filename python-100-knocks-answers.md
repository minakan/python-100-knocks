# Python基礎100本ノック - 解答集

## 基本操作編 (1-10)

### 1. 「Hello, World!」と出力するプログラム
```python
print("Hello, World!")
```

### 2. 変数に自分の名前を代入し、「こんにちは、[名前]さん！」と出力するプログラム
```python
name = "太郎"  # 自分の名前を代入
print(f"こんにちは、{name}さん！")
```

### 3. 二つの数値を入力として受け取り、その和を出力するプログラム
```python
a = float(input("1つ目の数値を入力してください: "))
b = float(input("2つ目の数値を入力してください: "))
print(f"合計: {a + b}")
```

### 4. 数値を入力として受け取り、その数値が偶数か奇数かを判定するプログラム
```python
num = int(input("数値を入力してください: "))
if num % 2 == 0:
    print(f"{num}は偶数です。")
else:
    print(f"{num}は奇数です。")
```

### 5. 1から10までの数字を出力するプログラム
```python
for i in range(1, 11):
    print(i)
```

### 6. 1から100までの数字の合計を計算して出力するプログラム
```python
total = sum(range(1, 101))
print(f"1から100までの合計: {total}")
```

### 7. リストに好きな果物の名前を5つ追加し、それらを一行ずつ出力するプログラム
```python
fruits = ["りんご", "バナナ", "オレンジ", "ぶどう", "いちご"]
for fruit in fruits:
    print(fruit)
```

### 8. 辞書に3人の名前と年齢を格納し、「[名前]は[年齢]歳です。」という形式で出力するプログラム
```python
people = {
    "田中": 25,
    "鈴木": 30,
    "佐藤": 22
}
for name, age in people.items():
    print(f"{name}は{age}歳です。")
```

### 9. ユーザーから入力を受け取り、その文字列の長さを出力するプログラム
```python
text = input("何か文字列を入力してください: ")
print(f"入力された文字列の長さは{len(text)}文字です。")
```

### 10. 2つの文字列を連結して出力するプログラム
```python
str1 = input("1つ目の文字列を入力してください: ")
str2 = input("2つ目の文字列を入力してください: ")
print(f"連結結果: {str1 + str2}")
```

## 条件分岐編 (11-20)

### 11. 3つの数値を入力として受け取り、最大値を出力するプログラム
```python
a = float(input("1つ目の数値を入力してください: "))
b = float(input("2つ目の数値を入力してください: "))
c = float(input("3つ目の数値を入力してください: "))
max_value = max(a, b, c)
print(f"最大値: {max_value}")
```

### 12. 年齢を入力として受け取り、成人（18歳以上）かどうかを判定するプログラム
```python
age = int(input("年齢を入力してください: "))
if age >= 18:
    print("成人です。")
else:
    print("未成年です。")
```

### 13. 数値を入力として受け取り、正の数、負の数、またはゼロかを判定するプログラム
```python
num = float(input("数値を入力してください: "))
if num > 0:
    print("正の数です。")
elif num < 0:
    print("負の数です。")
else:
    print("ゼロです。")
```

### 14. 三角形の3辺の長さを入力として受け取り、その三角形が正三角形、二等辺三角形、または不等辺三角形かを判定するプログラム
```python
a = float(input("1つ目の辺の長さを入力してください: "))
b = float(input("2つ目の辺の長さを入力してください: "))
c = float(input("3つ目の辺の長さを入力してください: "))

if a + b <= c or a + c <= b or b + c <= a:
    print("三角形が作れません。")
elif a == b == c:
    print("正三角形です。")
elif a == b or b == c or a == c:
    print("二等辺三角形です。")
else:
    print("不等辺三角形です。")
```

### 15. 西暦年を入力として受け取り、うるう年かどうかを判定するプログラム
```python
year = int(input("西暦年を入力してください: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year}年はうるう年です。")
else:
    print(f"{year}年はうるう年ではありません。")
```

### 16. 文字列を入力として受け取り、その文字列が回文（前から読んでも後ろから読んでも同じ）かどうかを判定するプログラム
```python
text = input("文字列を入力してください: ")
if text == text[::-1]:
    print("回文です。")
else:
    print("回文ではありません。")
```

### 17. 身長（cm）と体重（kg）を入力として受け取り、BMI（体重÷身長の2乗）を計算し、肥満度を判定するプログラム
```python
height = float(input("身長（cm）を入力してください: ")) / 100  # mに変換
weight = float(input("体重（kg）を入力してください: "))
bmi = weight / (height ** 2)
print(f"BMI: {bmi:.2f}")

if bmi < 18.5:
    print("低体重（やせ型）")
elif bmi < 25:
    print("普通体重")
elif bmi < 30:
    print("肥満（1度）")
elif bmi < 35:
    print("肥満（2度）")
elif bmi < 40:
    print("肥満（3度）")
else:
    print("肥満（4度）")
```

### 18. 1から100までの数字のうち、3の倍数のとき「Fizz」、5の倍数のとき「Buzz」、3と5の両方の倍数のとき「FizzBuzz」、それ以外のときはその数字を出力するプログラム
```python
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
```

### 19. 月の番号（1〜12）を入力として受け取り、その月の日数を出力するプログラム
```python
month = int(input("月の番号（1〜12）を入力してください: "))
days_in_month = {
    1: 31, 2: 28, 3: 31, 4: 30, 5: 31, 6: 30,
    7: 31, 8: 31, 9: 30, 10: 31, 11: 30, 12: 31
}

if month in days_in_month:
    print(f"{month}月は{days_in_month[month]}日あります。（うるう年を考慮していません）")
else:
    print("無効な月番号です。1から12までの数字を入力してください。")
```

### 20. 数値を入力として受け取り、その数値が素数かどうかを判定するプログラム
```python
def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

num = int(input("数値を入力してください: "))
if is_prime(num):
    print(f"{num}は素数です。")
else:
    print(f"{num}は素数ではありません。")
```

## ループ処理編 (21-30)

### 21. 1から10までの数字の二乗を計算して出力するプログラム
```python
for i in range(1, 11):
    print(f"{i}の二乗は{i**2}です。")
```

### 22. リストの要素を逆順に出力するプログラム
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
for num in reversed(numbers):
    print(num)
```

### 23. 1から100までの数字のうち、3の倍数と5の倍数の合計を別々に計算して出力するプログラム
```python
sum_of_multiples_of_3 = 0
sum_of_multiples_of_5 = 0

for i in range(1, 101):
    if i % 3 == 0:
        sum_of_multiples_of_3 += i
    if i % 5 == 0:
        sum_of_multiples_of_5 += i

print(f"3の倍数の合計: {sum_of_multiples_of_3}")
print(f"5の倍数の合計: {sum_of_multiples_of_5}")
```

### 24. フィボナッチ数列の最初の20項を出力するプログラム
```python
a, b = 0, 1
for _ in range(20):
    print(a, end=" ")
    a, b = b, a + b
print()  # 改行
```

### 25. ユーザーが「quit」と入力するまで、入力を受け取り続けるプログラム
```python
while True:
    user_input = input("何か入力してください（終了するには「quit」と入力）: ")
    if user_input.lower() == "quit":
        print("プログラムを終了します。")
        break
    print(f"入力されたテキスト: {user_input}")
```

### 26. リストの中から最大値と最小値を見つけて出力するプログラム
```python
numbers = [34, 12, 56, 78, 23, 45, 67, 89, 10]
print(f"最大値: {max(numbers)}")
print(f"最小値: {min(numbers)}")
```

### 27. 九九の表（1×1から9×9まで）を出力するプログラム
```python
for i in range(1, 10):
    for j in range(1, 10):
        print(f"{i} × {j} = {i*j}")
```

### 28. 数値を入力として受け取り、その数値の階乗を計算して出力するプログラム
```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

num = int(input("数値を入力してください: "))
if num < 0:
    print("負の数の階乗は定義されていません。")
else:
    result = factorial(num)
    print(f"{num}の階乗は{result}です。")
```

### 29. リストの要素の平均値を計算して出力するプログラム
```python
numbers = [23, 45, 67, 89, 12, 34, 56, 78]
average = sum(numbers) / len(numbers)
print(f"平均値: {average}")
```

### 30. 2つのリストの共通要素を見つけて出力するプログラム
```python
list1 = [1, 2, 3, 4, 5, 6, 7]
list2 = [5, 6, 7, 8, 9, 10]
common_elements = list(set(list1) & set(list2))
print(f"共通要素: {common_elements}")
```

## 文字列操作編 (31-40)

### 31. 文字列を入力として受け取り、その文字列を逆順にして出力するプログラム
```python
text = input("文字列を入力してください: ")
reversed_text = text[::-1]
print(f"逆順: {reversed_text}")
```

### 32. 文字列を入力として受け取り、その文字列に含まれる母音（a, e, i, o, u）の数を数えるプログラム
```python
text = input("英文を入力してください: ").lower()
vowels = "aeiou"
count = sum(1 for char in text if char in vowels)
print(f"母音の数: {count}")
```

### 33. 文字列を入力として受け取り、各単語の先頭文字を大文字にするプログラム
```python
text = input("文字列を入力してください: ")
capitalized_text = text.title()
print(f"変換後: {capitalized_text}")
```

### 34. 文字列を入力として受け取り、各文字の出現回数を数えるプログラム
```python
text = input("文字列を入力してください: ")
char_count = {}
for char in text:
    if char in char_count:
        char_count[char] += 1
    else:
        char_count[char] = 1

for char, count in char_count.items():
    print(f"'{char}': {count}回")
```

### 35. カンマ区切りの文字列を入力として受け取り、それをリストに変換するプログラム
```python
text = input("カンマ区切りの文字列を入力してください: ")
items = text.split(",")
items = [item.strip() for item in items]  # 空白を削除
print(f"リスト: {items}")
```

### 36. 文字列を入力として受け取り、その文字列に含まれるスペースをすべて削除するプログラム
```python
text = input("文字列を入力してください: ")
text_without_spaces = text.replace(" ", "")
print(f"スペース削除後: {text_without_spaces}")
```

### 37. 2つの文字列を入力として受け取り、一方がもう一方のアナグラム（文字の並べ替え）かどうかを判定するプログラム
```python
str1 = input("1つ目の文字列を入力してください: ").lower()
str2 = input("2つ目の文字列を入力してください: ").lower()

# 空白を削除し、ソートして比較
if sorted(str1.replace(" ", "")) == sorted(str2.replace(" ", "")):
    print("アナグラムです。")
else:
    print("アナグラムではありません。")
```

### 38. 文字列を入力として受け取り、その文字列の中の特定の文字をすべて別の文字に置き換えるプログラム
```python
text = input("文字列を入力してください: ")
char_to_replace = input("置換する文字を入力してください: ")
replacement_char = input("置換後の文字を入力してください: ")

new_text = text.replace(char_to_replace, replacement_char)
print(f"置換後: {new_text}")
```

### 39. 複数の文字列を含むリストを結合して一つの文字列にするプログラム
```python
strings = ["Hello", "World", "Python", "Programming"]
separator = input("区切り文字を入力してください: ")
joined_string = separator.join(strings)
print(f"結合後: {joined_string}")
```

### 40. URLを入力として受け取り、そのドメイン名を抽出するプログラム
```python
import re
url = input("URLを入力してください: ")
domain = re.search(r'https?://([^/]+)', url)
if domain:
    print(f"ドメイン名: {domain.group(1)}")
else:
    print("有効なURLではありません。")
```

## リスト・辞書操作編 (41-50)

### 41. 2つのリストを連結するプログラム
```python
list1 = [1, 2, 3, 4, 5]
list2 = [6, 7, 8, 9, 10]
combined_list = list1 + list2
print(f"連結後のリスト: {combined_list}")
```

### 42. リストの要素を昇順にソートするプログラム
```python
numbers = [5, 2, 8, 1, 9, 3, 7, 4, 6]
sorted_numbers = sorted(numbers)
print(f"ソート前: {numbers}")
print(f"ソート後: {sorted_numbers}")

# 元のリストを変更する場合
numbers.sort()
print(f"sort()後: {numbers}")
```

### 43. リストから重複要素を削除するプログラム
```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 5, 6]
unique_numbers = list(set(numbers))
print(f"重複削除後: {unique_numbers}")
```

### 44. 2つのリストからペアを作成するプログラム
```python
names = ["田中", "鈴木", "佐藤"]
ages = [25, 30, 22]
pairs = list(zip(names, ages))
print(f"ペア: {pairs}")

# 辞書に変換
person_dict = dict(zip(names, ages))
print(f"辞書: {person_dict}")
```

### 45. 辞書のキーと値を入れ替えるプログラム
```python
original_dict = {"apple": "りんご", "banana": "バナナ", "orange": "オレンジ"}
swapped_dict = {v: k for k, v in original_dict.items()}
print(f"元の辞書: {original_dict}")
print(f"入れ替え後: {swapped_dict}")
```

### 46. 2つの辞書をマージするプログラム
```python
dict1 = {"a": 1, "b": 2, "c": 3}
dict2 = {"d": 4, "e": 5, "f": 6}

# Python 3.9以降
merged_dict = dict1 | dict2

# Python 3.9未満
# merged_dict = {**dict1, **dict2}

print(f"マージ後: {merged_dict}")
```

### 47. リストの各要素の出現回数を数えて辞書として出力するプログラム
```python
items = ["apple", "banana", "apple", "orange", "banana", "apple"]
item_count = {}
for item in items:
    if item in item_count:
        item_count[item] += 1
    else:
        item_count[item] = 1

print(f"出現回数: {item_count}")

# collectionsモジュールを使用する方法
from collections import Counter
item_count2 = Counter(items)
print(f"Counterを使用: {dict(item_count2)}")
```

### 48. 辞書をキーでソートするプログラム
```python
my_dict = {"banana": 3, "apple": 1, "orange": 2, "grape": 4}
sorted_dict = dict(sorted(my_dict.items()))
print(f"ソート後: {sorted_dict}")
```

### 49. ネストしたリストを平坦化（フラット化）するプログラム
```python
nested_list = [[1, 2, 3], [4, 5], [6, 7, 8, 9]]
flat_list = [item for sublist in nested_list for item in sublist]
print(f"平坦化後: {flat_list}")
```

### 50. 複数の辞書を含むリストから、特定のキーの値に基づいてソートするプログラム
```python
people = [
    {"name": "田中", "age": 25},
    {"name": "鈴木", "age": 30},
    {"name": "佐藤", "age": 22}
]
sorted_people = sorted(people, key=lambda x: x["age"])
print(f"年齢でソート: {sorted_people}")
```

## 関数編 (51-60)

### 51. 2つの数値を引数に取り、その積を返す関数を作成してください。
```python
def multiply(a, b):
    return a * b

num1 = float(input("1つ目の数値を入力してください: "))
num2 = float(input("2つ目の数値を入力してください: "))
result = multiply(num1, num2)
print(f"{num1} × {num2} = {result}")
```

### 52. 文字列を引数に取り、その文字列が回文かどうかを判定する関数を作成してください。
```python
def is_palindrome(text):
    # 空白と大文字小文字を無視
    text = text.lower().replace(" ", "")
    return text == text[::-1]

text = input("文字列を入力してください: ")
if is_palindrome(text):
    print(f"「{text}」は回文です。")
else:
    print(f"「{text}」は回文ではありません。")
```

### 53. リストを引数に取り、その要素の合計を返す関数を作成してください。
```python
def sum_list(numbers):
    return sum(numbers)

# テスト用のリスト
numbers = [1, 2, 3, 4, 5]
total = sum_list(numbers)
print(f"合計: {total}")
```

### 54. 任意の数の引数を受け取り、それらの平均値を返す関数を作成してください。
```python
def average(*args):
    if not args:
        return 0
    return sum(args) / len(args)

avg1 = average(1, 2, 3, 4, 5)
print(f"平均値: {avg1}")

avg2 = average(10, 20, 30)
print(f"平均値: {avg2}")
```

### 55. 再帰を使用して、数値のフィボナッチ数を計算する関数を作成してください。
```python
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

n = int(input("数値を入力してください: "))
result = fibonacci(n)
print(f"フィボナッチ数({n}): {result}")
```

### 56. デフォルト引数を持つ関数を作成してください。
```python
def greet(name, greeting="こんにちは"):
    return f"{greeting}, {name}さん！"

print(greet("太郎"))
print(greet("花子", "おはよう"))
```

### 57. ラムダ関数を使用して、リストの各要素を2倍にするプログラムを作成してください。
```python
numbers = [1, 2, 3, 4, 5]
doubled = list(map(lambda x: x * 2, numbers))
print(f"元のリスト: {numbers}")
print(f"2倍にしたリスト: {doubled}")
```

### 58. map関数を使用して、リストの各要素を文字列に変換するプログラムを作成してください。
```python
numbers = [1, 2, 3, 4, 5]
strings = list(map(str, numbers))
print(f"元のリスト: {numbers}")
print(f"文字列に変換: {strings}")
```

### 59. filter関数を使用して、リストから偶数だけを抽出するプログラムを作成してください。
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(f"元のリスト: {numbers}")
print(f"偶数のみ: {even_numbers}")
```

### 60. reduce関数を使用して、リストの要素の積を計算するプログラムを作成してください。
```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y: x * y, numbers)
print(f"元のリスト: {numbers}")
print(f"要素の積: {product}")
```

## ファイル操作編 (61-70)

### 61. テキストファイルを作成し、何か文章を書き込むプログラムを作成してください。
```python
file_name = "sample.txt"
with open(file_name, "w", encoding="utf-8") as file:
    file.write("これはサンプルのテキストファイルです。\n")
    file.write("Pythonでファイル操作を学んでいます。")

print(f"{file_name}にテキストを書き込みました。")
```

### 62. テキストファイルを読み込み、その内容を表示するプログラムを作成してください。
```python
file_name = "sample.txt"
try:
    with open(file_name, "r", encoding="utf-8") as file:
        content = file.read()
        print(f"ファイルの内容:\n{content}")
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
```

### 63. テキストファイルの行数、単語数、文字数を数えるプログラムを作成してください。
```python
file_name = "sample.txt"
try:
    with open(file_name, "r", encoding="utf-8") as file:
        content = file.read()
        lines = content.split("\n")
        words = content.split()
        chars = len(content)
        
        print(f"行数: {len(lines)}")
        print(f"単語数: {len(words)}")
        print(f"文字数: {chars}")
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
```

### 64. CSVファイルを作成し、いくつかのデータを書き込むプログラムを作成してください。
```python
import csv

file_name = "data.csv"
data = [
    ["名前", "年齢", "都市"],
    ["田中", 25, "東京"],
    ["鈴木", 30, "大阪"],
    ["佐藤", 22, "名古屋"]
]

with open(file_name, "w", newline="", encoding="utf-8") as file:
    writer = csv.writer(file)
    writer.writerows(data)

print(f"{file_name}にデータを書き込みました。")
```

### 65. CSVファイルを読み込み、その内容を表示するプログラムを作成してください。
```python
import csv

file_name = "data.csv"
try:
    with open(file_name, "r", encoding="utf-8") as file:
        reader = csv.reader(file)
        for row in reader:
            print(row)
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
```

### 66. 2つのファイルを結合して新しいファイルを作成するプログラムを作成してください。
```python
file1 = "file1.txt"
file2 = "file2.txt"
output_file = "combined.txt"

# サンプルファイルを作成
with open(file1, "w", encoding="utf-8") as f:
    f.write("これは1つ目のファイルです。\n")

with open(file2, "w", encoding="utf-8") as f:
    f.write("これは2つ目のファイルです。\n")

# ファイルを結合
with open(output_file, "w", encoding="utf-8") as outfile:
    for filename in [file1, file2]:
        with open(filename, "r", encoding="utf-8") as infile:
            outfile.write(infile.read())

print(f"{file1}と{file2}を結合して{output_file}を作成しました。")
```

### 67. ファイル内の特定の文字列を検索し、その出現回数と行番号を表示するプログラムを作成してください。
```python
file_name = "sample.txt"
search_term = input("検索する文字列を入力してください: ")

try:
    with open(file_name, "r", encoding="utf-8") as file:
        lines = file.readlines()
        count = 0
        line_numbers = []
        
        for i, line in enumerate(lines, 1):
            if search_term in line:
                count += line.count(search_term)
                line_numbers.append(i)
        
        print(f"'{search_term}'の出現回数: {count}")
        print(f"出現行: {line_numbers}")
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
```

### 68. ディレクトリ内のすべてのファイルのリストを表示するプログラムを作成してください。
```python
import os

directory = input("ディレクトリのパスを入力してください: ")
if not directory:
    directory = "."  # カレントディレクトリ

try:
    files = os.listdir(directory)
    print(f"{directory}内のファイル:")
    for file in files:
        print(file)
except FileNotFoundError:
    print(f"{directory}が見つかりません。")
```

### 69. ファイルのコピーを作成するプログラムを作成してください。
```python
import shutil

source_file = input("コピー元ファイルのパスを入力してください: ")
destination_file = input("コピー先ファイルのパスを入力してください: ")

try:
    shutil.copy2(source_file, destination_file)
    print(f"{source_file}を{destination_file}にコピーしました。")
except FileNotFoundError:
    print("ファイルが見つかりません。")
except PermissionError:
    print("権限がありません。")
```

### 70. ファイル内の特定の文字列をすべて別の文字列に置き換えるプログラムを作成してください。
```python
file_name = "sample.txt"
search_string = input("置換する文字列を入力してください: ")
replace_string = input("置換後の文字列を入力してください: ")

try:
    # ファイルを読み込む
    with open(file_name, "r", encoding="utf-8") as file:
        content = file.read()
    
    # 文字列を置換
    modified_content = content.replace(search_string, replace_string)
    
    # 変更をファイルに書き込む
    with open(file_name, "w", encoding="utf-8") as file:
        file.write(modified_content)
    
    print(f"{file_name}内の'{search_string}'を'{replace_string}'に置き換えました。")
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
```

## モジュール・パッケージ編 (71-80)

### 71. mathモジュールを使用して、円の面積を計算するプログラムを作成してください。
```python
import math

radius = float(input("円の半径を入力してください: "))
area = math.pi * radius ** 2
print(f"半径{radius}の円の面積: {area:.2f}")
```

### 72. randomモジュールを使用して、1から100までのランダムな数値を10個生成するプログラムを作成してください。
```python
import random

random_numbers = [random.randint(1, 100) for _ in range(10)]
print(f"ランダムな数値: {random_numbers}")
```

### 73. datetimeモジュールを使用して、現在の日時を表示するプログラムを作成してください。
```python
import datetime

now = datetime.datetime.now()
print(f"現在の日時: {now}")
print(f"フォーマット済み: {now.strftime('%Y年%m月%d日 %H時%M分%S秒')}")
```

### 74. osモジュールを使用して、カレントディレクトリを表示するプログラムを作成してください。
```python
import os

current_dir = os.getcwd()
print(f"カレントディレクトリ: {current_dir}")
```

### 75. sysモジュールを使用して、コマンドライン引数を表示するプログラムを作成してください。
```python
import sys

print(f"コマンドライン引数: {sys.argv}")
print("引数の数:", len(sys.argv))
print("Pythonのバージョン:", sys.version)
```

### 76. timeモジュールを使用して、プログラムの実行時間を計測するプログラムを作成してください。
```python
import time

start_time = time.time()

# 何か時間のかかる処理
for i in range(1000000):
    pass

end_time = time.time()
execution_time = end_time - start_time
print(f"実行時間: {execution_time:.6f}秒")
```

### 77. collectionsモジュールのCounterクラスを使用して、リストの要素の出現回数を数えるプログラムを作成してください。
```python
from collections import Counter

words = ["apple", "banana", "apple", "orange", "banana", "apple", "grape"]
word_counts = Counter(words)

print(f"単語の出現回数:")
for word, count in word_counts.items():
    print(f"{word}: {count}回")

# 最も一般的な要素
most_common = word_counts.most_common(2)
print(f"最も一般的な2つの要素: {most_common}")
```

### 78. jsonモジュールを使用して、PythonオブジェクトをJSON形式で保存するプログラムを作成してください。
```python
import json

data = {
    "name": "田中太郎",
    "age": 30,
    "city": "東京",
    "hobbies": ["読書", "旅行", "プログラミング"]
}

file_name = "data.json"
with open(file_name, "w", encoding="utf-8") as file:
    json.dump(data, file, ensure_ascii=False, indent=4)

print(f"{file_name}にJSONデータを保存しました。")

# 読み込みテスト
with open(file_name, "r", encoding="utf-8") as file:
    loaded_data = json.load(file)

print(f"読み込んだデータ: {loaded_data}")
```

### 79. requestsモジュールを使用して、ウェブページの内容を取得するプログラムを作成してください。
```python
import requests

url = "https://www.example.com"
try:
    response = requests.get(url)
    print(f"ステータスコード: {response.status_code}")
    print(f"コンテンツタイプ: {response.headers['Content-Type']}")
    print(f"コンテンツの一部: {response.text[:200]}...")
except requests.exceptions.RequestException as e:
    print(f"エラー: {e}")
```

### 80. subprocessモジュールを使用して、シェルコマンドを実行するプログラムを作成してください。
```python
import subprocess

# 現在のディレクトリの内容を表示
try:
    result = subprocess.run(["dir" if os.name == "nt" else "ls", "-la"], 
                          capture_output=True, text=True, shell=True)
    print(f"コマンド出力:\n{result.stdout}")
    if result.stderr:
        print(f"エラー出力:\n{result.stderr}")
except Exception as e:
    print(f"エラー: {e}")
```

## エラー処理・クラス編 (81-90)

### 81. try-exceptを使用して、ゼロ除算エラーを処理するプログラムを作成してください。
```python
def divide(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        return "0で割ることはできません。"

numerator = float(input("分子を入力してください: "))
denominator = float(input("分母を入力してください: "))
print(f"計算結果: {divide(numerator, denominator)}")
```

### 82. try-except-elseを使用して、ファイルの読み込みを行うプログラムを作成してください。
```python
file_name = input("読み込むファイル名を入力してください: ")

try:
    with open(file_name, "r", encoding="utf-8") as file:
        content = file.read()
except FileNotFoundError:
    print(f"{file_name}が見つかりません。")
except PermissionError:
    print(f"{file_name}を読み込む権限がありません。")
else:
    print(f"ファイルの内容:\n{content}")
    print(f"{len(content)}文字読み込みました。")
```

### 83. try-except-finally構文を使用するプログラムを作成してください。
```python
def process_file(file_name):
    file = None
    try:
        file = open(file_name, "r", encoding="utf-8")
        content = file.read()
        return content
    except FileNotFoundError:
        print(f"{file_name}が見つかりません。")
        return None
    finally:
        if file is not None:
            file.close()
            print("ファイルを閉じました。")

content = process_file("sample.txt")
if content:
    print(f"ファイルの内容: {content[:50]}...")
```

### 84. カスタム例外クラスを定義するプログラムを作成してください。
```python
class NegativeValueError(Exception):
    """負の値が入力されたときに発生する例外"""
    def __init__(self, value, message="負の値は許可されていません"):
        self.value = value
        self.message = message
        super().__init__(self.message)

def calculate_square_root(n):
    if n < 0:
        raise NegativeValueError(n, f"{n}の平方根は実数では計算できません")
    return n ** 0.5

try:
    number = float(input("平方根を計算する数値を入力してください: "))
    result = calculate_square_root(number)
    print(f"{number}の平方根: {result}")
except NegativeValueError as e:
    print(f"エラー: {e.message}")
```

### 85. 単純な計算機クラスを作成してください。
```python
class Calculator:
    def add(self, a, b):
        return a + b
    
    def subtract(self, a, b):
        return a - b
    
    def multiply(self, a, b):
        return a * b
    
    def divide(self, a, b):
        if b == 0:
            raise ValueError("0で割ることはできません")
        return a / b

calc = Calculator()
print(f"10 + 5 = {calc.add(10, 5)}")
print(f"10 - 5 = {calc.subtract(10, 5)}")
print(f"10 * 5 = {calc.multiply(10, 5)}")
print(f"10 / 5 = {calc.divide(10, 5)}")
```

### 86. 銀行口座クラスを作成してください。
```python
class BankAccount:
    def __init__(self, account_number, owner_name, balance=0):
        self.account_number = account_number
        self.owner_name = owner_name
        self.balance = balance
    
    def deposit(self, amount):
        if amount <= 0:
            raise ValueError("預金額は正の数である必要があります")
        self.balance += amount
        return f"{amount}円を預けました。残高: {self.balance}円"
    
    def withdraw(self, amount):
        if amount <= 0:
            raise ValueError("引き出し額は正の数である必要があります")
        if amount > self.balance:
            raise ValueError(f"残高不足です。現在の残高: {self.balance}円")
        self.balance -= amount
        return f"{amount}円を引き出しました。残高: {self.balance}円"
    
    def get_balance(self):
        return f"口座残高: {self.balance}円"

# テスト
account = BankAccount("123456", "田中太郎", 1000)
print(account.get_balance())
print(account.deposit(500))
print(account.withdraw(200))
print(account.get_balance())
```

### 87. 継承を使用して、動物クラスとその派生クラスを作成してください。
```python
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species
    
    def make_sound(self):
        return "Some generic animal sound"
    
    def info(self):
        return f"{self.name}は{self.species}です。"

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name, "犬")
        self.breed = breed
    
    def make_sound(self):
        return "ワンワン！"
    
    def info(self):
        return f"{super().info()} 犬種は{self.breed}です。"

class Cat(Animal):
    def __init__(self, name, color):
        super().__init__(name, "猫")
        self.color = color
    
    def make_sound(self):
        return "ニャー！"
    
    def info(self):
        return f"{super().info()} 毛色は{self.color}です。"

# テスト
dog = Dog("ポチ", "柴犬")
cat = Cat("タマ", "三毛")

print(dog.info())
print(f"{dog.name}の鳴き声: {dog.make_sound()}")

print(cat.info())
print(f"{cat.name}の鳴き声: {cat.make_sound()}")
```

### 88. プロパティデコレータを使用するクラスを作成してください。
```python
class Temperature:
    def __init__(self, celsius=0):
        self._celsius = celsius
    
    @property
    def celsius(self):
        return self._celsius
    
    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("絶対零度より低い温度は存在しません。")
        self._celsius = value
    
    @property
    def fahrenheit(self):
        return self._celsius * 9/5 + 32
    
    @fahrenheit.setter
    def fahrenheit(self, value):
        self.celsius = (value - 32) * 5/9

# テスト
temp = Temperature(25)
print(f"摂氏: {temp.celsius}°C")
print(f"華氏: {temp.fahrenheit}°F")

temp.celsius = 30
print(f"摂氏: {temp.celsius}°C")
print(f"華氏: {temp.fahrenheit}°F")

temp.fahrenheit = 68
print(f"摂氏: {temp.celsius}°C")
print(f"華氏: {temp.fahrenheit}°F")
```

### 89. スタティックメソッドとクラスメソッドを持つクラスを作成してください。
```python
class MathUtils:
    PI = 3.14159
    
    def __init__(self, value):
        self.value = value
    
    def square(self):
        return self.value ** 2
    
    @classmethod
    def circle_area(cls, radius):
        return cls.PI * radius ** 2
    
    @staticmethod
    def is_prime(n):
        if n <= 1:
            return False
        if n <= 3:
            return True
        if n % 2 == 0 or n % 3 == 0:
            return False
        i = 5
        while i * i <= n:
            if n % i == 0 or n % (i + 2) == 0:
                return False
            i += 6
        return True

# テスト
math = MathUtils(4)
print(f"4の2乗: {math.square()}")
print(f"半径5の円の面積: {MathUtils.circle_area(5)}")
print(f"17は素数か: {MathUtils.is_prime(17)}")
print(f"20は素数か: {MathUtils.is_prime(20)}")
```

### 90. オブジェクトの文字列表現をカスタマイズするメソッド（__str__、__repr__）を実装するクラスを作成してください。
```python
class Person:
    def __init__(self, name, age, job):
        self.name = name
        self.age = age
        self.job = job
    
    def __str__(self):
        return f"{self.name}（{self.age}歳・{self.job}）"
    
    def __repr__(self):
        return f"Person(name='{self.name}', age={self.age}, job='{self.job}')"

# テスト
person = Person("田中太郎", 30, "エンジニア")
print(str(person))  # __str__が呼ばれる
print(repr(person))  # __repr__が呼ばれる

# リストに入れて表示
people = [
    Person("田中太郎", 30, "エンジニア"),
    Person("鈴木花子", 25, "デザイナー")
]
print(people)  # __repr__が呼ばれる
```

## 応用編 (91-100)

### 91. リストの内包表記を使用して、1から100までの数値のうち、3の倍数のリストを作成するプログラムを作成してください。
```python
multiples_of_three = [i for i in range(1, 101) if i % 3 == 0]
print(f"3の倍数: {multiples_of_three}")
print(f"個数: {len(multiples_of_three)}")
```

### 92. 辞書の内包表記を使用して、1から10までの数値とその二乗のペアを持つ辞書を作成するプログラムを作成してください。
```python
squares = {i: i**2 for i in range(1, 11)}
print(f"数値とその二乗: {squares}")
```

### 93. ジェネレータ関数を使用して、フィボナッチ数列を生成するプログラムを作成してください。
```python
def fibonacci_generator(n):
    a, b = 0, 1
    count = 0
    while count < n:
        yield a
        a, b = b, a + b
        count += 1

# 最初の10個のフィボナッチ数を生成
n = 10
fib_sequence = list(fibonacci_generator(n))
print(f"最初の{n}個のフィボナッチ数: {fib_sequence}")

# ジェネレータを使って一つずつ表示
print("\n一つずつ生成:")
for i, fib in enumerate(fibonacci_generator(n)):
    print(f"フィボナッチ数 {i}: {fib}")
```

### 94. デコレータを作成して、関数の実行時間を計測するプログラムを作成してください。
```python
import time
import functools

def timing_decorator(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"{func.__name__}の実行時間: {end_time - start_time:.6f}秒")
        return result
    return wrapper

@timing_decorator
def slow_function():
    """時間のかかる関数の例"""
    time.sleep(1)  # 1秒待機
    return "処理完了"

@timing_decorator
def calculate_sum(n):
    """1からnまでの合計を計算"""
    return sum(range(1, n + 1))

# テスト
result1 = slow_function()
print(result1)

result2 = calculate_sum(1000000)
print(f"合計: {result2}")
```

### 95. コンテキストマネージャを使用して、ファイルを自動的に閉じるプログラムを作成してください。
```python
class FileManager:
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode
        self.file = None
    
    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file
    
    def __exit__(self, exc_type, exc_val, exc_tb):
        if self.file:
            self.file.close()
            print(f"{self.filename}を閉じました。")
        if exc_type:
            print(f"例外が発生しました: {exc_val}")
        # 例外を伝播させない場合はTrueを返す
        return False

# テスト - ファイルが存在しなくても例外を捕捉して適切に処理
try:
    with FileManager("example.txt", "w") as f:
        f.write("これはコンテキストマネージャのテストです。")
        print("ファイルに書き込みました。")
    
    with FileManager("example.txt", "r") as f:
        content = f.read()
        print(f"ファイルの内容: {content}")
except Exception as e:
    print(f"外部のtry-exceptで捕捉した例外: {e}")
```

### 96. イテレータプロトコルを実装するクラスを作成してください。
```python
class Countdown:
    def __init__(self, start):
        self.start = start
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.start <= 0:
            raise StopIteration
        self.start -= 1
        return self.start + 1

# テスト
print("カウントダウン:")
for num in Countdown(5):
    print(num)

# リストに変換
countdown_list = list(Countdown(10))
print(f"カウントダウンリスト: {countdown_list}")
```

### 97. マルチスレッドを使用して、複数のタスクを並行して実行するプログラムを作成してください。
```python
import threading
import time

def task(name, delay):
    print(f"{name} タスク開始")
    time.sleep(delay)
    print(f"{name} タスク完了 ({delay}秒後)")

# スレッドを作成
thread1 = threading.Thread(target=task, args=("Thread-1", 2))
thread2 = threading.Thread(target=task, args=("Thread-2", 4))
thread3 = threading.Thread(target=task, args=("Thread-3", 1))

# 開始時間
start_time = time.time()

# スレッドを開始
thread1.start()
thread2.start()
thread3.start()

# メインスレッドはすべてのスレッドが終了するのを待つ
thread1.join()
thread2.join()
thread3.join()

# 終了時間
end_time = time.time()

print(f"すべてのタスクが完了しました。")
print(f"合計実行時間: {end_time - start_time:.2f}秒")
```

### 98. socketモジュールを使用して、簡単なクライアント・サーバープログラムを作成してください。
```python
import socket
import threading
import time

# サーバー関数
def start_server():
    server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    server_socket.bind(('localhost', 12345))
    server_socket.listen(1)
    print("サーバーが起動しました。クライアントの接続を待機中...")
    
    conn, addr = server_socket.accept()
    print(f"クライアント{addr}が接続しました。")
    
    while True:
        data = conn.recv(1024).decode('utf-8')
        if not data:
            break
        print(f"クライアントからのメッセージ: {data}")
        response = f"サーバーからの応答: {data}を受信しました"
        conn.send(response.encode('utf-8'))
    
    conn.close()
    server_socket.close()
    print("サーバーを終了しました。")

# クライアント関数
def start_client():
    time.sleep(1)  # サーバーが起動するのを待つ
    client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    client_socket.connect(('localhost', 12345))
    print("サーバーに接続しました。")
    
    for i in range(3):
        message = f"メッセージ {i+1}"
        client_socket.send(message.encode('utf-8'))
        print(f"サーバーに送信: {message}")
        
        response = client_socket.recv(1024).decode('utf-8')
        print(f"サーバーからの応答: {response}")
        time.sleep(1)
    
    client_socket.close()
    print("クライアントを終了しました。")

# スレッドを使ってサーバーとクライアントを同時に実行
server_thread = threading.Thread(target=start_server)
client_thread = threading.Thread(target=start_client)

server_thread.start()
client_thread.start()

server_thread.join()
client_thread.join()
```

### 99. numpyモジュールを使用して、行列の演算を行うプログラムを作成してください。
```python
import numpy as np

# 行列の作成
matrix_a = np.array([[1, 2, 3], [4, 5, 6]])
matrix_b = np.array([[7, 8], [9, 10], [11, 12]])

print("行列 A:")
print(matrix_a)
print(f"形状: {matrix_a.shape}")

print("\n行列 B:")
print(matrix_b)
print(f"形状: {matrix_b.shape}")

# 行列の積
matrix_c = np.dot(matrix_a, matrix_b)
print("\n行列の積 A × B:")
print(matrix_c)
print(f"形状: {matrix_c.shape}")

# 行列の転置
matrix_a_t = matrix_a.T
print("\n行列 A の転置:")
print(matrix_a_t)
print(f"形状: {matrix_a_t.shape}")

# 行列の固有値と固有ベクトル
square_matrix = np.array([[4, 2], [2, 3]])
eigenvalues, eigenvectors = np.linalg.eig(square_matrix)
print("\n正方行列:")
print(square_matrix)
print("\n固有値:")
print(eigenvalues)
print("\n固有ベクトル:")
print(eigenvectors)

# 行列式
determinant = np.linalg.det(square_matrix)
print(f"\n行列式: {determinant}")

# 逆行列
inverse_matrix = np.linalg.inv(square_matrix)
print("\n逆行列:")
print(inverse_matrix)

# 検証: 元の行列と逆行列の積は単位行列になる
identity = np.dot(square_matrix, inverse_matrix)
print("\n元の行列と逆行列の積:")
print(np.round(identity, 10))  # 浮動小数点の誤差を丸める
```

### 100. pandasモジュールを使用して、CSVファイルを読み込み、データの基本的な分析を行うプログラムを作成してください。
```python
import pandas as pd
import matplotlib.pyplot as plt

# サンプルCSVファイルを作成
sample_data = """日付,売上,経費,利益
2023-01-01,10000,5000,5000
2023-02-01,12000,6000,6000
2023-03-01,15000,7000,8000
2023-04-01,11000,6500,4500
2023-05-01,13000,7500,5500
2023-06-01,16000,8000,8000
2023-07-01,14000,7000,7000
2023-08-01,17000,8500,8500
2023-09-01,13500,7200,6300
2023-10-01,18000,9000,9000
2023-11-01,19000,9500,9500
2023-12-01,21000,10000,11000"""

with open("sales_data.csv", "w", encoding="utf-8") as f:
    f.write(sample_data)

# CSVファイルを読み込む
df = pd.read_csv("sales_data.csv")

# データの概要を確認
print("データの概要:")
print(df.head())
print("\nデータの情報:")
print(df.info())
print("\n基本統計量:")
print(df.describe())

# 売上の合計と平均
total_sales = df["売上"].sum()
average_sales = df["売上"].mean()
print(f"\n総売上: {total_sales}円")
print(f"平均月間売上: {average_sales}円")

# 最も利益が高かった月と最も低かった月
max_profit_month = df.loc[df["利益"].idxmax(), "日付"]
min_profit_month = df.loc[df["利益"].idxmin(), "日付"]
print(f"最も利益が高かった月: {max_profit_month}, 利益: {df['利益'].max()}円")
print(f"最も利益が低かった月: {min_profit_month}, 利益: {df['利益'].min()}円")

# 月ごとの売上と経費の割合
df["経費率"] = df["経費"] / df["売上"] * 100
print("\n月ごとの経費率:")
print(df[["日付", "経費率"]].to_string(index=False))

# 売上の四半期ごとの集計
df["四半期"] = pd.PeriodIndex(pd.to_datetime(df["日付"]), freq="Q")
quarterly_sales = df.groupby("四半期")["売上"].sum()
print("\n四半期ごとの売上:")
print(quarterly_sales)

# グラフ作成（実際の実行環境では表示されます）
plt.figure(figsize=(12, 6))
plt.plot(df["日付"], df["売上"], marker="o", label="売上")
plt.plot(df["日付"], df["経費"], marker="s", label="経費")
plt.plot(df["日付"], df["利益"], marker="^", label="利益")
plt.title("月別の売上・経費・利益の推移")
plt.xlabel("月")
plt.ylabel("金額（円）")
plt.legend()
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()
plt.savefig("sales_chart.png")  # グラフを画像ファイルとして保存

print("\n分析が完了しました。グラフを「sales_chart.png」に保存しました。")
```