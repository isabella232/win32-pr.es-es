---
title: Implementación de un complemento DSP de vídeo
description: Implementación de un complemento DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, implementar código
- Complementos DSP, implementar código
- Complementos de procesamiento de señal digital, modificar código de ejemplo
- Complementos DSP, modificar código de ejemplo
- Complementos de procesamiento de señal digital, implementación de vídeo
- Complementos DSP, implementación de vídeo
- Complementos de DSP de vídeo, implementar código
- Complementos de DSP de vídeo, modificar código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357212"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementación de un complemento DSP de vídeo

Los adaptadores de pantalla de vídeo del equipo admiten un conjunto de formatos de vídeo. Los códecs de vídeo digital también admiten un conjunto de formatos de vídeo. Al intentar reproducir un archivo de vídeo determinado, Windows Media Player debe elegir el formato que se va a usar para la representación. El reproductor intenta encontrar la mejor coincidencia entre los formatos admitidos por el códec de vídeo y los formatos admitidos por el adaptador de pantalla de vídeo, es decir, el que produce la máxima calidad.

Para crear un complemento DSP de Windows Media Player que procese el vídeo, primero deberá decidir qué formatos de vídeo quiere que procese el complemento. El complemento DSP de vídeo de ejemplo funciona con los siguientes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Los formatos que decida procesar dependerán de usted. Puede quitar formatos del complemento de ejemplo para que no se admitan más tiempo y pueda agregar código para procesar formatos adicionales.

En las secciones siguientes se proporciona información adicional que debe conocer antes de crear su propio complemento DSP de vídeo para Windows Media Player:

-   [Negociación del formato de vídeo en el complemento DSP de vídeo de ejemplo](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput en el complemento DSP de vídeo de ejemplo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Procesamiento del vídeo](processing-the-video.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación del código DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




