---
description: Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Acerca del dibujo y el dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997297"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="6e97d-103">Acerca del dibujo y el dibujo</span><span class="sxs-lookup"><span data-stu-id="6e97d-103">About Painting and Drawing</span></span>

<span data-ttu-id="6e97d-104">Casi todas las aplicaciones usan la pantalla para mostrar los datos que manipulan.</span><span class="sxs-lookup"><span data-stu-id="6e97d-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="6e97d-105">Una aplicación pinta imágenes, dibuja figuras y escribe texto para que el usuario pueda ver los datos a medida que se crean, editan e imprimen.</span><span class="sxs-lookup"><span data-stu-id="6e97d-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="6e97d-106">Microsoft Windows proporciona una amplia compatibilidad para dibujar y dibujar, pero, debido a la naturaleza de los sistemas operativos de multitarea, las aplicaciones deben cooperar entre sí al tener acceso a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6e97d-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="6e97d-107">Para mantener todas las aplicaciones en funcionamiento sin problemas y de forma cooperativa, el sistema administra todos los resultados en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6e97d-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="6e97d-108">Las aplicaciones usan Windows como dispositivo de salida principal en lugar de la propia pantalla.</span><span class="sxs-lookup"><span data-stu-id="6e97d-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="6e97d-109">El sistema proporciona los contextos de dispositivo de pantalla que se corresponden de forma única a las ventanas.</span><span class="sxs-lookup"><span data-stu-id="6e97d-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="6e97d-110">Las aplicaciones usan contextos de dispositivo de pantalla para dirigir su salida a las ventanas especificadas.</span><span class="sxs-lookup"><span data-stu-id="6e97d-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="6e97d-111">Dibujar en una ventana (dirigir la salida a ella) impide que una aplicación interfiera con la salida de otras aplicaciones y permite que las aplicaciones coexistan entre sí mientras se sigue aprovechando al máximo las capacidades de gráficos del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e97d-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="6e97d-112">Cuándo dibujar en una ventana</span><span class="sxs-lookup"><span data-stu-id="6e97d-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="6e97d-113">Mensaje de \_ dibujo de WM</span><span class="sxs-lookup"><span data-stu-id="6e97d-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="6e97d-114">Dibujo sin el mensaje de pintura de WM \_</span><span class="sxs-lookup"><span data-stu-id="6e97d-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="6e97d-115">Sistema de coordenadas de ventana</span><span class="sxs-lookup"><span data-stu-id="6e97d-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="6e97d-116">Regiones de ventana</span><span class="sxs-lookup"><span data-stu-id="6e97d-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="6e97d-117">Fondo de la ventana</span><span class="sxs-lookup"><span data-stu-id="6e97d-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="6e97d-118">Ventanas minimizadas</span><span class="sxs-lookup"><span data-stu-id="6e97d-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="6e97d-119">Ventanas cambiadas de tamaño</span><span class="sxs-lookup"><span data-stu-id="6e97d-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="6e97d-120">Área no cliente</span><span class="sxs-lookup"><span data-stu-id="6e97d-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="6e97d-121">Región de actualización de la ventana secundaria</span><span class="sxs-lookup"><span data-stu-id="6e97d-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="6e97d-122">Mostrar dispositivos</span><span class="sxs-lookup"><span data-stu-id="6e97d-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="6e97d-123">Bloqueo de actualización de ventana</span><span class="sxs-lookup"><span data-stu-id="6e97d-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="6e97d-124">Rectángulo delimitador acumulado</span><span class="sxs-lookup"><span data-stu-id="6e97d-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



