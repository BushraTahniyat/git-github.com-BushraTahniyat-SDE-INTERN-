# git-github.com-BushraTahniyat-SDE-INTERN-
import requests
import lxml
import BeautifulSoup
import urllib.request
url = urllib.request.urlopen("https://knowthychoice.in/blog/")
headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.132 Safari/537.36 QIHU 360SE'
}
f = requests.get(url, headers = headers)
programs_lst = []
soup = BeautifulSoup(f.content, 'lxml')
programs = soup.find('table',{'class':'table'}).find_all()
num = 0
urls =urllib.request.urlopen("https://knowthychoice.in/blog = anchor['href']")
programs_lst.append(urls)
num+= 1
programs_url = urls
programs_f = requests.get(programs_url, headers = headers)
programs_soup = BeautifulSoup(programs_f.content,'lxml')
programs_content =programs_soup.find('div', {
  'class': 'programs_synopsis clamp clamp-6 js-clamp'
})
print(num, urls, '\n','Program:' + content.string.strip())
print('Program info:'+ programs_content.string.strip())
