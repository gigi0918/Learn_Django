# 輿情分析

## 週計畫

- Django 學習
- csv 匯入與匯出資料
- FB 爬蟲
- 語意分析資料匯入csv檔案
- 文檔製作
- Kibana 使用
- JS自行設計




## 　Ｄjango 網路框架(Python)

### 環境設置 

Python : 3.6.3

Django : 1.11.9

### Install the Django:

```
$　pip install django==1.11.9 
```
```
$ python manage.py migrate
```
### Runing the Django:
```
$ python manage.py runserver
```
Brower： http://127.0.0.1:8000/

###　爬蟲


首頁路徑: home / templates / crawl_home.html

Python 爬蟲路徑 :  home /view.py 

### 跳頁

建立 html 檔案 
```
<form action="/home/Dcard_visulize/" method="post">
    {% csrf_token %}
        標題: <input type="text" name="title"> <br> <br>
    <input type="submit" value="Dcard">

</form>
```
在 home/urls.py中加連結
```
urlpatterns = [
    path('', views.crawl_home),
    path('POST_crawl/', views.POST_crawl),
    path('POST_crawl_PTT/', views.POST_crawl_PTT),
    path('Dcard_visulize/', views.Dcard_visulize),

]

```
在 home/views.py 呼叫函式
```
def Dcard_visulize(request):

    return render(request, 'dcard_visulize.html')
```

### 頁面服務

- home
功能: 搜尋主題，分為Dcard、PTT、fb 等按鈕進行分析。
Button: Dcard、PTT、fb

-- POST_crawl
功能:顯示 Dcard 的ID、愛心數、留言數、文章情緒值(圖片顯示or數值?)，可針對單一文章進行分析。
Button: 分析、下一頁(?)。

-- Dcard_visulize
功能: DashBoard (主要:標題、愛心數、留言數、文章內容、文章情緒值、留言內容、留言情緒值)




-------------------------------------
## 服務器端網站框架

## 伺服器端程式設計
[參考連結](https://developer.mozilla.org/zh-TW/docs/Learn/Server-side/First_steps)

## 網路伺服器(Web server)
[參考連結](https://developer.mozilla.org/zh-TW/docs/Learn/Common_questions/What_is_a_web_server)

可以指軟體、硬體、或他們共同運作的狀態。

+ 靜態網路伺服器:as-is
+ 動態網路伺服器:application server 、database

##　網站需要什麼軟件

[參考連結](https://developer.mozilla.org/zh-TW/docs/Learn/Common_questions/What_software_do_I_need)

## 網頁 VS 網站 VS 

[參考連結](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines)


## Internet work

[參考連結](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)

DSL 

ADSL 非對稱數碼用戶線路

ISP 網路服務業者

* 路由器(router):

* (modem):可將網路訊息轉成電話基礎架構管理的訊息傳送，反之亦然。

### Internet & Web
The Internet is an infrastructure, whereas the Web is a service built on top of the infrastructure. 