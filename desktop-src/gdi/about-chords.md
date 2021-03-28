---
description: Una cuerda es una región enlazada por la intersección de una elipse y un segmento de línea denominado secante. En la ilustración siguiente se muestra una cuerda dibujada con la función de cuerda.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Acerca de las cuerda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543630"
---
# <a name="about-chords"></a><span data-ttu-id="6c73f-104">Acerca de las cuerda</span><span class="sxs-lookup"><span data-stu-id="6c73f-104">About Chords</span></span>

<span data-ttu-id="6c73f-105">Una *cuerda* es una región enlazada por la intersección de una elipse y un segmento de línea denominado *secante*.</span><span class="sxs-lookup"><span data-stu-id="6c73f-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="6c73f-106">En la ilustración siguiente se muestra una cuerda dibujada con la función de [**cuerda**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .</span><span class="sxs-lookup"><span data-stu-id="6c73f-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![Ilustración de un elipse, que muestra dos radiales, una secante y una cuerda](images/csfsh-02.png)

<span data-ttu-id="6c73f-108">Al llamar a [**cuerda**](/windows/win32/api/wingdi/nf-wingdi-chord), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales.</span><span class="sxs-lookup"><span data-stu-id="6c73f-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="6c73f-109">Un radial es una línea dibujada desde el centro del rectángulo delimitador de una elipse hasta un punto de la elipse.</span><span class="sxs-lookup"><span data-stu-id="6c73f-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="6c73f-110">Cuando el sistema dibuja la parte curvada de la cuerda, lo hace mediante el uso de la dirección de arco actual para el contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c73f-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="6c73f-111">La dirección de arco predeterminada es en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="6c73f-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="6c73f-112">Puede hacer que la aplicación restablezca la dirección del arco llamando a la función [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="6c73f-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
