# calculator
Building a calculator with three approaches. Data Structure final project
# 工程計算機

* github webpage: https://github.com/oscar-shih/Final_Project
* **頁末有技術報告未說明清楚的補充!**

## 安裝環境及使用套件
1. **Tools and Packages**
	* python standard library (math, time, random, argparse)
	* numpy
	* pygame

2.  **執行環境**
	* python 3.8以上 (windows.macOS.Linux均可，須有對應bash檔案）



  
## 程式檔案與執行

1. **計算機界面** ```python3 ./GUI.py```
	*	進入GUI計算機頁面，操作與一般計算機相同，使用滑鼠點按即可
	*	程式預設: 三角函數輸入單位為度數、精準度為小數點後第三位，可調整```python3. /shunt_yard.py``` 更改

2. **計算機演算法** ```python3 ./parse_tree.py```, ```python3 ./dp.py```, ```python3 ./shunting_yard.py```
	*	分別對應 Parse Tree, Parse Tree + Recursion, Shunting Yard 演算法，詳情見技術報告說明 

3. **測資生成** ```python3 ./exp_generator.py```
	*	產生長度、複雜度相異的input.txt

4. **bash 測試**
	* for Windows
		* correctness: ```bash evaluation_win.sh```
		* time: ```bash time_evaluation_win.sh```
	* for MacOs/Ubuntu
		* correctness: ```bash evaluation_macOs.sh```
		* time: ```bash time_evaluation_macOs.sh```

## 計算機演算法參數調整

(```python3 ./parse_tree.py```, ```python3 ./dp.py```, ```python3 ./shunting_yard.py```)
 
*	調整輸入輸出檔案名稱: 至 ```if__name__ == 'main'``` 更改 ```default``` 參數
	```python 
	parser.add_argument("--input", type=str,default='./correctness/correct_1.txt',help="Input file root")
	parser.add_argument("--output", type=str, default='./ouput_1.txt', help="Output file root")
	```
*	調整輸入角度: 至 ```class Calculator```,```__init__``` 調整 ```self.angle```； ```True``` 為度數(預設)、```False``` 為弧度 (限三角函數)
	```python
	class Calculator
		def __init__(self):
			self.angle = True
			self.rnd_to = 3
	```

*	調整輸出精準度: 至 ```class Calculator```,```__init__``` 調整 ```self.rnd_to```，預設值為 3


