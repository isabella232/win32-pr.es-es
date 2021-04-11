---
description: ¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: ¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276379"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>¿Cómo puede una secuencia de vídeo codificada con VBR basada en la calidad tener menos fotogramas que la secuencia original?

El número de fotogramas de una secuencia codificada puede ser menor que el número de fotogramas del original por uno de estos dos motivos: fotogramas duplicados y fotogramas descartados.

El codificador no genera normalmente fotogramas que son duplicados exactos del fotograma anterior. Si necesita tener un ejemplo para cada fotograma (esto es necesario para algunos contenedores, por ejemplo), puede configurar el codificador para que genere fotogramas "ficticios" estableciendo la propiedad [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en Variant \_ true.

El codificador quita los fotogramas cuando no puede codificar todos los marcos sin desbordar el búfer. Los fotogramas quitados afectan a la calidad de la secuencia, no los fotogramas duplicados.

Puede obtener estadísticas de fotogramas del codificador para determinar si se han quitado los fotogramas. Para obtener más información, vea [obtener estadísticas de codificación](gettingencodingstatistics.md).

Normalmente, las secuencias VBR basadas en la calidad solo tendrán menos fotogramas que el original si hay fotogramas duplicados (porque la velocidad de bits no está restringida).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



