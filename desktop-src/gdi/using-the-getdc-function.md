---
description: La función GetDC se usa para llevar a cabo el dibujo que debe producirse de forma instantánea en lugar de cuando \_ se procesa un mensaje de pintura de WM.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Usar la función GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985347"
---
# <a name="using-the-getdc-function"></a><span data-ttu-id="7d54c-103">Usar la función GetDC</span><span class="sxs-lookup"><span data-stu-id="7d54c-103">Using the GetDC Function</span></span>

<span data-ttu-id="7d54c-104">La función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) se usa para llevar a cabo el dibujo que debe producirse de forma instantánea en lugar de cuando se procesa un mensaje de [**\_ pintura de WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="7d54c-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="7d54c-105">Este dibujo suele ser en respuesta a una acción por parte del usuario, como hacer una selección o dibujar con el mouse.</span><span class="sxs-lookup"><span data-stu-id="7d54c-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="7d54c-106">En tales casos, el usuario debe recibir comentarios instantáneos y no debe verse obligado a detener la selección o el dibujo para que la aplicación muestre el resultado.</span><span class="sxs-lookup"><span data-stu-id="7d54c-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="7d54c-107">En las secciones siguientes se muestra cómo usar GetDC para dibujar en una ventana:</span><span class="sxs-lookup"><span data-stu-id="7d54c-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="7d54c-108">Dibujar con el mouse</span><span class="sxs-lookup"><span data-stu-id="7d54c-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="7d54c-109">Dibujar a intervalos de tiempo</span><span class="sxs-lookup"><span data-stu-id="7d54c-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 



