<!--     範例 App_52  Markdown         -->

###  
<!--                 
# \[{  \color{Fuchsia}精\;銳\; \color{Purple}矩\;陣\;  \color{Red}計\;算\; \color{Green} 求\;解\;器  }\] 
-->  
![](Images/11-10-01.png) 


<!--         
#### \[{  \color{Fuchsia} 【 \color{Green}  Sharp \; Matrix \; Solver \;  \color{Brown} \iff  \;  \color{Red} S\;M\;S】 }\]  
-->  
![](Images/11-10-02.png)  

---

<!--   
## \[{ \color{Fuchsia} Time-Frequency-Signal \;(Response) \quad Solution  }\] 
-->
![](Images/11-30-01.png)  

<!--     ##### \[ using \]   -->
![](Images/11-30-07.png)
<!--    ##### $$using$$  -->  

<!--   
## \[  \color{Red} Precisely \; Numerical \; Value \; Computations  \]  
-->  
![](Images/11-30-02.png)  

<!--     ##### \[ with \]   -->  
![](Images/11-30-08.png)
<!--     ##### $$with$$   -->  

<!--   
## \[{ \color{Green} Real \; \color{Red} And \; \color{magenta} Complex \quad \; \color{Brown} Matrix \;\; Transform  }\] 
-->
![](Images/11-30-03.png)  

<!--         ##### \[ Part \; 1 \]    -->  
<!--    ![](Images/11-30-09.png)     -->  
<!--    ##### $$Part \quad 5$$  -->  

####

---  

# $$時\quad頻\quad數\quad值\quad計\quad算$$   

### $$Precisely \quad Time-Frequency \quad Numerical \quad Computations$$  

<!--  

# $$本實例程式碼\quad請參見本儲存庫$$ 

## $$已知實例如下 ：$$

$$y(t) = 
\begin{Bmatrix} 
2 \times t \\\\ 
\cos(10 \times t^2 + 100 \times t) \\\\  
\cos(60 \times t) \\\\ 
\cos(40 \times t) \\\\ 
\cos(t^2 + 20 \times t) \\\\ 
\cos(0.5 \times t^2 + 5 \times t) \\\\ 
1.0 
\end{Bmatrix}
$$ 

### $$條 \quad 件 \quad ： \quad t \geq 0 \quad 且 \quad t \leq \quad 2 \times \pi$$  

-->

##  

##  參考以下的網址 ：     

####  https://www.github.com/fastlib/fCWT  

#### https://www.nature.com/articles/s43588-021-00183-z  


#
# $$個\quad人\quad的\quad見\quad解：$$

### ( 1 ) .... ***有關儲存庫App_50和App_51是參考上述網站中的實例，實際撰寫CSharp程式碼，求得響應值【y】，並繪製時間與響應訊號圖。*** 

### ( 2 ) .... ***有關儲存庫App_48和App_49是已知實際的系統存在，也就是由齊次微分方程式，建構系統模型矩陣【A】，再求得特徵值矩陣【D】和特徵向量矩陣【Q】，進而求得系統頻率。如果已知系統的初始值或是邊界值，則可求得系統的響應訊號【y】，參見儲存庫App_6J和App_6M。***

### ( 3 ) .... ***比較( 1 )和( 2 )的合理性，( 1 )是頻率已知且是時間的變數，雖然是Nostationary system，但較不合理，因爲我們不太可能知道系統的頻率。( 2 )是由齊次微分方程式，求取實數系統矩陣【A】比較合理，尤其系統是可見的實體，譬如橋梁、房屋結構、機械系統等等，其空間維度(space dimension)有m個自由度(degree of freedom)和r個階數(Order)，故系統【A】為( m X r ) X ( m X r )的矩陣，由精銳矩陣計算求解器，可求得特徵值矩陣(D)和特徵向量矩陣(Q)，再由初始值或是邊界值，進而求得輸出振幅響應訊號【y】，參見App_48和App_49儲存庫中的C#程式碼。***  

### ( 4 ) .... ***( 1 )比較不合理的地方是，輸出的訊號是離散式數值，並不是時間的函數f(t)，故無法使用Fourier Transform【FT】、Short Time Fourier Transform【STFT】、Wavelet Transform【WT】、甚至 Hilbert-Huang Trasform【HHT】。其中HHT是使用 Empirical Mode Decomposition(EMD)、Emsemble Empirical Mode Decomposition(EEMD) 等模態分解的方法等等，這些都可能是問題？甚至量測的數據也可能有問題？因爲系統是多個節點，每一個節點是多個狀態(state)，譬如變位、速度、加速度、甚至三階以上的微分數據等等不同的狀態，故【不要太相信量測的數據是完全正確無誤】。***  

### ( 5 ) .... ***( 2 )是使用 Forward Problem 的求解方式，即 Wikipedia 所稱的 State-Space Representation，可得到精確的結果，而 Inverse Problem 的求解方式，即 ( 1 ) 的求解方式可能無法精確求取，故建議由 Inverse Problem 求得的結果，再 Feedback 到 Forward Problem 中，並修正系統矩陣【A】，反複 Forward 和 Imverse Problem 運算，最後的目標是精確求得【數學系統模型 A】。***

### ( 6 ) .... ***本人是初學者，所知有限，以上僅是個人的認知，尚待學者專家指正。***


###  

---  

#

![](Images/name_card.png)  

##
##
