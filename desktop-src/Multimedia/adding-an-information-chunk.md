---
title: Agregar un fragmento de información
description: Agregar un fragmento de información
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063017"
---
# <a name="adding-an-information-chunk"></a>Agregar un fragmento de información

Si necesita incluir otra información en la aplicación además de audio y vídeo, puede crear fragmentos de información e insertarlos en un archivo de captura. Los fragmentos de información pueden contener varios tipos de información, incluidos los detalles de un aviso de copyright, la identificación del origen del vídeo o la información de control de tiempo externa. En el ejemplo siguiente se almacena información de control de tiempo externa un código de tiempo de SMPTE (Society of Motion Picture and Tv Engineers) en un fragmento de información y se agrega el fragmento a un archivo de captura mediante la macro [**capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


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

 

 




