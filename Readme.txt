Windows 建置運行本地大模型步驟紀錄(Windows+LMStudio+qwen3.5)

資料來源: https://www.youtube.com/watch?v=jn7FzlTCyDw
https://www.dhzyw.com/archives/7940.html

01.下載LM Studio(https://lmstudio.ai/download)

02.設定LM 語系:
	點擊左側最下面的齒輪圖示
	點擊彈出視窗左側的General
	點擊彈出視窗右側的User Interface的下拉式選單
	
03.下載大模型	
	點擊左側最下面的齒輪圖示往上署第二個圖
	在搜尋框 尋找『qwen3.5-9b』『DeepSeek-R1-Distill-Qwen-7B』
	搜尋後 在搜尋框下方點擊對應列表
	在搜尋列表右側 除了看到對應介紹外 還有包含對應的下載按鈕
	
04.啟動可讓外部呼叫的服務功能 09:04
	點擊左側由上下數第二個圖式
	點擊右側『Server Setting』按鈕
	再彈出視窗中將『在本地網路上供應』變成啟用 再隨意點選空白處 關閉彈出視窗
	點擊Server Setting 按鈕 左側的 開啟服務
	最後點擊該列的『Load Model』按鈕
		刪除再LOCAL仔入的選項
		點選新加載 並在最右側上方點選『Load』頁籤 該頁籤內的『上下文長度』改為『16873』
		最後 在『Load』頁籤最下方點擊『重新載入以應用變更』
	複製『Load Model』按鈕 左側網址: http://192.168.56.1:1234
	在主區的『支持的端點』區中選擇 『OpenAI-compatible』頁籤 就可以取得GET正確網址:http://192.168.56.1:1234/v1/models
	正確GET網址資料如下:
	{
		"data": [
			{
				"id": "qwen/qwen3.5-9b",
				"object": "model",
				"owned_by": "organization_owner"
			},
			{
				"id": "deepseek-r1-distill-qwen-7b",
				"object": "model",
				"owned_by": "organization_owner"
			},
			{
				"id": "text-embedding-nomic-embed-text-v1.5",
				"object": "model",
				"owned_by": "organization_owner"
			}
		],
		"object": "list"
	}


