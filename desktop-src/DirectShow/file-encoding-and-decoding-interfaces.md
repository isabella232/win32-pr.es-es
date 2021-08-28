---
description: Interfaces de codificación y codificación de archivos
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces de codificación y codificación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6654497b0d2407666b286fb74f06a91e66834cfb963b62b7e22eb5755fa30b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639665"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfaces de codificación y codificación de archivos

Estas interfaces admiten la codificación y la codificación de archivos.



| Interfaz                                                    | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recuperar metadatos de una secuencia, como el autor y el título.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determine el progreso de una operación de apertura de archivos.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Consulte y establezca el tiempo de análisis de la posición actual en una secuencia MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controlar qué secuencias lógicas se reproducen y recuperar información sobre ellas.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Mostrar cuadros de diálogo proporcionados por códecs VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Establecer parámetros de compresión de vídeo.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controlar cómo el [filtro WM ASF Writer](wm-asf-writer-filter.md) escribe archivos de formato de sistemas avanzados (ASF). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controlar cómo el [filtro AVI Mux](avi-mux-filter.md) escribe archivos AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configure la intercalación cuando el filtro AVI Mux escriba archivos AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Establezca la resolución de codificación en el [filtro DV Video Encoder.](dv-video-encoder-filter.md)                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Degradación de la velocidad de fotogramas en una secuencia de vídeo digital (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Establezca la resolución de descodificación en el filtro [Descodificador de vídeo DV.](dv-video-decoder-filter.md)                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Establezca y recupere fragmentos info y DISP en secuencias AVI.                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



