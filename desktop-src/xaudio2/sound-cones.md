---
description: Modelo que describe la sonoridad del sonido orientado.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Conos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc6b55ce1cc98b1875dff7079a0a304ef77c5567966808a4678f01f2297ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005784"
---
# <a name="sound-cones"></a>Conos de sonido

Modelo que describe la sonoridad del sonido orientado.

Un sonido sin orientación tiene la misma amplitud a una distancia determinada en todas las direcciones. Un sonido con una orientación es más alto en la dirección de la orientación. El modelo que describe la sonoridad del sonido orientado se denomina cono de sonido. Los conos de sonido están hechos de un cono interior (o interno) y un cono exterior (o externo). El ángulo del cono exterior siempre debe ser igual o mayor que el ángulo del cono interior.

En cualquier ángulo dentro del cono interno, el volumen del sonido se establece en el volumen de cono interno. Esto tiene en cuenta el volumen básico del búfer, la distancia desde el agente de escucha, la orientación del agente de escucha si el agente de escucha tiene su propio cono, y así sucesivamente.

En cualquier ángulo fuera del cono exterior, el volumen normal se atenua mediante un factor establecido por la aplicación. El nivel de volumen de cono exterior se expresa como un escalador de amplitud lineal: 1,0 f no representa ninguna atenuación aplicada a la señal original, 0,5 f denota una atenuación de 6 dB y 0,0 f produce silencio. También se permite la > volumen (1,0 f) y no está fija. El intervalo de volúmenes válido es realmente de 0,0 f a 2,0 f.

Entre los conos internos y externos hay una zona de transición del volumen interno al volumen exterior. El volumen se aproxima al volumen exterior del cono a medida que aumenta el ángulo.

Los conos pueden afectar a parámetros distintos del volumen. El filtro de paso bajo y el nivel de envío de reverberación también pueden verse afectados, lo que hace que la técnica sea aún más drástica. Por ejemplo, con un cono en el agente de escucha, se puede especificar que todos los sonidos detrás del agente de escucha se desconcerten un poco y que el contenido de la relación entre reverberación y directo sea ligeramente mayor. Proporcionan más indicaciones de que el sonido está detrás del usuario. Esto mejora el realismo.

En la ilustración siguiente se muestra el concepto de conos de sonido.

![conos de sonido](images/common-audio-concepts-sound-cones.png)

Diseñar los conos de sonido correctamente puede agregar efectos drásticos a la aplicación. Por ejemplo, podría colocar una fuente de sonido en el centro de una sala, estableciendo su orientación hacia una puerta abierta en un ambiente. A continuación, establezca el ángulo del cono interior para que se extienda al ancho de la puerta, haga que el cono exterior sea un poco más ancho y, por último, establezca el volumen de cono exterior en inaudible. Un agente de escucha que se mueve a lo largo del sonido comenzará a escuchar el sonido solo cuando esté cerca de la puerta. El sonido será más alto a medida que el agente de escucha pase delante de la puerta abierta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos comunes de audio](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**CONO X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



