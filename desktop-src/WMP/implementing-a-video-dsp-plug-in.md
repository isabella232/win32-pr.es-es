---
title: Implementación de un complemento DSP de vídeo
description: Implementación de un complemento DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Reproductor de Windows Media complementos, DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señales digitales, implementar código
- Complementos de DSP, implementar código
- complementos de procesamiento de señales digitales, modificar código de ejemplo
- Complementos de DSP, modificar código de ejemplo
- complementos de procesamiento de señal digital, implementación de vídeo
- Complementos de DSP, implementación de vídeo
- complementos de DSP de vídeo, implementar código
- complementos de DSP de vídeo, modificar código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135708"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementación de un complemento DSP de vídeo

Los adaptadores de pantalla de vídeo del equipo admiten un conjunto de formatos de vídeo. Los códecs de vídeo digital también admiten un conjunto de formatos de vídeo. Al intentar reproducir un archivo de vídeo determinado, Reproductor de Windows Media debe elegir un formato que se usará para la representación. El reproductor intenta encontrar la mejor coincidencia entre los formatos admitidos por el códec de vídeo y los formatos admitidos por el adaptador de pantalla de vídeo, es decir, el que produce la máxima calidad.

Para crear un Reproductor de Windows Media DSP que procese vídeo, primero deberá decidir qué formatos de vídeo desea que procese el complemento. El complemento DSP de vídeo de ejemplo funciona con los siguientes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Los formatos que decida procesar son los que usted decida. Puede quitar formatos del complemento de ejemplo para que ya no se admiten y puede agregar código para procesar formatos adicionales.

En las secciones siguientes se proporciona información adicional que debe conocer antes de crear su propio complemento DSP de vídeo para Reproductor de Windows Media:

-   [Negociación de formato de vídeo en el complemento DSP de vídeo de ejemplo](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput en el complemento DSP de vídeo de ejemplo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Procesamiento del vídeo](processing-the-video.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación del código DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




