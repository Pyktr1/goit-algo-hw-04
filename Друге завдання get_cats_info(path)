# cтворення функції def get_cats_info(path)

def get_cats_info(path):


    # список для котів
    cats = []

    try:

        # відкриття файла для читання
        with open(path, "r", encoding="utf-8") as file:
            for line in file:

                # видалення пробілу 
                line = line.strip()

                # пропуск порожніх рядків
                if not line:
                    continue

                # добавляння коми
                parts = line.split(",")

                # чи є всі три елементи
                if len(parts) != 3:
                    continue


                cat_id, name, age = parts
                
                # словник для одного кота
                cat_info = {
                    "id": cat_id,
                    "name": name,
                    "age": age
                }

                 # словник до списку
                cats.append(cat_info)

    except FileNotFoundError:
        print(f"Файл за шляхом {path} не знайдено.")
    except Exception as e:
        print(f"Сталася помилка під час читання файлу: {e}")

    return cats


if __name__ == "__main__":

    # інформація про котів список з ID NAME AGE з шляхом до текстового файлу ("cats1.txt")
    cats_info = get_cats_info("cats1.txt")

    # виклик коду 
    print(cats_info)
