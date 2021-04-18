---
description: Modelo que describe la sonoridad del sonido orientado.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Conos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707126"
---
# <a name="sound-cones"></a>Conos de sonido

Modelo que describe la sonoridad del sonido orientado.

Un sonido sin orientación tiene la misma amplitud a una distancia determinada en todas las direcciones. Un sonido con una orientación es lo más alto en la dirección de la orientación. El modelo que describe la sonoridad del sonido orientado se denomina cono de sonido. Los conos de sonido se componen de un cono interior (o interno) y un cono exterior (o externo). El ángulo del cono exterior siempre debe ser igual o mayor que el ángulo del cono interior.

En cualquier ángulo del cono interior, el volumen del sonido se establece en el volumen del cono interno. Esto tiene en cuenta el volumen básico del búfer, la distancia del agente de escucha, la orientación del agente de escucha si el agente de escucha tiene su propio cono y así sucesivamente.

En cualquier ángulo fuera del cono exterior, el volumen normal se atenúa por un factor establecido por la aplicación. El nivel de volumen del cono exterior se expresa como una amplitud lineal Scaler: 1,0 f no representa ninguna atenuación aplicada a la señal original, 0,5 f denota una atenuación de 6 dB y 0,0 f da como resultado el silencio. También se permite la amplificación (volumen > 1,0 f) y no está fija. El intervalo de volumen válido es, en realidad, de 0,0 a 2,0 f.

Entre los conos interno y externo hay una zona de transición desde el volumen interior al volumen exterior. El volumen se aproxima al volumen exterior del cono a medida que aumenta el ángulo.

Los conos pueden afectar a los parámetros distintos del volumen. El filtro de paso bajo y el nivel de envío de reverberación también se pueden ver afectados, por lo que la técnica es aún más espectacular. Por ejemplo, con un cono en el agente de escucha, puede especificar que todos los sonidos detrás del agente de escucha se queden sin silenciar y que tengan un contenido de posición de reverberación a directo ligeramente superior. Proporcionan más indicios de que el sonido está detrás del usuario. Esto mejora el realismo.

En la ilustración siguiente se muestra el concepto de conos de sonido.

![conos de sonido](images/common-audio-concepts-sound-cones.png)

El diseño correcto de los conos de sonido puede agregar efectos drásticos a la aplicación. Por ejemplo, podría colocar un origen de sonido en el centro de una habitación y establecer su orientación hacia una puerta abierta en un vestíbulo. A continuación, establezca el ángulo del cono interior de modo que se extienda hasta el ancho de la puerta, haga que el cono exterior sea un poco más amplio y, por último, establezca el volumen del cono exterior en inaudible. Un agente de escucha que se mueve a lo largo del vestíbulo comenzará a oír el sonido solo cuando esté cerca de la puerta. El sonido será más alto a medida que el agente de escucha pase delante de la puerta abierta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de audio comunes](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**\_Cono X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



