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
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497295"
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



 

 




