---
description: Segmentos de sobre
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmentos de sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537378"
---
# <a name="envelope-segments"></a>Segmentos de sobre

Una curva de parámetro se compone de uno o varios segmentos de sobre, definidos mediante la estructura de [**\_ \_ segmentos de sobres de MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) . Esta estructura contiene la siguiente información:

-   Horas de inicio y finalización.
-   Los valores inicial y final.
-   El tipo de curva (lineal, cuadrada, etc.).
-   Marcas opcionales, descritas en breve.

El cliente agrega segmentos de sobre a un parámetro llamando al método [**IMediaParams:: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) y pasando una matriz de estructuras **de \_ \_ segmentos de sobre de MP** . El cliente debe ordenar los segmentos en orden temporal ascendente antes de llamar al método. A medida que DMO procesa los datos, puede imaginarse el parámetro que viaja sobre cada segmento de sobre, como un automóvil que conduce a una serie de colinas. El método [**IMediaParams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) devuelve el valor más reciente.

Dos segmentos adyacentes pueden tener un espacio entre ellos. Durante los huecos, el parámetro conserva su valor anterior, como se indica a continuación:

-   Antes del primer segmento, el valor es el valor neutro.
-   Entre segmentos, el valor es el valor final del segmento anterior.
-   Después del último segmento, el valor permanece en el valor final del segmento.
-   Si el cliente vacía DMO, el valor se revierte al valor neutro.

Puede modificar un segmento estableciendo cualquiera de las marcas siguientes:

-   MPF \_ ENVLP \_ Begin \_ CURRENTVAL. DMO usa el valor más reciente del parámetro como el valor inicial del segmento. Podría ser el valor neutro o el valor final del segmento anterior. DMO omite el miembro **valStart** de la estructura del **\_ \_ segmento de sobre de MP** .
-   MPF \_ ENVLP \_ Begin \_ NEUTRALVAL. DMO usa el valor neutro del parámetro como el valor inicial para el segmento. Omite **valStart**.

Puede pensar en estas marcas como en la captación del punto inicial del segmento y en moverla hacia arriba o hacia abajo, mientras que el valor final permanece fijo. El segmento se "ajustará" en consecuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



