---
title: Encabezado de conjunto de propiedades
description: Al principio de la secuencia del conjunto de propiedades es un encabezado. Consta de un indicador de orden de bytes, una versión de formato, la versión del sistema operativo original, el identificador de clase (CLSID) y un campo reservado.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Almacenamiento estructurado de encabezado de conjunto de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357785"
---
# <a name="property-set-header"></a>Encabezado de conjunto de propiedades

Al principio de la secuencia del conjunto de propiedades es un encabezado. Consta de un indicador de orden de bytes, una versión de formato, la versión del sistema operativo original, el identificador de clase (CLSID) y un campo reservado.

La pseudo estructura siguiente ilustra el encabezado.

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




