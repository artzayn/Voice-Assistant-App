# Voice-Assistant-App
Проект голосового ассистента на Python 3 для Windows 10, который умеет:
* распознавать и синтезировать речь в offline-моде (без доступа к Интернету);
* воспроизводить случайное приветствие;
* воспроизводить случайное прощание с последующим завершением работы программы;
* производить поисковый запрос в поисковой системе Google
  (а также открывать список результатов и сами результаты данного запроса);
* производить поисковый запрос видео в системе YouTube и открывать список результатов данного запроса;
* выполнять поиск определения в Wikipedia c дальнейшим прочтением первых двух предложений;
* переводить с изучаемого языка на родной язык пользователя (с учетом особенностей воспроизведения речи);
* менять настройки языка распознавания и синтеза речи;
* TODO многое другое...

Голосовой ассистент использует для синтеза речи встроенные в операционную систему Windows 10 возможности
(т.е. **голоса зависят от настроек операционной системы**). Для этого используется библиотека `pyttsx3`

    Для корректной работы системы распознавания речи в сочетании с библиотекой SpeechRecognition
    используется библиотека PyAudio для получения звука с микрофона.
    
Для установки PyAudio можно найти и скачать нужный в зависимости от архитектуры и версии Python whl-файл [здесь](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio) в папку с проектом.
После чего его можно установить при помощи подобной команды: `pip install PyAudio-0.2.11-cp37-cp37m-win_amd64.whl`

    Для использования SpeechRecognition в offline-режиме (без доступа к Интернету), потребуется дополнительно установить pocketsphinx (качество ниже, чем у Google)

Для избежания проблем с установкой, я предлагаю скачать whl-файл в зависимости от требуемой архитектуры и версии Python. Его можно найти [здесь](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pocketsphinx)
Загрузив файл в папку с проектом, установку можно будет запустить с помощью подобной команды: `pip install pocketsphinx-0.1.15-cp37-cp37m-win_amd64.whl`

Команды для установки прочих сторонних библиотек:
Команда установки  | Назначение библиотеки
----------------|----------------------
`pip install google`       | Работа с результатами поисковых запросов в Google
`pip install SpeechRecognition`       | Работа с распознаванием речи (Speech-To-Text), в проекте используется Google при наличии доступа в Интернет
`pip install pyttsx3`   | Работа с offline-синтезом речи на Windows (Text-To-Speech)
`pip3 install wikipedia-api`| Работа с Wikipedia API
`pip install googletrans`| Работа с Google Translate

Дополнительную информацию по установке и использованию библиотек можно найти [здесь](https://pypi.org/)

    У меня не возникало проблем с установкой библиотек, перечисленных в таблице выше, потому прилагаю только команды.
    В случае возникновения проблем с установкой, вы можете воспользоваться тем же способом, который я предлагала для установки PyAudio и pocketsphinx выше. 
