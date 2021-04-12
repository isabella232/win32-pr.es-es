---
description: Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima. ¿Cómo es posible?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360567"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima. ¿Cómo es posible?

La relación entre la velocidad de bits promedio y la velocidad de bits pico suele ser errónea. La velocidad de bits máxima describe una restricción de búfer durante un período de tiempo especificado por la ventana de búfer máximo. La velocidad de bits promedio para VBR de dos pasos (sin restricciones o con límite máximo) es el promedio de bits por segundo a lo largo de la duración del archivo.

Tal y como se describe en [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md), la velocidad de bits real usada durante un período de tiempo igual a la ventana de búfer puede alcanzar el doble de velocidad de bits. Esto se debe a que el búfer, definido como un número de bits igual a la velocidad de bits, la ventana de búfer (en segundos), se vacía a una velocidad constante.

Por ejemplo, en un segundo de una secuencia de 56 kbps, el codificador crea ejemplos con un total de 59 KB. Por lo tanto, se quitan de 56 KB de datos del búfer en ese segundo, con lo que se dejan 3 KB en el búfer. Si la secuencia tiene una ventana de búfer de tres segundos y, por lo tanto, un tamaño de búfer total de 168 KB, tardaría casi 40 segundos en rellenar el búfer. La velocidad de bits media de la secuencia (si su duración es menor que el tiempo que se tarda en rellenar el búfer) es de 59 Kbps, aunque la velocidad de bits esté establecida en 56 kbps.

El mismo fenómeno se aplica a las restricciones de velocidad de bits máxima. En el caso de contenido corto, la velocidad de bits promedio calculada por el objeto de códec una vez completada la codificación puede ser mayor que la velocidad de bits máxima.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



