import bs4, requests

def getAmazonPrice(productUrl):
    res = requests.get(productUrl)
    res.raise_for_status()
    
    soup = bs4.BeautifulSoup(res.text, 'html.parser')
    elem = soup.select('#price_inside_buybox')
    return elem[0].text.strip()
    
price = getAmazonPrice('https://www.amazon.com/gp/product/B07L87MH64/ref=as_li_tl?ie=UTF8&tag=outofstress-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=B07L87MH64&linkId=e4dcdf93f35335c858d0ae2b80db0aac')
print('The price is ' + price)
