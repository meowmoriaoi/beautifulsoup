# BeautifulSoup

```python
import requests  
from bs4 import BeautifulSoup

res = requests.get('https://nyaa.si')
soup = BeautifulSoup(res.content)

soup.find('div')
soup.find_all('td')[2]

soup.find(id="navbar")
soup.find_all(class_="success")
soup.find(attrs={"colspan": "2"})

soup.select('.text-center')
soup.select('#navbar')

soup.select('.text-center')[0].get_text()

for item in soup.select('.item'):
  print(item.get_text())
  
soup.body.div.contents[1].contents
soup.body.div.contents[0].next_sibling()

soup.find(id="section-3").find_previous_sibling()
soup.find(class_="autis").find_parent()
soup.find('h3').find_next_sibling('p')
```
