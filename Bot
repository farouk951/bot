import telebot
import requests
bot = telebot.TeleBot("1765795314:AAHTTxszSO1X2sWBuXABbi_pBYDcPoks3uc")
tok = "1765795314:AAHTTxszSO1X2sWBuXABbi_pBYDcPoks3uc"
banner = requests.get("https://pastebin.com/raw/YVX1VdBp").text
@bot.message_handler(commands=["start"])
def start(message):
	global tok
	global banner
	bot.send_message(message.chat.id,text=f"*{banner}\n\n\nHey @{message.from_user.username} \nIn Scrape Me Bot For Any help Type /help *",parse_mode="markdown")
	
@bot.message_handler(commands=["help"])
def help(message):
	bot.send_message(message.chat.id,text=f"*Welcome In Our Bot ❤\n\nDevelopers 🧑‍💻 : @FFQ_Q 🇹🇳 ، @ZIQO_0 🇲🇦 ، @SISKKO 🇹🇳\n\nCHANNEL : @CRACKWON ، @BREFAMILLY\n \nTo Get Proxies Choose : \n/http\n/socks4\n/socks5\n/socks5vanish *",parse_mode="markdown")
@bot.message_handler(commands=["http"])
def http(message):
	bot.reply_to(message,text="*Scraping...*",parse_mode="markdown")
	bh = requests.get("https://www.secproxy.org/getProxies?key=d71b3ced70c4805d6ffa6fe6fc0dcf1e&type=https&service=all").text
	rh = requests.get("https://api.proxyscrape.com/v2/?request=getproxies&protocol=http&timeout=10000&country=all&ssl=all&anonymity=all").text
	with open("http.txt","w") as h:
		h.write(rh+bh)
	hh = open("http.txt","rb")
	bot.send_document(message.chat.id,hh)
@bot.message_handler(commands=["socks5vanish"])
def vanish(message):
	bot.reply_to(message,text="*Scraping...*",parse_mode ="markdown")
	with open("socks5_ipvanish.txt","w")as v:
		v.write(requests.get("https://www.secproxy.org/getProxies?key=d71b3ced70c4805d6ffa6fe6fc0dcf1e&type=socks5&service=all").text)
		vv=open("socks5_ipvanish.txt","rb")
		bot.send_document(message.chat.id,vv)
@bot.message_handler(commands=["socks4"])
def socks4(message):
	bot.reply_to(message,text="*Scraping...*",parse_mode="markdown")
	so = requests.get("https://www.secproxy.org/getProxies?key=d71b3ced70c4805d6ffa6fe6fc0dcf1e&type=socks4&service=all").text
	sk = requests.get("https://api.proxyscrape.com/v2/?request=getproxies&protocol=socks4&timeout=10000&country=all").text
	with open("socks4.txt","w")as s:
		s.write(so+sk)
	so4=open("socks4.txt","rb")
	bot.send_document(message.chat.id,so4)
@bot.message_handler(commands=["socks5"])
def socks5(message):
	bot.reply_to(message,text="*Scraping...*",parse_mode="markdown")
	r5 = requests.get("https://api.proxyscrape.com/v2/?request=getproxies&protocol=socks5&timeout=10000&country=all").text
	with open("socks5.txt","w")as sok5:
		sok5.write(r5)
	soo5 = open("socks5.txt","rb")
	bot.send_document(message.chat.id,soo5)
	print(message.text)
bot.polling()
