---
description: Una elipse es una curva cerrada definida por dos puntos fijos (f1 y f2), de modo que la suma de las distancias (d1 +d2) desde cualquier punto de la curva hasta los dos puntos fijos es constante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Acerca de los puntos suspensivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0892bfd2a8aa6fad43d18ead65eb92d260150ab31ca9057177c33af2cb8d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888563"
---
# <a name="about-ellipses"></a>Acerca de los puntos suspensivos

Una elipse es una curva cerrada definida por dos puntos fijos (f1 y f2), de modo que la suma de las distancias (d1 +d2) desde cualquier punto de la curva hasta los dos puntos fijos es constante. En la ilustración siguiente se muestra una elipse dibujada mediante la [**función Ellipse.**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)

![ilustración que muestra una elipse, dos puntos fijos, dos distancias y un rectángulo delimitador](images/csfsh-01.png)

Al llamar [**a Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse. Un *rectángulo delimitador es* el rectángulo más pequeño que rodea completamente la elipse. Cuando el sistema dibuja la elipse, excluye los lados derecho e inferior si no se establece ninguna transformación del mundo. Por lo tanto, para cualquier rectángulo que mida x unidades de ancho por y unidades de alto, la elipse asociada mide x1 unidades de ancho por y1 unidades de alto. Si la aplicación establece una transformación del mundo mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform,**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) el sistema incluye los lados derecho e inferior.

 

 



