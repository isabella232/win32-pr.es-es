---
title: Identificador de formato/par de desplazamiento
description: La segunda parte de la secuencia del conjunto de propiedades contiene un identificador de formato/par de desplazamiento.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276ab4834ef6987f1e985f91b42d6c7203496f9db3836adaeca6b953b9a39a2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962039"
---
# <a name="format-identifieroffset-pair"></a>Identificador de formato/par de desplazamiento

La segunda parte de la secuencia del conjunto de propiedades contiene un identificador de formato/par de desplazamiento. FMTID es el nombre del conjunto de propiedades; identifica de forma única cómo interpretar el contenido de la sección siguiente. Offset es la distancia, en bytes, desde el inicio de la secuencia completa hasta donde comienza la sección.

La siguiente estructura es útil para controlar los pares de identificador de formato y desplazamiento.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




