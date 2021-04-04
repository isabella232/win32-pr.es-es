---
title: Diccionario de nombres para mostrar del conjunto de propiedades
description: Un diccionario de nombres para mostrar de propiedades permite que los usuarios del conjunto de propiedades adjunten significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792952"
---
# <a name="property-set-display-name-dictionary"></a>Diccionario de nombres para mostrar del conjunto de propiedades

Un diccionario de nombres para mostrar de propiedades permite que los usuarios del conjunto de propiedades adjunten significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.

## <a name="dictionary-structure"></a>Estructura del Diccionario

El diccionario contiene un recuento de las entradas de la lista, seguida de una lista de entradas del diccionario.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Estructura de entrada del Diccionario

Cada entrada del Diccionario de la lista es un par identificador/cadena de propiedad. La siguiente es una definición de pseudo estructura para una entrada de diccionario. Es una pseudo estructura porque el \[ \] miembro SZ tiene un tamaño variable.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Diccionario de ejemplo

El siguiente ejemplo de transferencia de datos de mercado de acciones podría incluir un nombre que se puede mostrar "cotización de bolsa" para todo el conjunto y "símbolo del indicador" para el símbolo del PID \_ . Si un conjunto de propiedades solo contiene un símbolo y el diccionario, la sección del conjunto de propiedades tendría un flujo de bytes similar al siguiente.

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

Tenga en cuenta los siguientes problemas relacionados con los diccionarios de conjuntos de propiedades:

-   El ID. de propiedad 0 no tiene un indicador de tipo. El tipo de datos **DWORD** que indica el recuento de entradas se encuentra en la posición del indicador de tipo.
-   El recuento de caracteres de la cadena *CCH* incluye el carácter cero que termina la cadena. Cuando la página de códigos de la propiedad establecida no es Unicode, este campo es realmente un recuento de **bytes** . En el caso de los conjuntos de propiedades con una versión de formato de 0, este recuento no puede superar 256. En el caso de los conjuntos de propiedades con una versión de formato de 1, este recuento puede ser tan grande como el permitido por el tamaño total del conjunto de propiedades.
-   El diccionario es opcional. No todos los nombres de las propiedades del conjunto deben aparecer en el diccionario. Por el contrario, no es necesario que todos los nombres del diccionario se correspondan con las propiedades del conjunto. El Diccionario debe omitir las entradas de las propiedades que se supone que las aplicaciones que manipulan el conjunto de propiedades reconocen universalmente. Normalmente, se omiten los nombres de los conjuntos de propiedades base para los estándares ampliamente aceptados, pero los conjuntos de propiedades de uso especial pueden incluir diccionarios para que los usen los exploradores.
-   Los nombres de propiedad del diccionario se almacenan en la página de códigos indicada por el [identificador de propiedad 1](/windows/desktop/Stg/reserved-property-identifiers). En las páginas de códigos ANSI, cada entrada del diccionario está alineada en bytes. Por lo tanto, no hay ningún espacio entre los nombres de propiedad con el identificador de propiedad 0. Este es el único caso en el que no es necesario que los valores de los tipos de datos **DWORD** (el identificador de propiedad y la longitud de la propiedad **DWORD** s) estén alineados en los límites de 32 bits. En las páginas Unicode, cada entrada del diccionario tiene una alineación de 32 bits.
-   Los nombres de propiedad que comienzan con los caracteres Unicode binarios 0x0001 a 0x001F se reservan para uso futuro.
-   El nombre de propiedad asociado a la propiedad ID 0 representa el nombre del conjunto completo de propiedades.

 

 