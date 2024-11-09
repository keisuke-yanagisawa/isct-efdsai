# 補習資料 Supplementary Materials

東京科学大学 大学院全学科目「基盤データサイエンス演習」および「基盤人工知能演習」の授業内容に関わる補習資料です。

This is supplementary material related to the course content of "Exercises in Fundamental of Data Science" and "Exercises in Fundamental of Artificial Intelligence" at Institute of Science Tokyo.

この補習資料は、otter graderによる自動添削システムが設定されています。

This supplementary material is equipped with an automatic grading system using Otter Grader.

## 補習資料の利用方法

### Google Colaboratory への持ち込み

Google Colaboratory にて、GitHub リポジトリの URL を指定することで、補習資料を利用することができます。

The supplementary materials can be used by specifying the URL of the GitHub repository in Google Colaboratory.

![upload](https://i.imgur.com/eCN8vZR.png)

### otter graderによる自動添削

Otter graderとは、自動採点システムの1つであり、Jupyter Notebookを使った課題について、ルールベースでの採点を行うことが出来るものです（なお、「基盤データサイエンス演習」「基盤人工知能演習」の実際の採点でも多数のテストケースとともに活用しています）。

Otter Grader is an automatic grading system that can perform rule-based grading for assignments using Jupyter Notebook. It is extensively used with numerous test cases in the actual grading of "Exercises in Fundamental of Data Science" and "Exercises in Fundamental of Artificial Intelligence." 

このotter graderは、自動採点機能のほかに、受講生が自主学習できるように、リアルタイムで解答の正誤を確認できる機能も提供しています。

In addition to automatic grading, Otter Grader provides a feature that allows students to check the correctness of their answers in real-time for self-study purposes.

この資料では、例えば、

In this material, for example,

```python
import numpy as np
import numpy.typing as npt

def normalize_vector(v: npt.NDArray[np.float64]) -> npt.NDArray[np.float64]:
  ... 
```

```python
grader.check("Exercise 1-1")
```

のように、問題の直後に `grader.check()` という関数を実行するコードセルが存在します。このコードセルを実行することで、直前のコードセルの回答が全自動で評価され、正誤が表示されます。

There is a code cell that executes the function `grader.check()` right after the problem. By running this code cell, your answer in the previous code cell will be automatically evaluated, and the correctness will be displayed.

例えば、先ほど記述したように、 関数の中身を `...` のままにして `grader.check()` を行った場合は以下のような結果が得られます（途中を全て省略しています）。

For example, if you leave the function body as `...` as shown above and run `grader.check()`, you will get the following result (omitting the middle parts):

```
Exercise 1-1 results:

Exercise 1-1 - 1 message: 返り値がNumPy配列になっていません。 / The return value is not a NumPy array.

Exercise 1-1 - 1 result:
    ❌ Test case failed

    ...

Exercise 1-1 - 2 message: 出力されたベクトルが単位ベクトルになっていません。 / The output vector is not a unit vector.

Exercise 1-1 - 2 result:
    ❌ Test case failed

    ...

Exercise 1-1 - 3 message: 出力されたベクトルが単位ベクトルになっていません。 / The output vector is not a unit vector.

Exercise 1-1 - 3 result:
    ❌ Test case failed

    ...
```

このように、問題の対象となっている関数 `normalize_vector()` の動作を自動で確認し、動作が想定されていない点について、メッセージが表示されるようになっています。

As you can see, it automatically checks the behavior of the function `normalize_vector()` and displays messages where the behavior is not as expected.

また、適切にプログラムを記述した上で同じように `grader.check()` を行った場合は、以下のような結果が得られます。

If you write the program correctly and run `grader.check()` in the same way, you will get the following result:

```
Exercise 1-1 passed! 🌈
```

このような表示になれば、この課題については正答したということを意味しています。

This message indicates that you have correctly solved the exercise.