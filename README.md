# Introducción-a-Php-uso-de-funciones

## Número capicúa (palíndromo numérico)

Implementa una función __esCapicua(int $n): bool__ que determine si un número entero positivo es capicúa.

- Un número es capicúa si se lee igual de izquierda a derecha que de derecha a izquierda.

> Ejemplo: `12321` → `true`

```php
<?php 
    declare(strict_types=1);
    function esCapicua(int $n): bool {
        $numeroOriginal = $n; 
        $invertido = 0;
        while ($n > 0) {
            $digito = $n % 10; 
            $invertido = $invertido * 10 + $digito; 
            $n = intdiv($n, 10);
        }
        if ($numeroOriginal == $invertido) {
            return true;
        }
        return false;
    }
    echo esCapicua(12321);
?>
```

![alt text](./img/001.png)

## Escalera de asteriscos

Implementa una función __montañaAsteriscos(int $n, $m): void__ que imprima una escalera de asteriscos de altura `N`y el tamaño M.

- La primera fila contiene 1 asterisco, la segunda 2, y así hasta `N`, `M` veces.

> Ejemplo con entrada `4,2`:

```text
*.     *
**.   **
***  ***
********
```

```php
<?php
    // SIN TERMINAR
    declare( strict_type=1);
    function montañaAsteriscos(int $n, int $m) {
        for ($i = 1; $i <= $n; $i++) {
        echo str_repeat("*", $i);
        echo "<br>";
        }
    }
    echo montañaAsteriscos(4,2);
?>
```

## Suma de dígitos

Implementa una función __sumaDigitos(int $n): int__ que calcule la suma de los dígitos de un número entero positivo.

- Descompón el número en dígitos y súmalos.

> Ejemplo: `2025` → `9` (2+0+2+5)

```php
<?php

?>
```

## Número secreto (múltiplos de 3 o 5)

Implementa una función __multiplosTresOCinco(int $n): array__ que devuelva todos los múltiplos de 3 o 5 menores que `N`.

- Además, calcula la suma de dichos múltiplos.

> Ejemplo con entrada `10`:

```code
3, 5, 6, 9
Suma = 23
```

```php
<?php

?>
```

## Secuencia de Collatz

Implementa una función __secuenciaCollatz(int $n): array__ que genere la secuencia de Collatz a partir de un entero positivo.

- Si el número es par → dividir entre 2.  
- Si es impar → multiplicar por 3 y sumar 1.  
- Repetir hasta llegar a 1.

> Ejemplo con entrada `6`:

```code
6 → 3 → 10 → 5 → 16 → 8 → 4 → 2 → 1
```

```php
<?php
// SIN TERMINAR
    declare( strict_type=1);
    function secuenciaCollatz(int $n) : array {
        $finalSecuencia = false;
        while (!$finalSecuencia) {
            
        }
    }
    echo secuenciaCollatz(10);
?>
```

---