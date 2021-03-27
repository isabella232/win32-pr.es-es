---
description: Un gráfico circular es una región enlazada por la intersección de una curva de elipse y dos radiales. En la ilustración siguiente se muestra un gráfico circular dibujada con la función de gráfico circular.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Acerca de los gráficos circulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082372"
---
# <a name="about-pies"></a><span data-ttu-id="05671-104">Acerca de los gráficos circulares</span><span class="sxs-lookup"><span data-stu-id="05671-104">About Pies</span></span>

<span data-ttu-id="05671-105">Un *gráfico circular* es una región enlazada por la intersección de una curva de elipse y dos radiales.</span><span class="sxs-lookup"><span data-stu-id="05671-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="05671-106">En la ilustración siguiente se muestra un gráfico circular dibujada con la función de [**gráfico circular**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .</span><span class="sxs-lookup"><span data-stu-id="05671-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![Ilustración en la que se muestra una elipse con un círculo sombreado](images/csfsh-03.png)

<span data-ttu-id="05671-108">Al llamar a un [**gráfico circular**](/windows/win32/api/wingdi/nf-wingdi-pie), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales.</span><span class="sxs-lookup"><span data-stu-id="05671-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="05671-109">Cuando el sistema dibuja la parte curva del gráfico circular, usa la dirección de arco actual para el contexto de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="05671-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="05671-110">La dirección de arco predeterminada es en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="05671-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="05671-111">Una aplicación puede restablecer la dirección del arco llamando a la función [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="05671-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
