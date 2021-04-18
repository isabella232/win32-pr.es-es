---
description: Uso del receptor de medios de EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del receptor de medios de EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717396"
---
# <a name="using-the-evr-media-sink"></a>Uso del receptor de medios de EVR

El receptor de medios de representador de vídeo mejorado (EVR) se puede usar como un componente independiente. Sin embargo, a menudo, una aplicación creará el receptor de medios EVR dentro de una topología y, a continuación, usará la sesión multimedia para controlar la reproducción.

Hay dos maneras de crear el receptor de medios EVR:

-   La función [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea el receptor de medios.

-   La función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un objeto de activación para el receptor de medios.

El receptor de medios EVR inicialmente tiene un receptor de flujo, que corresponde al flujo de referencia. Para agregar nuevos receptores de secuencia, llame a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[Receptores de medios](media-sinks.md)
</dt> </dl>

 

 



