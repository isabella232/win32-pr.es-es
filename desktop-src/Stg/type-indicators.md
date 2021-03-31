---
title: Indicadores de tipo
description: Las propiedades reales siguen la tabla de identificadores de propiedad y los valores de conjunto de propiedades de pares de desplazamiento. Cada propiedad se almacena como DWORD, seguida del valor del tipo de datos.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078113"
---
# <a name="type-indicators"></a>Indicadores de tipo

Las propiedades reales siguen la tabla de identificadores de propiedad y los valores de conjunto de propiedades de pares de desplazamiento. Cada propiedad se almacena como **DWORD**, seguida del valor del tipo de datos.

Los indicadores de tipo y sus valores asociados se describen en la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Todos los pares de tipo/valor deben comenzar en un límite de 32 bits. Por lo tanto, los valores pueden ir seguidos de bytes null para alinear el par subsiguiente en un límite de 32 bits.

En el código de ejemplo siguiente se calcula el número de bytes necesarios para alinear en un límite de 32 bits, dado un recuento de bytes.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



Dentro de un vector de valores, cada repetición de un valor escalar simple menor que 32 bits debe alinearse con su alineación natural en lugar de con una alineación de 32 bits. En la práctica, esto solo es importante para los tipos **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** y **VT \_ bool** (que tienen alineación natural de un byte o dos bytes). Todos los demás tipos tienen una alineación natural de cuatro bytes. Algunos tipos, por ejemplo, **VT \_ R8**, tienen una alineación natural de 8 bytes, pero se almacenan como si tienen una alineación de cuatro bytes.

Un valor de propiedad con el indicador de tipo **VT \_ I2** \| **\_ VT** puede incluir:

-   Un recuento de elementos **DWORD** .
-   Secuencia de enteros de dos bytes empaquetados sin relleno nulo entre ellos.

> [!IMPORTANT]
> Los recuentos de 32 bits o los tipos de propiedad que se almacenan como parte de un elemento de propiedad de vector también deben estar alineados con 32 bits.

 

Un valor de propiedad de tipo identificador de tipo **VT \_ LPSTR** \| **\_ VT** puede incluir:

-   Un recuento de elementos **DWORD** (**DWORD** *cElems*).
-   Secuencia de cadenas (**Char** *rgch \[ \]*), cada una de ellas precedida de un **valor DWORD** de longitud y, posiblemente, un relleno null para redondear a un límite de 32 bits.

 

 