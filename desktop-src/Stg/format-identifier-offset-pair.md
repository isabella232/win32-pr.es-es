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
# <a name="format-identifieroffset-pair"></a>Par de identificador de formato/desplazamiento

La segunda parte de la secuencia del conjunto de propiedades contiene un par de identificador de formato/desplazamiento. FMTID es el nombre del conjunto de propiedades. identifica de forma única cómo interpretar el contenido de la sección siguiente. El desplazamiento es la distancia, en bytes, desde el inicio de la secuencia completa hasta el punto en que comienza la sección.

La estructura siguiente es útil para controlar los pares de identificador de formato/desplazamiento.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




