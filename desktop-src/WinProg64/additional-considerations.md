---
title: Consideraciones adicionales
description: Al migrar el código, tenga en cuenta los siguientes puntos.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Sugerencias de portabilidad 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105708129"
---
# <a name="additional-considerations"></a>Consideraciones adicionales

Al migrar el código, tenga en cuenta los siguientes puntos:

- La hipótesis siguiente ya no es válida:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Sin embargo, el compilador de 64 bits define \_ Win32 para la compatibilidad con versiones anteriores.

- La hipótesis siguiente ya no es válida:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   En este caso, la cláusula else puede representar \_ Win32 o \_ WIN64.

- Tenga cuidado con la alineación de tipo de datos. La macro de **\_ alineación de tipos** devuelve los requisitos de alineación de un tipo de datos. Por ejemplo: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 en x86, 8 en procesador Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 Everywhere

    Por ejemplo, el código de kernel tiene el siguiente aspecto:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    probablemente se debe cambiar a:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Las correcciones automáticas de las excepciones de alineación del modo kernel están deshabilitadas para los sistemas Intel Itanium.

- Tenga cuidado con las operaciones NOT. Tenga en cuenta lo siguiente.

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    El problema es que ~ (b – 1) genera "0x0000 0000 XXXX XXXX" y no "0xFFFF FFFF XXXX XXXX". El compilador no lo detectará. Para solucionarlo, cambie el código de la siguiente manera:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Tenga cuidado al realizar operaciones sin firmar y firmadas. Tenga en cuenta lo siguiente.

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    El resultado es inesperadamente grande. La regla es que si alguno de los operandos es sin signo, el resultado es sin signo. En el ejemplo anterior, un se convierte en un valor sin signo, dividido por b, y el resultado almacenado en c. La conversión no implica ninguna manipulación numérica.

    Como otro ejemplo, tenga en cuenta lo siguiente:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    El problema surge porque x es sin signo, lo que hace que toda la expresión quede sin signo. Esto funciona bien a menos que y sea negativo. En este caso, y se convierte en un valor sin signo, la expresión se evalúa usando la precisión de 32 bits, escalada y se agrega a pVar1. Un número negativo sin signo de 32 bits se convierte en un número positivo de 64 bits grande, lo que da lugar a un resultado incorrecto. Para solucionar este problema, declare x como un valor con signo o convierta explícitamente a **Long** en la expresión.

- Tenga cuidado al realizar asignaciones de tamaño por etapas. Por ejemplo:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    El código siguiente es incorrecto porque el compilador rellenará la estructura con 4 bytes adicionales para establecer la alineación de 8 bytes:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    El código siguiente es correcto:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- No pase `(HANDLE)0xFFFFFFFF` a funciones como [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga). En su lugar, use un **\_ \_ valor de identificador no válido**.
- Use los especificadores de formato adecuados al imprimir una cadena. Use% p para imprimir punteros en formato hexadecimal. Esta es la mejor opción para los punteros de impresión. Microsoft Visual C++ admite% I para imprimir datos polimórficos. Visual C++ también admite% I64 para imprimir valores de 64 bits.

 

 