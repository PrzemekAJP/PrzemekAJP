# Instalacja Laravel - Krok po Kroku

## Wprowadzenie

Ten plik zawiera szczegółową instrukcję krok po kroku dotyczącą instalacji środowiska programistycznego, utworzenia projektu Laravel oraz instalacji wszystkich niezbędnych zależności. Poniżej znajdziesz instrukcje dotyczące instalacji narzędzi takich jak PHP, Composer, MySQL, Node.js oraz Git.

## 1. Wymagania systemowe

Aby uruchomić projekt Laravel, musisz mieć zainstalowane następujące narzędzia:

- **PHP** (wersja 8.0 lub nowsza)
- **Composer** (menedżer zależności dla PHP)
- **MySQL** (XAMPP i phpmyadmin)
- **Node.js i npm** (do kompilacji zasobów front-endowych)
- **Git** (do zarządzania wersjami)

## 2. Tworzenie aplikacji w Laravel

Najpierw zainstaluj Laravel, korzystając z Composer:
composer create-project --prefer-dist laravel/laravel mini-aplikacja
cd mini-aplikacja

## 3. Połączenie z bazą danych

W pliku .env, ustaw połączenie z bazą danych (np. MySQL):
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=mini-aplikacja
DB_USERNAME=root
DB_PASSWORD=

Użyjemy migracji do tworzenia tabel użytkowników:
php artisan migrate

## 4. Obsługa kont użytkowników
Laravel ma wbudowaną obsługę systemu logowania. Możemy skorzystać z pakietu Laravel Breeze:
composer require laravel/breeze --dev
php artisan breeze:install
npm install
npm run dev
php artisan migrate

## 5. Użycie PHPMailer
Zainstaluj PHPMailer za pomocą Composera:
composer require phpmailer/phpmailer

## 6. Uruchomienie serwera
Aby uruchomić serwer należy wykonać polecenie:
php artisan serve

Otwieranie stron w przeglądarce:
Po uruchomieniu serwera możesz otworzyć poszczególne strony w przeglądarce, korzystając z adresu http://localhost:8000.
