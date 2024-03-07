# TurboCache - High-Performance Cache Extension for PHP

## Description

TurboCache is a high-performance cache extension for PHP that aims to dramatically improve the speed and efficiency of caching operations. Built with performance in mind, TurboCache is written in C to leverage low-level optimizations and deliver lightning-fast caching capabilities.

## Key Features

- **Exceptional Speed**: TurboCache provides caching speeds that are 400+ times faster than traditional caching solutions like Memcached, Reddis.
- **Efficient Resource Utilization**: TurboCache optimizes resource utilization, ensuring maximum efficiency while minimizing memory overhead.
- **Low-Level Optimizations**: Leveraging the power of C, TurboCache incorporates various low-level optimizations for superior performance.
- **Seamless Integration**: TurboCache seamlessly integrates into existing PHP applications, offering an easy and straightforward caching solution.
- **Simple Usage**: TurboCache offers a simple and intuitive API, making it easy to use for developers. Example usage includes:
   - `turbo_set('group_key', 'key', $value);` - Sets a value in the cache.
   - `turbo_get('key');` - Retrieves a value from the cache.
   - `turbo_get_part('key');` - Retrieves a part value from the cache.
   - `turbo_get_touch('key');` - 
   - `turbo_size('key');` - 
   - `turbo_get_size_array($array);` - 
   - `turbo_reset();` - 
   - `turbo_hash('key');` - 
   - `turbo_stats();` - 
   - `turbo_show_hex($string);` - 
   - `turbo_serialize($array);` - 
   - `turbo_unserialize($serialize_string);` - 
   - `turbo_compress($string);` - lz4
   - `turbo_uncompress($compressed_string);` - lz4
     
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
  - TurboCache: 2.9 milliseconds
  - Difference: 416 times

# TurboCache - Высокопроизводительное расширение кэша для PHP

## Описание

TurboCache - это высокопроизводительное расширение кэша для PHP, которое стремится драматически улучшить скорость и эффективность операций кэширования. Разработанный с учетом производительности, TurboCache написан на языке C, чтобы использовать низкоуровневые оптимизации и обеспечить молниеносные возможности кэширования.

## Основные особенности

- **Исключительная скорость**: TurboCache обеспечивает скорость кэширования, превышающую в 400 и более раз традиционные решения кэширования, такие как Memcached, Reddis.
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
    
- **Время чтения**:
  - Memcached: 1206.98 миллисекунд
  - TurboCache: 2.9 миллисекунд
  - Разница: 416 раз
 
## Скорость
Встроенные функции turbo_serialize и turbo_unserialize высочайшая скорость и сжатие данных.

**Маленький массив 1 000 000 итераций**
- **Время записи, миллисекунд**:
  - turbo_serialize 48
  - php serialize 78 -62%
  - json_encode 79 -64%
  - igbinary_serialize 116 -141%
   
- **Время чтения, миллисекунд**:
  - turbo_unserialize 80
  - php unserialize 117 -46%
  - igbinary_unserialize 135 -68%
  - json_decode 217 -171%

**Небольшой массив 1 000 000 итераций**
- **Время записи, миллисекунд**:
  - turbo_serialize 473
  - php serialize 668 -41%
  - igbinary_serialize 1101 -132%
  - json_encode 1459 -208%
   
- **Время чтения, миллисекунд**:
  - turbo_unserialize 764
  - igbinary_unserialize 1010 -32%
  - php unserialize 1211 -58%
  - json_decode 3860 -407%

**Большой массив(24.9 MB) 100 итераций**
https://github.com/json-iterator/test-data/blob/master/large-file.json

- **Время записи, миллисекунд**:
  - turbo_serialize 1753
  - igbinary_serialize 2948 -68%
  - php serialize 3264 -86%
  - turbo_compress(turbo_serialize($arr)) 4279 -144% 6.43 MB copress ratio 3.872
  - json_encode 4458 -154%
    
- **Время чтения, миллисекунд**:
  - turbo_unserialize 2170
  - igbinary_unserialize 2760 -27%
  - php unserialize 2928 -34%
  - turbo_unserialize(turbo_uncompress($tx)) 2945 -35%
  - simdjson 3871 -78%
  - json_decode 7487 -245%

## Размер, байт
  - turbo_serialize 966
  - igbinary_serialize 1003 -4%
  - json_encode 1096 -12%
  - php serialize 1448 -50%

## Скорость
Встроенные функции turbo_hash 32 бита высочайшая скорость.
  - turbo_hash 30
  - crc32 45 -50%
  - xxh3 75 -150%
  - md5 100 -233%

