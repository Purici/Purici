import zipfile
import os

# Create directories
os.makedirs('/mnt/data/project/gallery', exist_ok=True)

# Create HTML file
html_content = """<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Установка мебели и перевозка тяжелых грузов</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Установка мебели и перевозка тяжелых грузов</h1>
        <nav>
            <ul>
                <li><a href="#home">Главная</a></li>
                <li><a href="#about">О нас</a></li>
                <li><a href="#services">Услуги</a></li>
                <li><a href="#gallery">Галерея</a></li>
                <li><a href="#contact">Контакты</a></li>
                <li><a href="#blog">Блог</a></li>
            </ul>
        </nav>
    </header>
    <section id="home">
        <h2>Профессиональные услуги по доступным ценам</h2>
        <p>Предлагаем качественные услуги по установке мебели и транспортировке тяжелых предметов. Наша команда профессионалов обеспечит безопасную и быструю работу.</p>
        <button onclick="location.href='#contact'">Заказать сейчас</button>
        <button onclick="location.href='#services'">Узнать больше</button>
    </section>
    <section id="about">
        <h2>О нас</h2>
        <p>Наша компания имеет более 10 лет опыта в установке мебели и перевозке тяжелых грузов. Мы гарантируем качество и надежность наших услуг.</p>
    </section>
    <section id
