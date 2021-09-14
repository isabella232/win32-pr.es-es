---
title: Acerca del complemento DSP de vídeo de ejemplo
description: Acerca del complemento DSP de vídeo de ejemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Reproductor de Windows Media complementos,ejemplos
- complementos, ejemplos
- complementos de procesamiento de señales digitales, ejemplos
- Complementos de DSP, ejemplos
- Reproductor de Windows Media complementos,DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señales digitales, ejemplos de vídeo
- Complementos de DSP, ejemplos de vídeo
- samples,DSP plug-ins
- complementos de DSP de vídeo, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967776"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>Acerca del complemento DSP de vídeo de ejemplo

El complemento DSP de vídeo de ejemplo proporciona una implementación de procesamiento simple que escala la saturación de color del vídeo por un factor proporcionado por el usuario en la página de propiedades. El complemento acepta valores entre cero y 1. El valor predeterminado es 1. Un valor de 1 no tiene ningún efecto en la imagen de vídeo; otros factores de escala desaturan el color de la imagen. Por ejemplo, un valor de .5 daría como resultado una saturación de color del 50 por ciento. Un valor de cero da como resultado un vídeo de escala de grises.

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

[**Creación de un complemento de DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




