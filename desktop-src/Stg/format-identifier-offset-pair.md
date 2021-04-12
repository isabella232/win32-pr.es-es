---
title: Par de identificador de formato/desplazamiento
description: La segunda parte de la secuencia del conjunto de propiedades contiene un par de identificador de formato/desplazamiento.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356988"
---
# <a name="format-identifieroffset-pair"></a><span data-ttu-id="ee1b6-103">Par de identificador de formato/desplazamiento</span><span class="sxs-lookup"><span data-stu-id="ee1b6-103">Format Identifier/Offset Pair</span></span>

<span data-ttu-id="ee1b6-104">La segunda parte de la secuencia del conjunto de propiedades contiene un par de identificador de formato/desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ee1b6-104">The second part of the property set stream contains one Format Identifier/Offset Pair.</span></span> <span data-ttu-id="ee1b6-105">FMTID es el nombre del conjunto de propiedades. identifica de forma única cómo interpretar el contenido de la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="ee1b6-105">The FMTID is the name of the property set; it uniquely identifies how to interpret the contents of the following section.</span></span> <span data-ttu-id="ee1b6-106">El desplazamiento es la distancia, en bytes, desde el inicio de la secuencia completa hasta el punto en que comienza la sección.</span><span class="sxs-lookup"><span data-stu-id="ee1b6-106">The Offset is the distance, in bytes, from the start of the whole stream to where the section begins.</span></span>

<span data-ttu-id="ee1b6-107">La estructura siguiente es útil para controlar los pares de identificador de formato/desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ee1b6-107">The following structure is helpful in handling Format Identifier/Offset Pairs.</span></span>

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




