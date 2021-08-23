---
description: Nuevos segmentos
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuevos segmentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28701a29a3b4edd61e9eb408aeab744297eac56408c49dc77dd4328a5afd24b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790935"
---
# <a name="new-segments"></a>Nuevos segmentos

Un *segmento es* un grupo de ejemplos multimedia que comparten una hora de inicio, una hora de detenerse y una velocidad de reproducción comunes. El [**método IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) señala el inicio de un nuevo segmento. Proporciona una manera de que un filtro de origen informe a los filtros de bajada de que la información de velocidad y hora ha cambiado. Por ejemplo, si el filtro de origen busca un nuevo punto en la secuencia, llama a **NewSegment** con la nueva hora de inicio.

Algunos filtros de nivel inferior usan la información de segmento al procesar ejemplos. Por ejemplo, en un formato que usa la compresión entre tramas, si la hora de detenerse se encuentra en un marco delta, es posible que el filtro de origen tenga que enviar muestras adicionales después de la hora de detenerse. Esto permite al descodificador descodificar el marco delta final. Para determinar el fotograma final correcto, el descodificador hace referencia al tiempo de detenerse del segmento. Como otro ejemplo, los representadores de audio usan la velocidad de segmento junto con la velocidad de muestreo de audio para generar la salida de audio correcta.

En el modelo de inserción, el filtro de origen inicia **la llamada NewSegment.** En el modelo de extracción, esto se realiza mediante el filtro del analizador. En cualquier caso, el filtro llama a **NewSegment** en el pin de entrada de bajada, que propaga la llamada al filtro siguiente, hasta que la llamada llega al representador. Los filtros deben serializar **llamadas NewSegment** con otras llamadas de streaming, como [**IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

El tiempo de transmisión se restablece en cero después de cada nuevo segmento. Marcas de tiempo en los ejemplos entregados después de que el segmento comience desde cero.

 

 



