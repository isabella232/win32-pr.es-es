---
title: Acerca del complemento DSP de vídeo de ejemplo
description: Acerca del complemento DSP de vídeo de ejemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Reproductor de Windows Media complementos, ejemplos
- complementos, ejemplos
- complementos de procesamiento de señales digitales, ejemplos
- Complementos de DSP, ejemplos
- Reproductor de Windows Media complementos, DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señales digitales, ejemplos de vídeo
- Complementos de DSP, ejemplos de vídeo
- samples,DSP plug-ins
- complementos de DSP de vídeo, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb771bb87ffb53cf46022fc17ee2588e7cdac0b6b2c821f98fe6cf86799434c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470255"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>Acerca del complemento DSP de vídeo de ejemplo

El complemento DSP de vídeo de ejemplo proporciona una implementación de procesamiento simple que escala la saturación de color del vídeo por un factor proporcionado por el usuario en la página de propiedades. El complemento acepta valores entre cero y 1. El valor predeterminado es 1. Un valor de 1 no tiene ningún efecto sobre la imagen de vídeo; otros factores de escala desaturan el color de la imagen. Por ejemplo, un valor de .5 produciría una saturación de color del 50 por ciento. Un valor de cero da como resultado un vídeo de escala de grises.

El complemento DSP de vídeo de ejemplo funciona con los siguientes formatos de vídeo:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un complemento DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




