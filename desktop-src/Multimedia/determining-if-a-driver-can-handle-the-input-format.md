---
title: Determinar si un controlador puede controlar el formato de entrada
description: Determinar si un controlador puede controlar el formato de entrada
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- administrador de compresión de vídeo (VCM), formato de entrada
- VCM (administrador de compresión de vídeo), formato de entrada
- Macro ICDrawQuery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370388"
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



 

 




