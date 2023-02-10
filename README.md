# 3-Way Scientific Calculator
A scientific calculator built through three different algorithms.

## Prerequisites
1. **Tools and Packages**
	* python standard library (math, time, random, argparse)
	* numpy
	* pygame

2.  **Environments**
	* python 3.8+ (windows.macOS.Linux均可，須有對應bash檔案）



  
## Execution

1. **Scientific Calculator User Interface** ```python3 ./GUI.py```
    *   Click buttons on screen to add operands or numbers to your input.  
    *   Trigonometry functions are default to take radians as input
    *   Precision was set to three digits behind the decimal point
    *   See ```Amendable Variables``` for more details

2. **Scientific Calculator Algorithms** ```python3 ./parse_tree.py```, ```python3 ./dp.py```, ```python3 ./shunting_yard.py```
	*	Each uses algorithms of ***Parse Tree, Parse Tree + Recursion, and Shunting Yard*** respectively, see report ```技術報告.pdf``` for more details 

3. **Test data generation** ```python3 ./exp_generator.py```
	*	Generates test data of variety length and complexity: ```input.txt```

4. **Bash Testing**
	* for Windows
		* correctness: ```bash evaluation_win.sh```
		* time: ```bash time_evaluation_win.sh```
	* for MacOs/Ubuntu
		* correctness: ```bash evaluation_macOs.sh```
		* time: ```bash time_evaluation_macOs.sh```

## Amendable Variables

(```python3 ./parse_tree.py```, ```python3 ./dp.py```, ```python3 ./shunting_yard.py```)
 
*	Input and output filenames: go to  ```if__name__ == 'main'``` and change variable ```default``` 
	```python 
	parser.add_argument("--input", type=str,default='./correctness/correct_1.txt',help="Input file root")
	parser.add_argument("--output", type=str, default='./ouput_1.txt', help="Output file root")
	```
*	Amend angle units: go to ```class Calculator```,```__init__``` and change ```self.angle```； ```True``` for degrees, and ```False``` for radians
	```python
	class Calculator
		def __init__(self):
			self.angle = True
			self.rnd_to = 3
	```

*	Amend output perciion: go to ```class Calculator```,```__init__``` set ```self.rnd_to```, the default value is 3




# 工程計算機
此專案以三種不同的演算法建置工程計算機: ***Parse Tree, Parse Tree + Recursion, Shunting Yard***

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


