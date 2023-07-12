import telebot
import webbrowser

bot = telebot.TeleBot('5953185850:AAHa95PpRhrA0egpSjQNUxvQbFeUOXkhe98')


@bot.message_handler(commands=['site', 'websites'])
def site(message):
    webbrowser.open('https://www.ivi.ru/new')


@bot.message_handler(commands=['start'])
def main(message):
    bot.send_message(message.chat.id, f'Здравствуйте, {message.from_user.first_name} {message.from_user.last_name}! Выберите жанр фильмов/сериалов, которые больше всего вам нравиться смотреть.')

@bot.message_handler(commands=['main'])
def main(message):
    bot.send_message(message.chat.id, f'Боевик\n'f'Вестерн\nГангстерский фильм\nДетектив\nДрама\nИсторический фильм\nКомедия\nМелодрама\nМузыкальный фильм\nНуар\nПолитический фильм\nПриключенческий фильм\nСказка\nТрагедия\nТрагикомедия')


@bot.message_handler()
def into(message):
    if message.text.lower() == 'приветствие':
        bot.send_message(message.chat.id, f'Здравствуйте, {message.from_user.first_name} {message.from_user.last_name}!','Выберите жанр фильмов/сериалов, которые больше всего вам нравиться смотреть.')
    elif message.text.lower() == 'id':
        bot.reply_to(message, f'ID: {message.from_user.id}')


bot.polling(none_stop=True)
