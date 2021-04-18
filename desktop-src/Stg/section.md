---
title: Sección
description: La sección es la tercera parte de la secuencia del conjunto de propiedades y contiene los valores reales del conjunto de propiedades.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665645"
---
# <a name="section"></a>Sección

La sección es la tercera parte de la secuencia del conjunto de propiedades y contiene los valores reales del conjunto de propiedades.

Una sección contiene:

-   Recuento de bytes para la sección, que incluye el recuento de bytes.
-   Matriz de pares de identificador y desplazamiento de propiedad de 32 bits.
-   Matriz de pares de valor/indicadores de tipo de propiedad.

Los desplazamientos son la distancia desde el inicio de la sección hasta el inicio del par de propiedad (tipo, valor). Esto permite que una sección se copie como una matriz de bytes sin ninguna traducción de la estructura interna.

Las siguientes pseudo-estructuras muestran el formato de una sección.

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

 

 




