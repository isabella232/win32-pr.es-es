---
description: Interfaces de codificación y codificación de archivos
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces de codificación y codificación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255176"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfaces de codificación y codificación de archivos

Estas interfaces admiten la codificación y la codificación de archivos.



| Interfaz                                                    | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recuperar metadatos de una secuencia, como el autor y el título.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determine el progreso de una operación de apertura de archivos.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Consultar y establecer la hora de análisis de la posición actual en una secuencia MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controlar qué flujos lógicos se reproducen y recuperar información sobre ellos.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Mostrar cuadros de diálogo proporcionados por códecs VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Establecer parámetros de compresión de vídeo.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controlar cómo el [filtro WM ASF Writer](wm-asf-writer-filter.md) escribe archivos de formato de sistemas avanzados (ASF). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controlar cómo el [filtro Mux de AVI](avi-mux-filter.md) escribe archivos AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configure la intercalación cuando el filtro Mux de AVI escriba archivos AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Establezca la resolución de codificación en el filtro [DV Video Encoder.](dv-video-encoder-filter.md)                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Degradación de la velocidad de fotogramas en una secuencia de vídeo digital (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Establezca la resolución de descodificación en el filtro [Descodificador de vídeo DV.](dv-video-decoder-filter.md)                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Establezca y recupere fragmentos info y DISP en secuencias AVI.                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



