---
title: Encabezado del conjunto de propiedades
description: Al principio de la secuencia del conjunto de propiedades hay un encabezado . Consta de un indicador de orden de bytes, una versión de formato, la versión del sistema operativo de origen, el identificador de clase (CLSID) y un campo reservado.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Propiedad Set Header Structured Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662225"
---
# <a name="property-set-header"></a>Encabezado del conjunto de propiedades

Al principio de la secuencia del conjunto de propiedades hay un encabezado . Consta de un indicador de orden de bytes, una versión de formato, la versión del sistema operativo de origen, el identificador de clase (CLSID) y un campo reservado.

En la pseudoestrucción siguiente se muestra el encabezado .

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

 

 




