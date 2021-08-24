---
title: Sección
description: La sección es la tercera parte de la secuencia del conjunto de propiedades y contiene los valores reales del conjunto de propiedades.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682805"
---
# <a name="section"></a>Sección

La sección es la tercera parte de la secuencia del conjunto de propiedades y contiene los valores reales del conjunto de propiedades.

Una sección contiene:

-   Recuento de bytes de la sección que incluye el propio recuento de bytes.
-   Matriz de pares de id. de propiedad y desplazamiento de 32 bits.
-   Matriz de pares de valores/indicadores de tipo de propiedad.

Los desplazamientos son la distancia desde el inicio de la sección hasta el inicio del par de propiedad (tipo, valor). Esto permite copiar una sección como una matriz de bytes sin ninguna traducción de la estructura interna.

Las pseudoes estructuras siguientes ilustran el formato de una sección.

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




