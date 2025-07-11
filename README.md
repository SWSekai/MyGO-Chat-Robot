# MyGO-Chat-Robot

## 基本介紹
本專案採用了進階版的 RAG（Retrieval-Augmented Generation）架構，並結合二階段思考機制（Two-Stage Thinking）與多模態輸出（Multimodal Output）技術，主要結合以下模型與工具：
* LLM（大型語言模型）：用於意圖轉譯與上下文生成。
* 向量資料庫（Vector DB）：使用如 Faiss 或 ChromaDB 儲存經嵌入的圖片描述及元資料，支援高效率檢索。
* Gradio：用於建構互動式使用者介面，實現圖片回覆呈現。
* CLIP 模型：用於計算語意相似度，支援文字與圖片間檢索橋接。

本模型設計的創新之處在於突破文字生成限制，直接輸出圖片作為回答，並強化使用者意圖的理解與情境轉譯能力，提升互動真實性與文化貼合度。

## 目標
本專案的核心目標在於打造一個：「能以圖片回覆問題，並具備對特定文化圈（如 MyGO!!!!!）語境高度理解能力的智能互動機器人」。
具體來說，目標如下：
1.	打破 RAG 回覆僅限文字的限制，實現以圖片作為主要回覆形式。
2.	提升模型的語境理解能力，特別針對 MyGO!!!!! 的詞彙、梗、語氣與情緒進行專屬調校。
3.	強化提示工程與意圖推理能力，透過二階段思考流程將模糊問題精煉為可檢索指令。
4.	改善互動體驗，透過 Gradio 介面讓使用者能夠便捷提問並即時獲得圖片式回覆。

## 流程
1.	精煉提示與語境轉譯（第一階段）
2.	向量資料庫搜尋與圖片配對（第二階段）
3.	生成圖片結果與回覆