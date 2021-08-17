---
title: Sugerencias de migración
description: Es importante tener en cuenta los cálculos de direcciones y la aritmética de punteros al portear el código a archivos de 64 Windows.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guía de programación de 64 Windows de programación de 64 Windows programación, sugerencias de migración
- sugerencias de migración de 64 bits Windows programación
- compatibilidad de 64 bits con Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743600"
---
# <a name="migration-tips"></a>Sugerencias de migración

Las dos áreas principales de preocupación al examinar el código para la compatibilidad de 64 bits son las siguientes:

-   Cálculos de direcciones
-   Aritmética de puntero

Por muchas razones, los desarrolladores han almacenado direcciones como **un valor ULONG.** Después de todo, en las Windows de 32 bits, una dirección, un puntero y un valor **ULONG** tienen una longitud total de 32 bits. Sin embargo, en las Windows de 64 bits, una dirección y **un ULONG** no tienen la misma longitud. Aunque **un ULONG** sigue siendo un valor de 32 bits, ahora todos los punteros son valores de 64 bits.

## <a name="in-this-section"></a>En esta sección

-   [Directrices generales de porte](general-porting-guidelines.md)
-   [Almacenamiento de un valor de 64 bits](storing-a-64-bit-value.md)
-   [Errores comunes del compilador](common-compiler-errors.md)
-   [Consideraciones adicionales](additional-considerations.md)

 

 




