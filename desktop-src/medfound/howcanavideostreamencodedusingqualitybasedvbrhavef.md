---
description: ¿Cómo puede una secuencia de vídeo codificada mediante VBR basada en calidad tener menos fotogramas que la secuencia original?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: ¿Cómo puede una secuencia de vídeo codificada mediante VBR basada en calidad tener menos fotogramas que la secuencia original?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475835"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>¿Cómo puede una secuencia de vídeo codificada mediante VBR basada en calidad tener menos fotogramas que la secuencia original?

El número de fotogramas de una secuencia codificada puede ser inferior al número de fotogramas del original por una de estas dos razones: fotogramas duplicados y fotogramas eliminados.

Normalmente, el codificador no genera fotogramas que son exactamente duplicados del fotograma anterior. Si necesita tener un ejemplo para cada fotograma (esto lo requieren algunos contenedores, por ejemplo), puede configurar el codificador para que produzca fotogramas "ficticios" estableciendo la propiedad [ \_ MFPKEY PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en VARIANT \_ TRUE.

El codificador quita fotogramas cuando no puede codificar todos los fotogramas sin desbordar el búfer. Los fotogramas eliminados afectan a la calidad de la secuencia; los fotogramas duplicados no.

Puede obtener estadísticas de fotogramas del codificador para determinar si se han eliminado los fotogramas. Para obtener más información, vea [Obtener estadísticas de codificación.](gettingencodingstatistics.md)

Normalmente, las secuencias de VBR basadas en la calidad solo tendrán menos fotogramas que el original si hay fotogramas duplicados (porque la velocidad de bits no está restringida).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



