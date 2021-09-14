---
title: Acerca del complemento DSP de audio de ejemplo
description: Acerca del complemento DSP de audio de ejemplo
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Reproductor de Windows Media complementos,ejemplos
- complementos, ejemplos
- complementos de procesamiento de señales digitales, ejemplos
- Complementos de DSP, ejemplos
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señales digitales, ejemplos de audio
- Complementos de DSP, ejemplos de audio
- samples,DSP plug-ins
- complementos de DSP de audio, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890212"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a>Acerca del complemento DSP de audio de ejemplo

El complemento DSP de audio de ejemplo proporciona una implementación de procesamiento simple que escala la amplitud del audio por un factor proporcionado por el usuario en la página de propiedades. El complemento acepta valores entre cero y 1. El valor predeterminado es 1. Un valor de 1 no tiene ningún efecto en el sonido; otros factores de escala son multiplicadores para las muestras de audio. Por ejemplo, un valor de .5 daría como resultado una disminución de 6 decibelios en el volumen. Un valor de cero da como resultado silencio.

El complemento DSP de audio de ejemplo funciona con audio PCM estéreo o mono.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un complemento de DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




