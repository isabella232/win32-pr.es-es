---
description: Puede usar el mensaje de \_ pintura de WM para llevar a cabo el dibujo necesario para mostrar la información.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Usar el mensaje de WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276452"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="fb72b-103">Usar el mensaje de Paint de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb72b-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="fb72b-104">Puede usar el mensaje [**de \_ pintura de WM**](wm-paint.md) para llevar a cabo el dibujo necesario para mostrar la información.</span><span class="sxs-lookup"><span data-stu-id="fb72b-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="fb72b-105">Dado que el sistema envía \_ mensajes de WM Paint a la aplicación cuando se debe actualizar la ventana o cuando se solicita explícitamente una actualización, se puede consolidar el código para dibujar en el procedimiento de ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb72b-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="fb72b-106">Después, puede usar este código cada vez que la aplicación deba dibujar información nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="fb72b-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="fb72b-107">En las secciones siguientes se muestran varias formas de usar el \_ mensaje de Paint de WM para dibujar en una ventana:</span><span class="sxs-lookup"><span data-stu-id="fb72b-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="fb72b-108">Dibujo en el área cliente</span><span class="sxs-lookup"><span data-stu-id="fb72b-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="fb72b-109">Volver a dibujar todo el área cliente</span><span class="sxs-lookup"><span data-stu-id="fb72b-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="fb72b-110">Volver a dibujar en la región de actualización</span><span class="sxs-lookup"><span data-stu-id="fb72b-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="fb72b-111">Invalidar el área de cliente</span><span class="sxs-lookup"><span data-stu-id="fb72b-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="fb72b-112">Dibujar una ventana minimizada</span><span class="sxs-lookup"><span data-stu-id="fb72b-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="fb72b-113">Dibujo de un fondo de ventana personalizado</span><span class="sxs-lookup"><span data-stu-id="fb72b-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



