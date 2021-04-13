---
title: Adición de un fragmento de información
description: Adición de un fragmento de información
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268919"
---
# <a name="adding-an-information-chunk"></a><span data-ttu-id="47696-104">Adición de un fragmento de información</span><span class="sxs-lookup"><span data-stu-id="47696-104">Adding an Information Chunk</span></span>

<span data-ttu-id="47696-105">Si necesita incluir otra información en la aplicación además de audio y vídeo, puede crear fragmentos de información e insertarlos en un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="47696-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="47696-106">Los fragmentos de información pueden contener varios tipos de información, como los detalles de un aviso de propiedad intelectual, la identificación de la fuente de vídeo o la información de tiempo externa.</span><span class="sxs-lookup"><span data-stu-id="47696-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="47696-107">En el ejemplo siguiente se almacena la información de temporización externa en el código de tiempo de SMPTE (sociedad de los ingenieros de películas y televisión) en un fragmento de información y se agrega el fragmento a un archivo de captura mediante la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="47696-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a><span data-ttu-id="47696-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47696-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47696-109">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="47696-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




