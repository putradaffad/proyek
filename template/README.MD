# STRUKTUR LARAVEL FILAMENT

## Menjalankan Docker
- docker compose up -d --build
- docker exec -it pemweb bash

## Membuat Project Laravel Filament Starter
- composer create-project --prefer-dist raugadh/fila-starter .

# Jika gagal hapus isi folder
- rm -rf *
- rm -rf .*

## Set Permission Storage
- chown -R www-data:www-data storage/*

## Edit File .env
- APP_NAME="PemWeb"
- APP_TIMEZONE='Asia/Jakarta'
- APP_URL=http://localhost
- ASSET_URL=http://localhost
- DB_CONNECTION=mysql
- DB_HOST=db_pemweb
- DB_PORT=3306
- DB_DATABASE=db_pemweb
- DB_USERNAME=root
- DB_PASSWORD=p455w0rd

## Migrasi Database & Seeder
- php artisan migrate
- php artisan migrate:fresh
- php artisan db:seed --force

## Generate Shield & Init Project
- php artisan shield:generate --all
- php artisan project:init

## Set Permission
- chmod 777 -R storage/* && chmod 777 bootstrap/*
