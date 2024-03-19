import os

# Загрузка настройки рабочей папки из файла конфигурации
def load_config():
    with open('config.txt', 'r') as file:
        return file.read()

# Создание папки
def create_folder(folder_name):
    try:
        os.mkdir(os.path.join(load_config(), folder_name))
        print(f"Папка {folder_name} создана.")
    except FileExistsError:
        print(f"Папка {folder_name} уже существует.")

# Удаление папки
def delete_folder(folder_name):
    try:
        os.rmdir(os.path.join(load_config(), folder_name))
        print(f"Папка {folder_name} удалена.")
    except FileNotFoundError:
        print(f"Папка {folder_name} не найдена.")

# Перемещение в папку
def move_to_folder(folder_name):
    new_path = os.path.join(load_config(), folder_name)
    if os.path.isdir(new_path):
        os.chdir(new_path)
        print(f"Перемещение в папку {folder_name}.")
    else:
        print(f"Папка {folder_name} не найдена.")

# Создание файла
def create_file(file_name):
    with open(os.path.join(load_config(), file_name), 'w') as file:
        pass  # пустой файл создан

# Запись в файл
def write_to_file(file_name, text):
    with open(os.path.join(load_config(), file_name), 'w') as file:
        file.write(text)

# Чтение файла
def read_file(file_name):
    try:
        with open(os.path.join(load_config(), file_name), 'r') as file:
            print(file.read())
    except FileNotFoundError:
        print(f"Файл {file_name} не найден.")

# Удаление файла
def delete_file(file_name):
    try:
        os.remove(os.path.join(load_config(), file_name))
        print(f"Файл {file_name} удален.")
    except FileNotFoundError:
        print(f"Файл {file_name} не найден.")

# Копирование файла
def copy_file(file_name, destination_folder):
    try:
        os.replace(os.path.join(load_config(), file_name), os.path.join(load_config(), destination_folder, file_name))
        print(f"Файл {file_name} скопирован в папку {destination_folder}.")
    except FileNotFoundError:
        print(f"Файл {file_name} не найден.")

# Перемещение файла
def move_file(file_name, destination_folder):
    try:
        os.replace(os.path.join(load_config(), file_name), os.path.join(load_config(), destination_folder, file_name))
        print(f"Файл {file_name} перемещен в папку {destination_folder}.")
    except FileNotFoundError:
        print(f"Файл {file_name} не найден.")

# Переименование файла
def rename_file(old_name, new_name):
    try:
        os.rename(os.path.join(load_config(), old_name), os.path.join(load_config(), new_name))
        print(f"Файл {old_name} переименован в {new_name}.")
    except FileNotFoundError:
        print(f"Файл {old_name} не найден.")


# Пример использования функций
if __name__ == "__main__":
    # Пример использования
    create_folder('новая_папка')
    delete_folder('старая_папка')
    move_to_folder('папка_2')
    create_file('новый_файл.txt')
    write_to_file('новый_файл.txt', 'Пример текста')
    read_file('новый_файл.txt')
    delete_file('старый_файл.txt')
    copy_file('файл.txt', 'папка_2')
    move_file('файл.txt', 'папка_3')
    rename_file('старый_файл.txt', 'новый_файл.txt')
