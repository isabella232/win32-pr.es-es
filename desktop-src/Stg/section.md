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
# <a name="section"></a><span data-ttu-id="15359-103">Sección</span><span class="sxs-lookup"><span data-stu-id="15359-103">Section</span></span>

<span data-ttu-id="15359-104">La sección es la tercera parte de la secuencia del conjunto de propiedades y contiene los valores reales del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="15359-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="15359-105">Una sección contiene:</span><span class="sxs-lookup"><span data-stu-id="15359-105">A section contains:</span></span>

-   <span data-ttu-id="15359-106">Recuento de bytes para la sección, que incluye el recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="15359-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="15359-107">Matriz de pares de identificador y desplazamiento de propiedad de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="15359-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="15359-108">Matriz de pares de valor/indicadores de tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="15359-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="15359-109">Los desplazamientos son la distancia desde el inicio de la sección hasta el inicio del par de propiedad (tipo, valor).</span><span class="sxs-lookup"><span data-stu-id="15359-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="15359-110">Esto permite que una sección se copie como una matriz de bytes sin ninguna traducción de la estructura interna.</span><span class="sxs-lookup"><span data-stu-id="15359-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="15359-111">Las siguientes pseudo-estructuras muestran el formato de una sección.</span><span class="sxs-lookup"><span data-stu-id="15359-111">The following pseudo-structures illustrate the format of a section.</span></span>

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

 

 




