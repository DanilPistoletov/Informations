<h3>Как отправлять сообщения от имени бота?</h3>
<h5>
  [Проверено на Aiogram 2]<br>
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
<h3>Как приветствовать новых пользователей чата?</h3>
<h5>[Проверено на Aiogram 3]</h5><br>
Пример кода:
<details>
  <summary>Код</summary>
@dp.message(F.new_chat_members)
async def new_member(message: types.Message):
  await bot.send_message(chat_id, "Привет, новенький")
</details>
<h3>Можно ли использовать два равных диспетчера одновременно?</h3>
<details><summary>Ответ</summary>
Нет, один из них будет перекрывать работу другого. Лучше включить функционал одного диспетчера внутрь другого.<br>
Если ваш диспетчер обрабатывает только текст, а нужно ещё стикеры, картинки и так далее - пропишите другой диспетчер для этого вида сообщений отдельно.
</details>
