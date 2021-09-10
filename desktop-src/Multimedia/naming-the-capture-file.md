---
title: Asignar un nombre al archivo de captura
description: Asignar un nombre al archivo de captura
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- CapFileSetCaptureFile macro
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371378"
---
# <a name="naming-the-capture-file"></a>Asignar un nombre al archivo de captura

En el ejemplo siguiente se usa la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) para especificar un nombre de archivo alternativo (MYCAP.AVI) para el archivo de captura y la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) para preasignar un archivo de 5 MB.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




