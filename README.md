# Train Your Own Neural Network (Handwritten Digits)

Bilingual (English / Русский) lesson notebook: students teach a small neural network to read their own handwriting, change its settings and compare results.

**Open in Binder (no account needed):**

https://mybinder.org/v2/gh/YOUR_GITHUB_NAME/YOUR_REPO_NAME/HEAD?urlpath=lab/tree/Train_Your_Own_Neural_Network_Binder.ipynb

Replace `YOUR_GITHUB_NAME` and `YOUR_REPO_NAME` with your GitHub user name and the name of this repository.

## Для учителя (по-русски)

1. Создайте на github.com **публичный** репозиторий (Public), например `neural-network-digits`.
2. Загрузите в него все файлы этой папки: нажмите «Add file → Upload files» и перетащите содержимое папки (включая папки `sample_digits` и `my_digits`). Файл `mnist.pkl.gz` весит около 17 МБ, через браузер он загружается.
3. Подставьте имя пользователя и название репозитория в ссылку выше.
4. **Откройте ссылку сами за день до урока и в день урока.** Первый запуск собирает среду и занимает несколько минут, повторные быстрее. Если открыть ссылку заранее, сервис подготовит образ.
5. Раздайте ссылку ученикам. Каждый получает свою временную копию.

### Как ученики добавляют картинки
В левом списке файлов дважды щёлкнуть папку `my_digits`, нажать кнопку **Upload** (стрелка вверх) и выбрать файлы `0.png` … `9.png`. Новую картинку для проверки загружают в ту же папку под именем `new.png`. Нет своих картинок: в блокноте поменять `DIGITS_FOLDER = "sample_digits"` на готовый набор.

### Задание в паре (Step 3B)
После первого обучения ученики обмениваются своими 10 картинками с соседом (мессенджер, почта, флешка), загружают файлы соседа в папку `friend_digits` (блокнот создаёт её сам) и запускают ячейку Step 3B: сеть читает чужой почерк. Результат «friend» попадает в итоговую таблицу. Затем пары меняются ролями и обсуждают, почему сеть ошибается на чужом почерке.

### Что важно знать
- Сессия Binder временная: после примерно 10 минут без активности она закрывается, и загруженные файлы и результаты пропадают. Результаты записывайте в рабочий лист.
- При 15 одновременных запусках сервис может работать медленно или отказать. Проверьте работу заранее и держите запасной вариант (работа в парах с Google Colab или локальный запуск).
- Если обучение идёт слишком долго, уменьшите `MNIST_SIZE` или `EPOCHS` в Step 2.
- Запуск без интернета: установите Python 3 и выполните `pip install notebook numpy matplotlib pillow`, затем откройте блокнот командой `jupyter notebook`.

## Files

- `Train_Your_Own_Neural_Network_Binder.ipynb`: the bilingual lesson notebook (every cell has English and Russian text)
- `network.py`, `mnist_loader.py`, `mnist.pkl.gz`, `LICENSE.md`: network code and MNIST data from the Python 3 port by Michał Dobrzański (MIT licence) of Michael Nielsen's [neural-networks-and-deep-learning](https://github.com/mnielsen/neural-networks-and-deep-learning). One change: a docstring in `network.py` was made a raw string to remove a harmless `SyntaxWarning`.
- `requirements.txt`: libraries Binder installs
- `sample_digits/`: ready-made pictures `0.png` … `9.png` and `new.png`
- `my_digits/`: the folder where students upload their own pictures
- `friend_digits/`: created by the notebook; the neighbour's pictures go here (Step 3B pair task)
