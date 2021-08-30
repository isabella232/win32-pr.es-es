---
title: Acerca del complemento DSP de audio de ejemplo
description: Acerca del complemento DSP de audio de ejemplo
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Reproductor de Windows Media complementos, ejemplos
- complementos, ejemplos
- complementos de procesamiento de señales digitales, ejemplos
- Complementos de DSP, ejemplos
- Reproductor de Windows Media complementos, DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señales digitales, ejemplos de audio
- Complementos de DSP, ejemplos de audio
- samples,DSP plug-ins
- audio DSP plug-ins,samples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda93e663e8f80421a096ebc6c5c026621c95c7681516475645913214d99437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956575"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a>Acerca del complemento DSP de audio de ejemplo

El complemento DSP de audio de ejemplo proporciona una implementación de procesamiento simple que escala la amplitud del audio mediante un factor proporcionado por el usuario en la página de propiedades. El complemento acepta valores entre cero y 1. El valor predeterminado es 1. Un valor de 1 no tiene ningún efecto sobre el sonido; otros factores de escala son multiplicadores para las muestras de audio. Por ejemplo, un valor de .5 produciría una disminución de 6 decibelios en el volumen. Un valor de cero produce un silencio.

El complemento DSP de audio de ejemplo funciona con audio PCM estéreo o mono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un complemento DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




