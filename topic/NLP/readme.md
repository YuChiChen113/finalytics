# NLP


## Reference


1. 20240603 present
paper


2. Topic: returns prediction using sentiment analysis.


## Qauntinar explorations


### 1. DEDA_class_SoSe2023_Covid-19_Financial_News_Sentiment_Analysis

Summary: useless,.. 



ABSA.

## Teng's guess/dream

Aims
1. returns prediction ok
2. NLP and LLM: ? 
3. text: ? 
x: existing features



1: y = f( x, Standard polarity) 
2: y = f( x, **Our proposed polarity**) 



## 不卒之處

1. How to calcualte Polarity?
2. What is the role in LLM?



Quantinar 


model 1: y= f(x)
model 2: y= f(x, sentiment analysis)

LLM selected features


## 1. Leveraging hierarchical language models for aspect-based sentiment analysis on financial data
  * 更多層 hierarchical
  * 針對不同的產業選擇不同的 aspect
  * 測試其他 few-shot learning 的結果
  * A Hybrid Approach To Aspect Based Sentiment Analysis Using Transfer Learning，利用他的方法強化 ABSA 效果(？
  * LM用較新的
## 2. Time LLM
  * 將 timellm 用於 stock return prediction
  * 更改或強化 patch reprogramming 的方式
    * 利用像 stockformer STL的分割方式
    * 生成更好的 prompt
    * vs. TimeGPT
      * TimeGPT retrain model 需要大量的時間算力以及數據
      * TimeGPT 只能使用在單一領域
      * 方法截然不同但結果相似
## 3. Stockformer
  * 將 Stockformer 模型分為三個子模塊，分別處理趨勢、季節性和殘差組件
    * 使用多頭自注意力機制，使模型能夠關注不同特徵對這三個組件的不同影響
  * 多模態特徵：利用文本分析強化 encoder 的解釋性
    * 將文本數據轉換為數值特徵，並使用多模態學習技術，整合文本特徵與時間序列數據
    * 為每個子模塊輸入不同的特徵組合。例如，趨勢模塊可以更多地關注長期新聞和財報數據，而季節性模塊則可以重點關注周期性事件和數據
  * 在 decoder 後面加入可解釋的方法
  * 強化學習優化
    * 解釋部分可利用 [self reflection](https://arxiv.org/abs/2303.11366) 優化 (每次預測後，將預測結果與實際結果進行比較，生成反思回饋)
    * 使用PPO算法根據反思回饋更新模型參數，使其能夠更準確地預測趨勢、季節性和殘差組
