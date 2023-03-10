# Начало работы

Для начала нужно создать репозиторий, где вы будете хранить, писать и тестировать весь код, написанный в модуле. 
Для этого необходимо создать свой репозиторий из шаблона:

0. Откройте страницу шаблона:

```
https://github.com/cpppracticum/cpp-backend-template-practicum
```
1. Создайте собственный репозиторий из шаблона по данной инструкции:
- Необходимо придумать имя репозитория
- Копируя все ветки или только главную

```
https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template
```
2. Для создания локальной копии перейдите в консоли в папку где хотите расположить проект
и выполните команду заменив `<адрес созданного репозитория>` (включая скобки) на адрес вашего репозитория, созданного на предыдущем шаге:

```
git clone <адрес созданного репозитория> cpp-backend 
```

3. В результате вы получите локальную копию репозитория, расположенную по адресу <ваша папка>/cpp-backend. После этого останется только перейти в директорию с репозиторием:

```
cd cpp-backend 
```

# Обновление шаблона

4. Чтобы иметь возможность получать обновления автотестов и других частей шаблона выполните следующую команду:

```
git remote add -m main template https://github.com/cpppracticum/cpp-backend-template-practicum.git
```
5. Проверить результат добавления удалённой ветки можно командой:

```
git remote 
```
6. Теперь в вашем репозитории две удалённые ветки. Для обновления кода автотестов выполните команду:

```
git fetch template && git checkout template/main .github 
```
7. И обновить удаленный репозиторий в соответсвии с локальным

```
git push
```

# Тестирование в Github Actions

При отправке (push) изменений в ветку main репозитория будет запущен пайплайн Github Actions, 
который позволит увидеть результат прохождения тестов.
