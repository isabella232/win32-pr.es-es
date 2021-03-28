---
description: El rectángulo delimitador acumulado es el rectángulo más pequeño que incluye la parte de una ventana o área cliente afectada por las operaciones de dibujo recientes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rectángulo delimitador acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544558"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="c68ad-103">Rectángulo delimitador acumulado</span><span class="sxs-lookup"><span data-stu-id="c68ad-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="c68ad-104">El *rectángulo delimitador acumulado* es el rectángulo más pequeño que incluye la parte de una ventana o área cliente afectada por las operaciones de dibujo recientes.</span><span class="sxs-lookup"><span data-stu-id="c68ad-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="c68ad-105">Una aplicación puede usar este rectángulo para determinar de forma cómoda el alcance de los cambios causados por las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c68ad-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="c68ad-106">A veces se usa junto con [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para determinar qué parte del área de cliente se debe volver a dibujar una vez desactivado el bloqueo de actualización.</span><span class="sxs-lookup"><span data-stu-id="c68ad-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="c68ad-107">Una aplicación utiliza la función [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (ESPECIFICAndo DCB \_ enable) para empezar a acumular el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="c68ad-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="c68ad-108">Posteriormente, el sistema acumula puntos para el rectángulo delimitador a medida que la aplicación utiliza el contexto de dispositivo de pantalla especificado.</span><span class="sxs-lookup"><span data-stu-id="c68ad-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="c68ad-109">La aplicación puede recuperar el rectángulo delimitador actual en cualquier momento mediante la función [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) .</span><span class="sxs-lookup"><span data-stu-id="c68ad-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="c68ad-110">La aplicación detiene la acumulación al llamar a **SetBoundsRect** de nuevo, especificando el valor de DCB \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="c68ad-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



