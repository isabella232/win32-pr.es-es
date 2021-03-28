---
description: Una elipse es una curva cerrada definida por dos puntos fijos (F1 y F2), de modo que la suma de las distancias (D1 + D2) de cualquier punto de la curva a los dos puntos fijos es constante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Acerca de los puntos suspensivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549866"
---
# <a name="about-ellipses"></a>Acerca de los puntos suspensivos

Una elipse es una curva cerrada definida por dos puntos fijos (F1 y F2), de modo que la suma de las distancias (D1 + D2) de cualquier punto de la curva a los dos puntos fijos es constante. En la ilustración siguiente se muestra una elipse dibujada con la función [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .

![Ilustración que muestra una elipse, dos puntos fijos, dos distancias y un rectángulo delimitador](images/csfsh-01.png)

Al llamar a [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse. Un *rectángulo delimitador* es el rectángulo más pequeño que rodea A la elipse. Cuando el sistema dibuja la elipse, excluye los lados derecho e inferior si no se establece ninguna transformación universal. Por lo tanto, para cualquier rectángulo que mida x unidades de ancho por unidades y, la elipse asociada mide x1 unidades de ancho por unidades Y1 de alto. Si la aplicación establece una transformación universal mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , el sistema incluye los lados derecho e inferior.

 

 



