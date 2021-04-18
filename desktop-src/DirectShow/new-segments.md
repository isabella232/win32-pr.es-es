---
description: Nuevos segmentos
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuevos segmentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686278"
---
# <a name="new-segments"></a>Nuevos segmentos

Un *segmento* es un grupo de muestras multimedia que comparten una hora de inicio, una hora de detención y una velocidad de reproducción comunes. El método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) señala el inicio de un nuevo segmento. Proporciona un método para que un filtro de origen informe de los filtros de nivel inferior que la información de hora y tasa ha cambiado. Por ejemplo, si el filtro de origen busca un punto nuevo en la secuencia, llama a **NewSegment** con la nueva hora de inicio.

Algunos filtros de nivel inferior usan la información del segmento cuando procesan ejemplos. Por ejemplo, en un formato que usa la compresión entre fotogramas, si la hora de detención cae en un fotograma Delta, es posible que el filtro de origen necesite enviar muestras adicionales después de la hora de detención. Esto permite al descodificador descodificar el fotograma delta final. Para determinar el fotograma final correcto, el descodificador hace referencia a la hora de detención del segmento. Otro ejemplo: los representadores de audio usan la velocidad de segmento junto con la velocidad de muestreo de audio para generar la salida de audio correcta.

En el modelo de extracción, el filtro de origen inicia la llamada a **NewSegment** . En el modelo de extracción, esto se realiza mediante el filtro del analizador. En cualquier caso, el filtro llama a **NewSegment** en el PIN de entrada de nivel inferior, que propaga la llamada al siguiente filtro, hasta que la llamada alcanza el representador. Los filtros deben serializar llamadas **NewSegment** con otras llamadas de streaming, como [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).

El tiempo de secuencia se restablece en cero después de cada nuevo segmento. Marcas de tiempo en las muestras entregadas después de que el segmento empiece desde cero.

 

 



