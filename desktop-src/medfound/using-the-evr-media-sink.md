---
description: Uso del receptor de medios EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del receptor de medios EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579789"
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

 

 



