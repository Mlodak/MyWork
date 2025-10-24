# EStoreApi

API dla sklepu internetowego (E-Store) zbudowane w ASP.NET Core 9.0, zapewniające kompletną funkcjonalność do zarządzania produktami, kategoriami, użytkownikami i zamówieniami.

## 📋 Opis

EStoreApi to RESTful API dla aplikacji e-commerce, oferujące:
- Zarządzanie użytkownikami (rejestracja, logowanie z JWT)
- Zarządzanie produktami i kategoriami
- System koszyka zakupowego
- Obsługa zamówień
- Autoryzacja oparta na rolach (Admin, Customer)

## 🚀 Technologie

- **.NET 9.0**
- **C# 13.0**
- **ASP.NET Core Web API**
- **Entity Framework Core** (prawdopodobnie)
- **JWT Authentication**
- **Repository Pattern**

## 📦 Funkcjonalności

### Użytkownicy (`/api/Users`)
- `POST /RegisterUser` - Rejestracja nowego użytkownika
- `POST /LoginUser` - Logowanie użytkownika i otrzymanie tokenu JWT

### Produkty (`/api/Products`) 🔒
- `GET /` - Pobranie listy produktów z filtrowaniem po typie i kategorii
- `GET /{id}` - Pobranie szczegółów produktu
- `POST /` - Dodanie nowego produktu (tylko Admin)
- Wsparcie dla produktów trendujących i najlepiej sprzedających się

### Kategorie (`/api/Categories`) 🔒
- `GET /` - Pobranie wszystkich kategorii
- `POST /` - Dodanie nowej kategorii (tylko Admin)
- `DELETE /{id}` - Usunięcie kategorii (tylko Admin)

### Zamówienia (`/api/Orders`) 🔒
- `GET /` - Pobranie wszystkich zamówień (tylko Admin)
- `GET /user/{userId}` - Pobranie zamówień użytkownika
- `GET /{orderId}` - Pobranie szczegółów zamówienia
- `POST /` - Złożenie nowego zamówienia

🔒 - wymaga autoryzacji

## ⚙️ Wymagania

- [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)
- SQL Server lub inna baza danych zgodna z Entity Framework Core
- Visual Studio 2022 lub VS Code (opcjonalnie)

## 🔧 Instalacja i Konfiguracja

1. **Sklonuj repozytorium:**

2. **Skonfiguruj connection string:**

Edytuj plik `appsettings.json` i dodaj swój connection string do bazy danych.

3. **Skonfiguruj klucz JWT:**

W pliku `appsettings.json` dodaj sekcję:

4. **Uruchom migracje bazy danych:**

5. **Uruchom aplikację:**

API będzie dostępne pod adresem: `https://localhost:7xxx` lub `http://localhost:5xxx`

## 🔑 Autoryzacja

API używa JWT Bearer Token do autoryzacji. Po zalogowaniu otrzymasz token, który należy dołączyć do nagłówka żądania:

### Role użytkowników:
- **Customer** - standardowy użytkownik (zakupy, przeglądanie produktów)
- **Admin** - administrator (pełne zarządzanie produktami, kategoriami, zamówieniami)

## 📝 Przykłady użycia

### Rejestracja użytkownika
````````
{
	"email": "test@example.com",
	"password": "string",
	"confirmPassword": "string"
}
````````

## 📂 Struktura projektu


## 👨‍💻 Autor

[Mlodak](https://github.com/Mlodak) sysmed@sysmed.com.pl

## 📄 Licencja

Ten projekt jest dostępny na licencji [MIT](LICENSE) _(dodaj plik LICENSE jeśli potrzebny)_

---

⭐ Jeśli projekt Ci się podoba, zostaw gwiazdkę!