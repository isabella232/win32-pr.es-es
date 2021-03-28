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
# <a name="about-ellipses"></a><span data-ttu-id="c4d80-103">Acerca de los puntos suspensivos</span><span class="sxs-lookup"><span data-stu-id="c4d80-103">About Ellipses</span></span>

<span data-ttu-id="c4d80-104">Una elipse es una curva cerrada definida por dos puntos fijos (F1 y F2), de modo que la suma de las distancias (D1 + D2) de cualquier punto de la curva a los dos puntos fijos es constante.</span><span class="sxs-lookup"><span data-stu-id="c4d80-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="c4d80-105">En la ilustración siguiente se muestra una elipse dibujada con la función [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .</span><span class="sxs-lookup"><span data-stu-id="c4d80-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![Ilustración que muestra una elipse, dos puntos fijos, dos distancias y un rectángulo delimitador](images/csfsh-01.png)

<span data-ttu-id="c4d80-107">Al llamar a [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse.</span><span class="sxs-lookup"><span data-stu-id="c4d80-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="c4d80-108">Un *rectángulo delimitador* es el rectángulo más pequeño que rodea A la elipse.</span><span class="sxs-lookup"><span data-stu-id="c4d80-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="c4d80-109">Cuando el sistema dibuja la elipse, excluye los lados derecho e inferior si no se establece ninguna transformación universal.</span><span class="sxs-lookup"><span data-stu-id="c4d80-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="c4d80-110">Por lo tanto, para cualquier rectángulo que mida x unidades de ancho por unidades y, la elipse asociada mide x1 unidades de ancho por unidades Y1 de alto.</span><span class="sxs-lookup"><span data-stu-id="c4d80-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="c4d80-111">Si la aplicación establece una transformación universal mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , el sistema incluye los lados derecho e inferior.</span><span class="sxs-lookup"><span data-stu-id="c4d80-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



