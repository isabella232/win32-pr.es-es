---
title: Sugerencias de migración
description: Es importante tener en cuenta los cálculos de direcciones y la aritmética de punteros al trasladar el código a Windows de 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, sugerencias de migración
- sugerencias para la migración de 64 bits programación de Windows
- compatibilidad con la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777245"
---
# <a name="migration-tips"></a>Sugerencias de migración

Las dos áreas principales de preocupación al examinar el código para la compatibilidad con 64 bits son las siguientes:

-   Cálculos de direcciones
-   Aritmética de puntero

Por muchas razones, los desarrolladores han almacenado direcciones como un valor **ULong** . Después de todo, en Windows de 32 bits, una dirección, un puntero y un valor **ULong** tienen una longitud de 32 bits. Sin embargo, en Windows de 64 bits, una dirección y un **ULong** no tienen la misma longitud. Mientras que **ULong** sigue siendo un valor de 32 bits, todos los punteros son ahora valores de 64 bits.

## <a name="in-this-section"></a>En esta sección

-   [Instrucciones generales de portabilidad](general-porting-guidelines.md)
-   [Almacenar un valor de 64 bits](storing-a-64-bit-value.md)
-   [Errores comunes del compilador](common-compiler-errors.md)
-   [Consideraciones adicionales](additional-considerations.md)

 

 




