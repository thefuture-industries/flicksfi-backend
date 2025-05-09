# Как внести свой вклад

Благодарим вас за проявленный интерес к проекту! Мы приветствуем любые улучшения и исправления. Чтобы процесс был максимально плавным, пожалуйста, следуйте следующим рекомендациям.

## ВАЖНЫЕ ПРАВИЛА

1. Ветку main не трогаем и не изменяем!
2. В репозитории всегда есть версионные ветки (например v0.5.x или v0.17.192), после исправления фитчи или исправления бага надо создать pull request - создается именно в эти ветки. (а не в MAIN!!!)
   `Как определить текущую версионную ветку?` - Смотрите в репозитории слева последний релиз например v0.4.121 - значит текущая версионная ветка v0.5.x

## Основные шаги

1. Клонируем репозиторий

```bash
git clone https://github.com/thefuture-industries/flicksfi-backend
```

2. Для КАЖДОЙ новой фитчи или испралвения бага, cоздайте новую ветвь из основной ветви main. (По дефолту если делаете по issues - то ВЕТКА уже создана)

```bash
git checkout main
git checkout -b <your-branch-name>
```

Для получения веток и новый версий с GitHub используйте

```bash
git fetch
git checkout <ветка с GitHub>
```

3. Внесите изменения в индекс

```bash
git add .
```

4. Зафиксируйте изменения

```bash
git commit -m "<summary of changes>"
```

5. Отправьте изменения в свой репозиторий fork

```bash
git push origin <your-branch-name>
```

6. Создайте запрос (Pull Request) на перенос из вашей ветки в основную ветку проекта через интерфейс GitHub.
7. Дождитесь подтверждения. Наставники или другие участники проекта проверят ваши изменения и оставят комментарии, если потребуется дополнительная работа.
8. После того, как ваш Pull Request будет одобрен, он будет объединен с основной веткой!

> Мы ценим ваше время и усилия и надеемся, что этот процесс будет полезным и приятным!

## Основные команды Git

```bash
git fetch - Получает изменения из GitHub, но не применяет их к текущей ветке.
git pull - Загружает и сразу сливает изменения из GitHub ветки в текущую. Или еще так git pull origin <ветка>
git checkout <ветка> - Переключиться на существующую ветку.
git checkout -b <название ветки> - Создать новую ветку и сразу переключиться на неё.
git checkout -b <локальная ветка> origin/<ветка с GitHub> - Создать локальную копию GitHub ветки и переключиться на неё.
git branch - Позволяет посмотреть все ветки и в какой вы находитесь.
git branch <название ветки> - Просто создать новую ветку, но не переключаться на неё.
git branch <локальная ветка> origin/<ветка с GitHub> - Создать локальную ветку, ссылающуюся на Github ветку (без переключения).
git branch -D <локальная ветка> - Жёстко удалить локальную ветку (даже если в ней есть несохранённые изменения).
git stash - Убрать изменения и времено сохранить, чтобы очистить рабочую область.
git stash -u - Убрать изменения и времено сохранить, и еще новые (неотслеживаемые) файлы.
git stash pop - Вернуть последние отложенные изменения обратно в рабочую область.
git push origin <ветка> - Отправить локальную ветку на удалённый репозиторий.
git push origin --delete <ветка> - Удалить ветку на удалённом репозитории (GitHub).
git commit -m "описание изменений" - Сохранить изменения с комментарием.
git rebase <ветка> - Переписать текущую ветку так, как будто она основана на указанной (делает историю чище, но требует аккуратности). Например вы в ветки v0.6.x и вы хотите получить все изменения ветки v0.5.x тогда используйте - git checkout v0.6.x потом git rebase v0.5.x
git merge <ветка> - Объединить указанную ветку с текущей (сохраняет историю как есть).
```
