#Kali Linux

## 1.1. Скачивание и установка

Качаем с сайта https://www.kali.org/downloads/
Устанавливаем по методике https://youtu.be/LMla679bTOY
После этого вставляем флешку, перезагружаем компьютер, запускаемся с флешки через биос.

> логин: root
> пароль: toor

## 1.2. Настройка режима Persistence

1.2.1. После загрузки в терминале вводим `fdisk`, чтобы отыскать название флешки.
1.2.2. Создаем раздел Persistence, используюя любую программу: MiniTool Partition Magic, Gparted и т.д.
1.2.3. Остальные настройки

```
fsisk - l (смотрим имеющиеся разделы и какое имя у persistance - sda или sdb)
mkdir -p /mnt/sdb2
mount /dev/sdb2 /mnt/sdb2
echo "/ union" > /mnt/sdb2/persistence.conf
umount /dev/sdb2
перезагружаемся в persistence
```
