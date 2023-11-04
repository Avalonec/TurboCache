# TurboCache - High-Performance Cache Extension for PHP

## Description

TurboCache is a high-performance cache extension for PHP that aims to dramatically improve the speed and efficiency of caching operations. Built with performance in mind, TurboCache is written in C to leverage low-level optimizations and deliver lightning-fast caching capabilities.

## Key Features

- **Exceptional Speed**: TurboCache provides caching speeds that are 100+ times faster than traditional caching solutions like Memcached, Reddis.
- **Efficient Resource Utilization**: TurboCache optimizes resource utilization, ensuring maximum efficiency while minimizing memory overhead.
- **Low-Level Optimizations**: Leveraging the power of C, TurboCache incorporates various low-level optimizations for superior performance.
- **Seamless Integration**: TurboCache seamlessly integrates into existing PHP applications, offering an easy and straightforward caching solution.
- **Simple Usage**: TurboCache offers a simple and intuitive API, making it easy to use for developers. Example usage includes:
   - `turbo_set('key', $value);` - Sets a value in the cache.
   - `turbo_get('key');` - Retrieves a value from the cache.

## Test Procedure
The testing involved creating and retrieving 10 variables in a loop of 10,000 iterations.

## Test Results

The performance test results show significant improvements with TurboCache compared to Memcached:

- **Write Time**:
  - Memcached: 1010.32 milliseconds
  - TurboCache: 3.78 milliseconds
  - Difference: 267 times

- **Read Time**:
  - Memcached: 1206.98 milliseconds
  - TurboCache: 4.19 milliseconds
  - Difference: 287 times

# TurboCache - Высокопроизводительное расширение кэша для PHP

## Описание

TurboCache - это высокопроизводительное расширение кэша для PHP, которое стремится драматически улучшить скорость и эффективность операций кэширования. Разработанный с учетом производительности, TurboCache написан на языке C, чтобы использовать низкоуровневые оптимизации и обеспечить молниеносные возможности кэширования.

## Основные особенности

- **Исключительная скорость**: TurboCache обеспечивает скорость кэширования, превышающую в 100 и более раз традиционные решения кэширования, такие как Memcached, Reddis.
- **Эффективное использование ресурсов**: TurboCache оптимизирует использование ресурсов, обеспечивая максимальную эффективность при минимальном использовании памяти.
- **Низкоуровневые оптимизации**: Используя мощь языка C, TurboCache включает различные низкоуровневые оптимизации для высокой производительности.
- **Безшовная интеграция**: TurboCache легко интегрируется в существующие приложения на PHP, предлагая простое и понятное решение для кэширования.
- **Простое использование**: TurboCache предлагает простой и интуитивно понятный API, что делает его легким в использовании для разработчиков. Примеры использования включают:
   - `turbo_set('key', $value);` - Устанавливает значение в кэше.
   - `turbo_get('key');` - Извлекает значение из кэша.

## Процедура тестирования
Тестирование включало создание и извлечение 10 переменных в цикле из 10 000 итераций.

## Результаты тестирования

Результаты тестирования производительности показывают значительное улучшение с использованием TurboCache по сравнению с Memcached:

- **Время записи**:
  - Memcached: 1010.32 миллисекунд
  - TurboCache: 3.78 миллисекунд
  - Разница: 267 раз
  - 
- **Время чтения**:
  - Memcached: 1206.98 миллисекунд
  - TurboCache: 4.19 миллисекунд
  - Разница: 287 раз

  Тестирование включало создание и извлечение 10 переменных в цикл из 10 000 000 итераций.
- TurboCache: 8.19 миллисекунд