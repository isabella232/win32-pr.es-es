---
title: Agregar un fragmento de información
description: Agregar un fragmento de información
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420181fd0da326ebf3ccc6f921e55161c2005d17c3f8713cd104481147b40f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145138"
---
# <a name="adding-an-information-chunk"></a>Agregar un fragmento de información

Si necesita incluir otra información en la aplicación además de audio y vídeo, puede crear fragmentos de información e insertarlos en un archivo de captura. Los fragmentos de información pueden contener varios tipos de información, incluidos los detalles de un aviso de copyright, la identificación del origen del vídeo o la información de control de tiempo externa. En el ejemplo siguiente se almacena información de control de tiempo externa en un código de tiempo SMPTE (Society of Motion Picture and Tv Engineers) en un fragmento de información y se agrega el fragmento a un archivo de captura mediante la macro [**capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




