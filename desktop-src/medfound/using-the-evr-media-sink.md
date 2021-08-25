---
description: Uso del receptor de medios EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del receptor de medios EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ced80b4f9ee17093a00436a26f3f142281907597191791712fd6900520926ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826295"
---
# <a name="using-the-evr-media-sink"></a>Uso del receptor de medios EVR

El receptor multimedia de representador de vídeo mejorado (EVR) se puede usar como componente independiente. Sin embargo, con más frecuencia, una aplicación creará el receptor de medios EVR dentro de una topología y, a continuación, usará la sesión multimedia para controlar la reproducción.

Hay dos maneras de crear el receptor de medios EVR:

-   La [**función MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea el receptor multimedia.

-   La [**función MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un objeto de activación para el receptor multimedia.

El receptor de medios EVR inicialmente tiene un receptor de flujo, que corresponde a la secuencia de referencia. Para agregar nuevos receptores de flujo, llame [**a IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> </dl>

 

 



