---
description: Interfaces de codificación y descodificación de archivos
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces de codificación y descodificación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152694"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfaces de codificación y descodificación de archivos

Estas interfaces admiten la codificación y descodificación de archivos.



| Interfaz                                                    | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recuperar metadatos de un flujo, como el autor y el título.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determine el progreso de una operación de apertura de archivos.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Consultar y establecer el tiempo de análisis para la posición actual en una secuencia MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controlar qué secuencias lógicas se reproducen y recuperar información sobre ellas.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Mostrar cuadros de diálogo proporcionados por códecs VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Establecer parámetros de compresión de vídeo.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controlar cómo el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) escribe archivos de formato de sistema avanzado (ASF). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controlar el modo en que el filtro de [AVI](avi-mux-filter.md) no escribe archivos AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configurar la intercalación cuando el filtro de AVI MUX escribe archivos AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Establezca la resolución de codificación en el filtro del [codificador de vídeo DV](dv-video-encoder-filter.md) .                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Degradar la velocidad de fotogramas en una secuencia de vídeo digital (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Establezca la resolución de descodificación en el filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) .                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Establezca y recupere información y DISP fragmentos en secuencias AVI.                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



