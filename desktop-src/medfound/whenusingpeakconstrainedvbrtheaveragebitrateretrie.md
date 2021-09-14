---
description: Cuando uso VBR con restricciones máximas, la velocidad de bits media recuperada del objeto de códec es mayor que la velocidad de bits máxima.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Cuando uso VBR con restricciones máximas, la velocidad de bits media recuperada del objeto de códec es mayor que la velocidad de bits máxima. ¿Cómo es posible?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263159"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Cuando uso VBR con restricciones máximas, la velocidad de bits media recuperada del objeto de códec es mayor que la velocidad de bits máxima. ¿Cómo es posible?

La relación entre la velocidad de bits media y la velocidad de bits máxima a menudo se malinterpreta. La velocidad de bits máxima describe una restricción de búfer durante un período de tiempo especificado por la ventana de búfer máximo. La velocidad de bits media de VBR de dos pases (sin restricciones o con restricciones máximas) es el promedio de bits por segundo durante la duración del archivo.

Como se describe en [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md)(Modelo de búfer de cubo filtrada), la velocidad de bits real usada durante un período de tiempo igual a la ventana de búfer puede aproximarse al doble de la velocidad de bits. Esto se debe a que el búfer, definido como un número de bits igual a la velocidad de bits veces que la ventana del búfer (en segundos), se vacía a una velocidad constante.

Por ejemplo, en un segundo de una secuencia de 56 Kbps, el codificador crea muestras que suman 59 Kb. Por lo tanto, se quitan 56 Kb de datos del búfer en ese segundo, dejando 3 Kb en el búfer. Si la secuencia tiene una ventana de búfer de tres segundos y, por tanto, un tamaño total de búfer de 168 Kb, se tardarían casi 40 segundos en rellenar el búfer. La velocidad de bits media de la secuencia (si su duración es menor que el tiempo necesario para rellenar el búfer) es de 59 Kbps, aunque la velocidad de bits esté establecida en 56 Kbps.

El mismo fenómeno se aplica a las restricciones de velocidad de bits máxima. En el caso del contenido corto, la velocidad de bits media calculada por el objeto de códec una vez completada la codificación puede ser mayor que la velocidad de bits máxima.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



