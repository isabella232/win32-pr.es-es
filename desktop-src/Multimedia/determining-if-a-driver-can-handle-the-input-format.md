---
title: Determinar si un controlador puede controlar el formato de entrada
description: Determinar si un controlador puede controlar el formato de entrada
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Administrador de compresión de vídeo (VCM), formato de entrada
- VCM (administrador de compresión de vídeo), formato de entrada
- Macro ICDrawQuery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074250"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Determinar si un controlador puede controlar el formato de entrada

En el ejemplo siguiente se muestra cómo comprobar el formato de entrada con la macro [**ICDrawQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery)


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




