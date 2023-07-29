<h3>Как отправлять сообщения от имени бота?</h3>
<h5>
  [Проверено на Aiogram 2]
  За основу можете взять этот код:
<details>
  <summary>Код </summary>
import requests<br>
while 1:<br>
    chat_id = ""<br>
    message = input()<br>
    url = f"https://api.telegram.org/bot{API_TOKEN}/sendMessage?chat_id={chat_id}&text={message}"<br>
    print(requests.get(url).json())<br>
</details>
</h5>
