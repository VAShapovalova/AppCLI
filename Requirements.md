# Первый набор требований   

R1.1 Приложение должно аутентифицировать пользователя по логину и паролю (логин[a -z],{1-9})  

R1.2 Пароль должен храниться безопасно  

R1.3 Приложение должно авторизовывать пользователя к определенному ресурсу с определенной ролью(ресурс - слова из заглавных букв, разделенные точками)  

R1.4 Ресурсы должны храниться в виде дерева  

R1.5 Допустимые роли - WRITE., READ, EXECUTE  

R1.6 Доступ к ресурсу с определенной ролью автоматически предоставляет доступ ко всем его потомкам  

R1.7 Приложение должно иметь возможность учесть время доступа и потребляемый объем  

R1.8 Приложение это консольная утилита, принимающая на вход параметры:  
 пусто  
`-h вывод справки`  
`-login<str>  -pass<str> `  
`-login<str>  -pass<str> -<res> -<role>`   
`-login<str>  -pass<str>  -<res> -<role> -ds<YYYY-MM-DD> -de<YYYY-MM-DD> -vol<int>`  

R1.9 Приложение возвращает следующие коды: 0 - успех , 1 - справка, 2 - неверный формат логина, 3 - неизвестный логин, 4 - неверный пароль, 5 - неизвестная роль, 6 - нет доступа, 7 - некорректная активность(неверная дата или объем)  

R1.10 Приложение на вход принимает параметры в любом порядке  

R1.11 Приложение должно сначала аутентифицировать(коды 0,1,2,3,4), потом авторизовать(коды 0, 5, 6), потом аккаунтить(коды 0, 7)  

R1.12 Создайте скрипты bash/sh которые:   
* компилируют и собирают jar  
* выполняют программу  
* прогоняют тесты
