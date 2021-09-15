---
title: Indicadores de tipo
description: Las propiedades reales siguen la tabla de valores de conjunto de propiedades Identificadores de propiedad/Pares de desplazamiento. Cada propiedad se almacena como DWORD, seguida del valor del tipo de datos.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270524"
---
# <a name="type-indicators"></a>Indicadores de tipo

Las propiedades reales siguen la tabla de valores de conjunto de propiedades Identificadores de propiedad/Pares de desplazamiento. Cada propiedad se almacena como **DWORD,** seguido del valor del tipo de datos.

Los indicadores de tipo y sus valores asociados se describen en la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Todos los pares tipo-valor deben comenzar en un límite de 32 bits. Por lo tanto, los valores se pueden seguir con bytes null para alinear el par posterior en un límite de 32 bits.

El código de ejemplo siguiente calcula cuántos bytes se necesitan para alinearse en un límite de 32 bits, dado un recuento de bytes.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



Dentro de un vector de valores, cada repetición de un valor escalar simple menor que 32 bits debe alinearse con su alineación natural en lugar de con una alineación de 32 bits. En la práctica, esto solo es significativo para los tipos **VT \_ UI1,** **VT \_ UI2,** **VT \_ I2** y **VT \_ BOOL** (que tienen alineación natural de un byte o dos bytes). Todos los demás tipos tienen una alineación natural de cuatro bytes. Algunos tipos, por ejemplo, **VT \_ R8,** realmente tienen una alineación natural de 8 bytes, pero se almacenan como si hubieran una alineación de cuatro bytes.

Un valor de propiedad con el indicador **de tipo VT \_ I2** \| **VT \_ VECTOR** incluiría:

-   Recuento **de elementos DWORD.**
-   Secuencia de enteros empaquetados de dos bytes sin relleno nulo entre ellos.

> [!IMPORTANT]
> Los recuentos de 32 bits o los tipos de propiedad que se almacenan como parte de un elemento de propiedad vectorial también deben estar alineados de 32 bits.

 

Un valor de propiedad del identificador de **tipo VT \_ LPSTR** \| **VT \_ VECTOR** incluiría:

-   Un **recuento de elementos DWORD** (**DWORD** *cElems*).
-   Secuencia de cadenas **(char** *\[ \] rgch),* cada una precedida de un **DWORD** de recuento de longitudes y, posiblemente, seguida de relleno nulo para redondear a un límite de 32 bits.

 

 