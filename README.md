# Network-Administration

##申請Let's Encrypt憑證 (FreeBSD/Apache)

**1.	安裝Git指令**
使用package安裝: `pkg install git`

**2.	從GitHub下載Let's Encrypt專案所有的程式碼**
` git clone https://github.com/letsencrypt/letsencrypt`
> 備註：Git指令會在你目前執行的目錄中，產生一個「letsencrypt」目錄，存放Let's Encrypt專案的所有程式碼

**3.  向Let's Encrypt申請SSL憑證**
> 若要簽兩個domain, 可用同一把key(可重複使用)   
> 可去/etc/letsencrypt/renewal 底下找key資訊

`cd letsencrypt`   
需在/etc/letsencrypt/letsencrypt下執行   
`./letsencrypt-auto --debug certonly --webroot --email xxx@xxx.com.tw -w /usr/local/www/tech.idv.tw -d tech.idv.tw -d www.tech.idv.tw`

* 「--email xxx@xxx.com.tw」請填上你的聯絡信箱
* 「-w /usr/local/www/tech.idv.tw」是指定你的網站存放的目錄
* 「-d tech.idv.tw」是指你要申請的網域名稱

## Add this header in virtual host zone file to get a+ in ssllab
