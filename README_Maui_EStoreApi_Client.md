# MauiClient - Aplikacja E-commerce

![.NET MAUI](https://img.shields.io/badge/.NET%20MAUI-8.0-blue)
![Platform](https://img.shields.io/badge/platform-Android%20%7C%20iOS%20%7C%20Windows%20%7C%20macOS-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

## 📱 Opis Projektu

MauiClient to nowoczesna aplikacja mobilna e-commerce zbudowana przy użyciu .NET MAUI (Multi-platform App UI). Aplikacja umożliwia użytkownikom przeglądanie produktów, zarządzanie koszykiem zakupów, składanie zamówień oraz przeglądanie historii zamówień.

## 🎯 Funkcjonalności

### Uwierzytelnianie
- ✅ Rejestracja nowych użytkowników
- ✅ Logowanie użytkowników
- ✅ Zarządzanie tokenami JWT
- ✅ Bezpieczne przechowywanie danych uwierzytelniających

### Produkty
- ✅ Przeglądanie kategorii produktów
- ✅ Wyświetlanie listy produktów
- ✅ Filtrowanie produktów według kategorii
- ✅ Filtrowanie według typu produktu (popularny, najpopularniejszy)
- ✅ Szczegółowy widok produktu

### Koszyk Zakupów
- ✅ Dodawanie produktów do koszyka
- ✅ Aktualizacja ilości produktów
- ✅ Usuwanie produktów z koszyka
- ✅ Wyświetlanie łącznej wartości koszyka
- ✅ Automatyczne przeliczanie sum częściowych

### Zamówienia
- ✅ Składanie zamówień
- ✅ Historia zamówień użytkownika
- ✅ Szczegółowy widok zamówienia
- ✅ Wyświetlanie produktów w zamówieniu
- ✅ Informacje o statusie zamówienia

### Profil Użytkownika
- ✅ Wyświetlanie informacji o użytkowniku
- ✅ Wylogowanie

## 🏗️ Architektura

### Technologie
- **.NET MAUI 8.0** - Framework aplikacji wieloplatformowych
- **C# 12.0** - Język programowania
- **.NET 8** - Platforma docelowa
- **Newtonsoft.Json** - Serializacja/deserializacja JSON
- **HttpClient** - Komunikacja z API

### Wzorce Projektowe
- **MVVM** (Model-View-ViewModel) - Separacja logiki od UI
- **Service Layer** - ApiService dla komunikacji z backendem
- **Data Binding** - Dwukierunkowe wiązanie danych
- **Command Pattern** - Obsługa interakcji użytkownika
- **Repository Pattern** - Abstrakcja dostępu do danych

### Struktura Projektu

## 📦 Zależności (NuGet Packages)

## 🔧 Wymagania Systemowe

### Dla Deweloperów
- **Visual Studio 2022** (wersja 17.8 lub nowsza)
- **.NET 8 SDK**
- **Workload .NET MAUI** zainstalowany w Visual Studio
- **Android SDK** (dla rozwoju na Androida)
- **Xcode** (dla rozwoju na iOS/macOS - tylko macOS)

### Dla Użytkowników Końcowych
- **Android**: 5.0 (API 21) lub nowszy
- **iOS**: 11.0 lub nowszy
- **Windows**: Windows 10 wersja 1809 lub nowsza
- **macOS**: 10.15 lub nowszy

## 🚀 Instalacja i Uruchomienie

### 1. Klonowanie Repozytorium

### 2. Konfiguracja Backend API
Przed uruchomieniem aplikacji, skonfiguruj URL API w pliku `AppSettings.cs`:

### 3. Przywracanie Pakietów NuGet

### 4. Uruchomienie Aplikacji

#### Dla Androida:dotnet build -t:Run -f net8.0-android
#### Dla iOS: dotnet build -t:Run -f net8.0-ios
#### Dla Windows: dotnet build -t:Run -f net8.0-windows
#### Dla macOS: dotnet build -t:Run -f net8.0-macos
## 🛠️ Kontrybucja

## 🔌 API Endpoints

Aplikacja komunikuje się z następującymi endpointami:

### Użytkownicy
- `POST /api/Users/registerUser` - Rejestracja użytkownika
- `POST /api/Users/loginUser` - Logowanie użytkownika

### Produkty
- `GET /api/Categories` - Pobieranie kategorii
- `GET /api/Products` - Pobieranie produktów (z filtrami)
- `GET /api/Products?categoryId={id}` - Produkty według kategorii

### Koszyk
- `GET /api/ShoppingCartItems?userId={id}` - Produkty w koszyku
- `POST /api/ShoppingCartItems?userId={id}` - Dodawanie do koszyka
- `PUT /api/ShoppingCartItems?productId={id}&userId={id}&action={action}` - Aktualizacja koszyka
- `DELETE /api/ShoppingCartItems?productId={id}&userId={id}` - Usuwanie z koszyka

### Zamówienia
- `POST /api/Orders` - Składanie zamówienia
- `GET /api/Orders/user/{userId}` - Historia zamówień użytkownika
- `GET /api/Orders/{orderId}` - Szczegóły zamówienia

## 🎨 Struktura Nawigacji

Aplikacja wykorzystuje nawigację opartą na zakładkach (TabBar):

1. **Home** 🏠 - Strona główna z kategoriami i produktami
2. **Koszyk** 🛒 - Zarządzanie koszykiem zakupów
3. **Zamówienia** 📦 - Historia zamówień
4. **Profil** 👤 - Informacje o użytkowniku

## 🔐 Bezpieczeństwo

- **JWT Token Authentication** - Bezpieczne uwierzytelnianie
- **Secure Storage** - Wykorzystanie `Preferences` do bezpiecznego przechowywania tokenów
- **HTTPS** - Szyfrowana komunikacja z API
- **Authorization Headers** - Tokeny Bearer w nagłówkach żądań

## 📱 Screenshots

### HomePage
Wyświetla kategorie produktów i produkty według typu (popularne, najpopularniejsze).

### CartPage
Zarządzanie produktami w koszyku z możliwością aktualizacji ilości i usuwania.

### OrdersHistoryPage
Lista wszystkich zamówień użytkownika z datami i sumami.

### OrderDetailPage
Szczegółowy widok pojedynczego zamówienia z listą produktów.

## 🛠️ Rozwój

### Dodawanie Nowych Funkcji
1. Stwórz nowy branch: `git checkout -b feature/nazwa-funkcji`
2. Wprowadź zmiany
3. Commit: `git commit -m 'Dodanie nowej funkcji'`
4. Push: `git push origin feature/nazwa-funkcji`
5. Stwórz Pull Request

### Konwencje Kodowania
- Używaj **PascalCase** dla nazw klas, metod i właściwości
- Używaj **camelCase** dla zmiennych lokalnych
- Async metody powinny kończyć się na `Async`
- Komentuj złożoną logikę biznesową
- Stosuj `try-catch` dla operacji sieciowych

## 🐛 Znane Problemy i Rozwiązania

### Problem z ładowaniem obrazków
Upewnij się, że `FullImageUrl` w modelach zawiera prawidłowy pełny URL:

### Problem z deserializacją JSON
Sprawdź, czy nazwy właściwości w atrybutach `[JsonProperty]` odpowiadają nazwom z API.

## 📝 Roadmap

### Planowane Funkcjonalności
- [ ] Obsługa płatności online
- [ ] Powiadomienia push o statusie zamówienia
- [ ] Oceny i recenzje produktów
- [ ] Wyszukiwarka produktów
- [ ] Filtrowanie produktów (cena, popularność)
- [ ] Lista życzeń
- [ ] Tryb offline z synchronizacją
- [ ] Obsługa wielu języków (i18n)
- [ ] Tryb ciemny (Dark Mode)
- [ ] Analityka użytkownika

## 👥 Wkład w Projekt

Wszelkie wkłady są mile widziane! Jeśli chcesz przyczynić się do rozwoju projektu:

1. Fork projektu
2. Stwórz branch z funkcją (`git checkout -b feature/AmazingFeature`)
3. Commit zmian (`git commit -m 'Add some AmazingFeature'`)
4. Push do brancha (`git push origin feature/AmazingFeature`)
5. Otwórz Pull Request

## 📄 Licencja

Ten projekt jest licencjonowany na licencji MIT - zobacz plik [LICENSE](LICENSE) dla szczegółów.

## 📧 Kontakt

**Autor Projektu**: Mlodak  (sysmed@sysmed.com.pl))

**Link do Projektu**: [https://github.com/Mlodak/MauiClient](https://github.com/Mlodak/MauiClient)

## 🙏 Podziękowania

- Microsoft za .NET MAUI
- Społeczność .NET za wsparcie i zasoby
- Newtonsoft.Json za świetną bibliotekę JSON
- CommunityToolkit.Maui za dodatkowe kontrolki i narzędzia

## 📚 Dodatkowe Zasoby

- [Dokumentacja .NET MAUI](https://learn.microsoft.com/en-us/dotnet/maui/)
- [.NET MAUI Community Toolkit](https://github.com/CommunityToolkit/Maui)
- [Newtonsoft.Json Documentation](https://www.newtonsoft.com/json/help/html/Introduction.htm)
- [REST API Best Practices](https://restfulapi.net/)

---

**Wersja**: 1.0.0  
**Data ostatniej aktualizacji**: Październik 2025  
**Status**: Aktywny rozwój 🚀