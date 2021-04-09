---
title: Capturar datos
description: Capturar datos
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence (macro)
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076076"
---
# <a name="capturing-data"></a><span data-ttu-id="815a6-105">Capturar datos</span><span class="sxs-lookup"><span data-stu-id="815a6-105">Capturing Data</span></span>

<span data-ttu-id="815a6-106">En el ejemplo siguiente se usa la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) para iniciar la captura de vídeo y la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) para copiar los datos capturados del archivo de captura en el archivo NEWFILE.AVI.</span><span class="sxs-lookup"><span data-stu-id="815a6-106">The following example uses the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro to start video capture and the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro to copy the captured data from the capture file to the file NEWFILE.AVI.</span></span>


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a><span data-ttu-id="815a6-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="815a6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="815a6-108">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="815a6-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




