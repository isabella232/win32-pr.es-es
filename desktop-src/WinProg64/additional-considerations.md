---
title: Consideraciones adicionales
description: Al portear el código, tenga en cuenta los siguientes puntos.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- sugerencias de porte de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068309"
---
# <a name="additional-considerations"></a>Consideraciones adicionales

Al porte el código, tenga en cuenta los siguientes puntos:

- La siguiente suposición ya no es válida:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Sin embargo, el compilador de 64 bits define \_ WIN32 para la compatibilidad con versiones anteriores.

- La siguiente suposición ya no es válida:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   En este caso, la cláusula else puede representar \_ WIN32 \_ o WIN64.

- Tenga cuidado con la alineación del tipo de datos. La **macro TYPE \_ ALIGNMENT** devuelve los requisitos de alineación de un tipo de datos. Por ejemplo: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 en x86, 8 en procesador Intel Itanium `TYPE_ALIGNMENT( UCHAR )` == 1 en todas partes

    Por ejemplo, el código de kernel que actualmente tiene el siguiente aspecto:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    probablemente se debe cambiar a:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Las correcciones automáticas de excepciones de alineación en modo kernel están deshabilitadas para los sistemas Intel Itanium.

- Tenga cuidado con las operaciones NOT. Tenga en cuenta lo siguiente.

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    El problema es que ~(b–1) genera "0x0000 0000 xxxx xxxx" y no "0xFFFF FFFF xxxx xxxx". El compilador no lo detectará. Para corregirlo, cambie el código como se muestra a continuación:

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

    El resultado es inesperadamente grande. La regla es que si alguno de los operandos no tiene signo, el resultado es unsigned. En el ejemplo anterior, se convierte en un valor sin signo, dividido por b y el resultado se almacena en c. La conversión no implica ninguna manipulación numérica.

    Como otro ejemplo, tenga en cuenta lo siguiente:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    El problema surge porque x no tiene signo, lo que hace que toda la expresión no tenga signo. Esto funciona bien a menos que y sea negativo. En este caso, y se convierte en un valor sin signo, la expresión se evalúa con una precisión de 32 bits, se escala y se agrega a pVar1. Un número negativo de 32 bits sin signo se convierte en un gran número positivo de 64 bits, lo que da un resultado incorrecto. Para corregir este problema, declare x como un valor con firma o conéctelo explícitamente a **LONG** en la expresión.

- Tenga cuidado al realizar asignaciones de tamaño por lotes. Por ejemplo:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    El código siguiente es incorrecto porque el compilador completará la estructura con 4 bytes adicionales para realizar la alineación de 8 bytes:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    El código siguiente es correcto:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- No pase `(HANDLE)0xFFFFFFFF` a funciones como [**CreateFileMapping.**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) En su lugar, use **VALOR DE IDENTIFICADOR NO \_ \_ VÁLIDO.**
- Use los especificadores de formato adecuados al imprimir una cadena. Use %p para imprimir punteros en hexadecimal. Esta es la mejor opción para imprimir punteros. Microsoft Visual C++ admite %I para imprimir datos polimórficos. Visual C++ admite %I64 para imprimir valores de 64 bits.

 

 