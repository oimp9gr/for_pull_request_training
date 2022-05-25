Сделано


1. [Создайте fork репозитория.](https://user-images.githubusercontent.com/35418986/170212411-0a19bb1d-e2ff-47e7-979e-6eae098f222b.png)

2. Склонируйте репозиторий к себе на компьютер.

    2.1. [Скопируйте ссылку на репозиторий.](https://user-images.githubusercontent.com/35418986/170212811-01da4207-e911-4569-8594-4d43eba02d1f.png)

    2.2. [Откройте git bash в директории куда вы хотите склонировать репозиторий.](https://user-images.githubusercontent.com/35418986/170213533-6d1d6f2b-e173-4a77-92b0-3ea214c8dfb9.png) (если у вас нет такой опции, то скорее всего у вас не установлен git)

3. Измените ваш git config при помощи команды `git config -e`, следующм образом:

```
[filter "lfs"]
        clean = git-lfs clean -- %f
        smudge = git-lfs smudge -- %f
        process = git-lfs filter-process
        required = true
[core]
        editor = vim
[credential]
        helper = osxkeychain
        useHttpPath = true
[user]
        email = <your email>
        name = <your name>
```

где вместо <your email> впишите ваш email от github.com. Найти его можно [здесь](https://user-images.githubusercontent.com/35418986/170214607-1a2b6e37-010b-4179-a1dd-86451c3fad7a.png). Вместо <your name> впишите ваше имя.

3. [Добавьте изменения и сделайте commit.](https://user-images.githubusercontent.com/35418986/170215646-afd36f28-f22d-4172-9ae9-8cebe08b38ae.png)
  
4. Запушьте изменения: `git push origin main`. Если у вас открылось такое [окошко](https://user-images.githubusercontent.com/35418986/170215761-5e7227fc-820b-4482-9621-34514ec6751a.png) для авторизации на github, то следуйте инструкциям в нём для авторизации.

5. Зайдите к вам в репозиторий и нажмите [contribute->open pull request](https://user-images.githubusercontent.com/35418986/170219883-bb788e65-c3cd-412a-b7a1-4a7a0cc74a6b.png).

6. Поменяйте имя PR на ваше имя и фамилию латиницей. И создайте Pull Request.

Должен получиться примерно [такой](https://user-images.githubusercontent.com/35418986/170220429-2f5c77c7-dfb5-4281-b6a0-1306c946a083.png) результат.
