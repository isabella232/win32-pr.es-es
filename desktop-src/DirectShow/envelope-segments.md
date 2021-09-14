---
description: Segmentos de sobre
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmentos de sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272996"
---
# <a name="envelope-segments"></a>Segmentos de sobre

Una curva de parámetros consta de uno o varios segmentos de sobre, definidos mediante la estructura [**MP \_ ENVELOPE \_ SEGMENT.**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) Esta estructura contiene la siguiente información:

-   Horas de inicio y finalización.
-   Los valores inicial y final.
-   Tipo de curva (lineal, cuadrada, etc.).
-   Marcas opcionales, descritas en breve.

El cliente agrega segmentos de sobre a un parámetro llamando al método [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) y pasando una matriz de estructuras **MP ENVELOPE \_ \_ SEGMENT.** El cliente debe ordenar los segmentos en orden de hora ascendente antes de llamar al método . A medida que DMO datos, puede imaginar el parámetro que viaja por cada segmento de sobre, como un automóvil que conduce sobre una serie de bicicletas. El [**método IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) devuelve el valor más reciente.

Dos segmentos adyacentes pueden tener una brecha entre ellos. Durante las brechas, el parámetro conserva su valor anterior, como se muestra a continuación:

-   Antes del primer segmento, el valor es el valor neutro.
-   Entre segmentos, el valor es el valor final del segmento anterior.
-   Después del último segmento, el valor permanece en el valor final de ese segmento.
-   Si el cliente vacía el DMO, el valor vuelve al valor neutro.

Puede modificar un segmento estableciendo cualquiera de las siguientes marcas:

-   MPF \_ ENVLP \_ BEGIN \_ CURRENTVAL. El DMO usa el valor más reciente del parámetro como valor inicial del segmento. Puede ser el valor neutro o el valor final del segmento anterior. El DMO omite el miembro **valStart** de la estructura **MP ENVELOPE \_ \_ SEGMENT.**
-   MPF \_ ENVLP \_ BEGIN \_ NEUTRALVAL. El DMO usa el valor neutro del parámetro como valor inicial del segmento. Omite **valStart.**

Puede pensar que estas marcas capturan el punto inicial del segmento y lo mueven hacia arriba o hacia abajo, mientras que el valor final permanece fijo. El segmento se "extenderá" en consecuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 



