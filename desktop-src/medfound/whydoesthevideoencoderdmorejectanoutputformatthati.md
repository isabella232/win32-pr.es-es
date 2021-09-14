---
description: ¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer cuando he recuperado el formato del mismo objeto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: ¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer cuando he recuperado el formato del mismo objeto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263151"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>¿Por qué el codificador de vídeo rechaza un formato de salida que intento establecer cuando he recuperado el formato del mismo objeto?

A diferencia de los tipos de salida del codificador de audio, las salidas admitidas enumeradas por los codificadores de vídeo no se completan como se entregan. Debe establecer la velocidad de bits de la secuencia en el **miembro dwBitrate** de la estructura **VIDEOINFOHEADER** para que coincida con el valor establecido para la [propiedad \_ MFPKEY DEVERG.](mfpkey-ravgproperty.md)

Una vez establecidas todas las opciones de la manera que quiere, debe recuperar los datos privados del códec y anexarlos a la **estructura VIDEOINFOHEADER.** Para obtener más información, consulte [Uso de datos privados de códec de vídeo.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



