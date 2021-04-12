---
title: Asignar nombre al archivo de captura
description: Asignar nombre al archivo de captura
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile (macro)
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357275"
---
# <a name="naming-the-capture-file"></a><span data-ttu-id="89aa0-105">Asignar nombre al archivo de captura</span><span class="sxs-lookup"><span data-stu-id="89aa0-105">Naming the Capture File</span></span>

<span data-ttu-id="89aa0-106">En el ejemplo siguiente se usa la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) para especificar un nombre de archivo alternativo (MYCAP.AVI) para el archivo de captura y la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) para asignar previamente un archivo de 5 MB.</span><span class="sxs-lookup"><span data-stu-id="89aa0-106">The following example uses the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro to specify an alternate filename (MYCAP.AVI) for the capture file and the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro to preallocate a file of 5 MB.</span></span>


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="89aa0-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89aa0-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89aa0-108">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="89aa0-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




