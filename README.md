# Spawn.Technology.RandomDataGenerator
English Description:

Spawn.Technology.RandomDataGenerator is a lightweight and easy-to-use library for generating random personal data. It provides a set of utilities to create random names, emails, phone numbers, street addresses, cities, postal codes, birth dates, and more. This package is highly customizable, allowing you to specify parameters (like gender, age range, etc.) or generate fully random values with default settings.

Whether you're developing test data for your application, working on data anonymization, or creating randomized content for any purpose, Spawn.Technology.RandomDataGenerator makes it quick and easy to generate realistic fake data on the fly.

Key Features:
Generate random first and last names (with optional gender parameter).
Create random email addresses (with or without specified name).
Generate phone numbers with customizable country code.
Randomly generate age, birth date, and street addresses.
Generate random cities, countries, and postal codes.
Fully customizable with optional parameters or full randomization.

Use Cases:
Generating test data for applications.
Creating fake user profiles for testing.
Anonymizing data for privacy protection.
Quickly populating forms with random data.




Russian Description:

Spawn.Technology.RandomDataGenerator — это легковесная и простая в использовании библиотека для генерации случайных личных данных. Она предоставляет набор утилит для создания случайных имен, электронных адресов, номеров телефонов, уличных адресов, городов, почтовых кодов, дат рождения и многого другого. Пакет имеет высокую степень настройки, позволяя задавать параметры (например, пол, диапазон возрастов и т.д.) или генерировать полностью случайные значения с использованием настроек по умолчанию.

Будь то создание тестовых данных для вашего приложения, работа с анонимизацией данных или генерация случайного контента для любых целей, Spawn.Technology.RandomDataGenerator позволяет быстро и легко генерировать реалистичные фальшивые данные.

Основные особенности:
Генерация случайных имен и фамилий (с опциональным параметром пола).
Создание случайных электронных адресов (с указанным или без имени).
Генерация номеров телефонов с настраиваемым кодом страны.
Случайная генерация возраста, даты рождения и уличных адресов.
Генерация случайных городов, стран и почтовых кодов.
Полная настройка с возможностью использования параметров или полной рандомизации.

Применение:
Генерация тестовых данных для приложений.
Создание фальшивых профилей пользователей для тестирования.
Анонимизация данных для защиты конфиденциальности.
Быстрое заполнение форм случайными данными.





Demos:

```
using System;
using RandomDataGenerator;

namespace Lesson
{
    public class Program
    {
        public static void Main()
        {
            // Пример 1: Генерация случайных данных (все по умолчанию)
            // Example 1: Generating random data (default values)
            Console.WriteLine("Пример 1: Генерация случайных данных");
            var name1 = RandomDataGenerator.RandomDataGenerator.GenerateName();
            var age1 = RandomDataGenerator.RandomDataGenerator.GenerateAge();
            var birthDate1 = RandomDataGenerator.RandomDataGenerator.GenerateBirthDate();
            Console.WriteLine($"Name: {name1}, Age: {age1}, Birth Date: {birthDate1.ToShortDateString()}");

            // Пример 2: Генерация данных с заданными параметрами
            // Example 2: Generating data with specified parameters
            Console.WriteLine("\nПример 2: Генерация данных с параметрами");
            var name2 = RandomDataGenerator.RandomDataGenerator.GenerateName(isMale: true); // Мужское имя
            // Male name
            var age2 = RandomDataGenerator.RandomDataGenerator.GenerateAge(minAge: 25, maxAge: 40); // Возраст от 25 до 40 лет
            // Age between 25 and 40
            var birthDate2 = RandomDataGenerator.RandomDataGenerator.GenerateBirthDate(minAge: 25, maxAge: 40);
            Console.WriteLine($"Name: {name2}, Age: {age2}, Birth Date: {birthDate2.ToShortDateString()}");

            // Пример 3: Генерация случайной почты с указанным именем
            // Example 3: Generating a random email with a specified name
            Console.WriteLine("\nПример 3: Генерация email для имени 'JohnDoe'");
            var email = RandomDataGenerator.RandomDataGenerator.GenerateEmail("JohnDoe");
            Console.WriteLine($"Email: {email}");

            // Пример 4: Генерация случайной почты без указания имени
            // Example 4: Generating a random email without specifying a name
            Console.WriteLine("\nПример 4: Генерация случайного email");
            var randomEmail = RandomDataGenerator.RandomDataGenerator.GenerateEmail();
            Console.WriteLine($"Random Email: {randomEmail}");

            // Пример 5: Генерация случайного номера телефона (по умолчанию для США)
            // Example 5: Generating a random phone number (default for the USA)
            Console.WriteLine("\nПример 5: Генерация номера телефона для США");
            var phoneNumber = RandomDataGenerator.RandomDataGenerator.GeneratePhoneNumber();
            Console.WriteLine($"Phone Number: {phoneNumber}");

            // Пример 6: Генерация случайного номера телефона для другой страны
            // Example 6: Generating a random phone number for a different country
            Console.WriteLine("\nПример 6: Генерация номера телефона для Канаде");
            var phoneNumberCanada = RandomDataGenerator.RandomDataGenerator.GeneratePhoneNumber("+1");
            Console.WriteLine($"Phone Number (Canada): {phoneNumberCanada}");

            // Пример 7: Генерация случайного адреса и города с параметрами
            // Example 7: Generating a random address and city with specified parameters
            Console.WriteLine("\nПример 7: Генерация адреса и города с параметрами");
            var streetAddress = RandomDataGenerator.RandomDataGenerator.GenerateStreetAddress("Sunset Blvd");
            var city = RandomDataGenerator.RandomDataGenerator.GenerateCity("Los Angeles");
            var postalCode = RandomDataGenerator.RandomDataGenerator.GeneratePostalCode();
            var country = RandomDataGenerator.RandomDataGenerator.GenerateCountry("USA");
            Console.WriteLine($"Address: {streetAddress}, City: {city}, Postal Code: {postalCode}, Country: {country}");

            // Пример 8: Генерация случайного адреса и города без параметров
            // Example 8: Generating a random address and city without specifying parameters
            Console.WriteLine("\nПример 8: Генерация случайного адреса и города");
            var randomStreetAddress = RandomDataGenerator.RandomDataGenerator.GenerateStreetAddress();
            var randomCity = RandomDataGenerator.RandomDataGenerator.GenerateCity();
            var randomPostalCode = RandomDataGenerator.RandomDataGenerator.GeneratePostalCode();
            var randomCountry = RandomDataGenerator.RandomDataGenerator.GenerateCountry();
            Console.WriteLine($"Address: {randomStreetAddress}, City: {randomCity}, Postal Code: {randomPostalCode}, Country: {randomCountry}");
        }
    }
}
```
