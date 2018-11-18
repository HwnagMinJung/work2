import requests

url='https://search.naver.com/search.naver?sm=top_hty&fbm=0&ie=utf8&query=%EC%99%84%EB%B2%BD%ED%95%9C+%ED%83%80%EC%9D%B8'
response = requests.get(url)

print(response)

st = sim/date
srchby = all/title
date_from = yyyymmdd
date_to = yyyymmdd
date_option = 0/2/3/4/6/7/8
dup_remove = 0/1
start = '숫자'

param = {
    'where' : 'post',
    'query' : '완벽한 타인',
    'date_from':'20181112',
    'date_to' : '20181118',
    'date_option':'8' }
response = requests.get(url,params=param)
soup = BeautifulSoup(response.text, 'html.parser')

are=soup.find('div',{'class': 'blog section _blogbase'}).find_all('a',{'class':'url'})
