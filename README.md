# PHP_API
Using PHP to complete API connection

＊目的　Objective
一般API串接可由JavaScript在HTML頁面發出。優點是方便易使用，缺點是若API須提供金鑰，則會將金鑰暴露於公開環境下。本案例將API串接工作移置PHP執行，此作法在HTML頁面僅能看到發送訊息到PHP檔案與接收PHP回傳的資料，API的金鑰保存在PHP檔案中。
API connection can be issued by JavaScript in HTML pages. The pros is that it is convenient and easy to use, but the cons is that if the API needs to provide the key, the key will be exposed to in public. In this case, the API connection is execute in PHP. In this method, only the information sent to the PHP file and the data responosed by PHP can be seen on the HTML page. The API key is stored in the PHP file.


＊方法　Methods
file_get_contents()


＊備註　Note
php伺服器若關閉allow_url_fopen，則file_get_contents()會產生錯誤：
Warning: file_get_contents(): http:// wrapper is disabled in the server configuration by allow_url_fopen=0

此時有兩種解法：
1. php伺服器開啟allow_url_fopen，但容易產生安全隱患
2. 使用CURL方法改寫


＊參考文獻　References 
https://5balloons.info/fix-file_get_contents-disabled-error-php/amp/
