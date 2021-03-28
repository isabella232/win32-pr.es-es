---
description: Antes de pintar, el sistema debe preparar el dispositivo de pantalla para las operaciones de dibujo.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Mostrar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984990"
---
# <a name="display-devices"></a><span data-ttu-id="97054-103">Mostrar dispositivos</span><span class="sxs-lookup"><span data-stu-id="97054-103">Display Devices</span></span>

<span data-ttu-id="97054-104">Antes de pintar, el sistema debe preparar el dispositivo de pantalla para las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="97054-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="97054-105">Un contexto de dispositivo de pantalla define un conjunto de objetos gráficos y sus atributos asociados, así como los modos gráficos que afectan a la salida.</span><span class="sxs-lookup"><span data-stu-id="97054-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="97054-106">El sistema prepara cada contexto de dispositivo de presentación para la salida en una ventana, estableciendo los objetos de dibujo, los colores y los modos de la ventana en lugar del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="97054-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="97054-107">Cuando la aplicación proporciona el contexto de mostrar el dispositivo a través de llamadas a funciones GDI, GDI usa la información en el contexto para generar la salida en la ventana especificada sin intrusión en otras ventanas u otras partes de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="97054-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="97054-108">El sistema proporciona cinco tipos de contextos de dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="97054-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="97054-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="97054-109">Type</span></span>                                           | <span data-ttu-id="97054-110">Significado</span><span class="sxs-lookup"><span data-stu-id="97054-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97054-111">normal</span><span class="sxs-lookup"><span data-stu-id="97054-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="97054-112">Permite dibujar en el área de cliente de una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="97054-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="97054-113">class</span><span class="sxs-lookup"><span data-stu-id="97054-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="97054-114">Permite dibujar en el área de cliente de una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="97054-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="97054-115">parent</span><span class="sxs-lookup"><span data-stu-id="97054-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="97054-116">Permite dibujar en cualquier parte de la ventana.</span><span class="sxs-lookup"><span data-stu-id="97054-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="97054-117">Aunque el contexto de dispositivo primario también permite dibujar en la ventana primaria, no está diseñado para usarse de esta manera.</span><span class="sxs-lookup"><span data-stu-id="97054-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="97054-118">private</span><span class="sxs-lookup"><span data-stu-id="97054-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="97054-119">Permite dibujar en el área de cliente de una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="97054-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="97054-120">periodo</span><span class="sxs-lookup"><span data-stu-id="97054-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="97054-121">Permite dibujar en cualquier parte de la ventana.</span><span class="sxs-lookup"><span data-stu-id="97054-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="97054-122">El sistema proporciona un contexto de dispositivo común, de clase, primario o privado a una ventana basada en el tipo de contexto de dispositivo de pantalla especificado en el estilo de clase de la ventana.</span><span class="sxs-lookup"><span data-stu-id="97054-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="97054-123">El sistema proporciona un contexto de dispositivo de ventana solo cuando la aplicación solicita explícitamente uno, por ejemplo, mediante una llamada a la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) .</span><span class="sxs-lookup"><span data-stu-id="97054-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="97054-124">En todos los casos, una aplicación puede usar la función [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) para determinar qué ventana representa un DC de visualización actualmente.</span><span class="sxs-lookup"><span data-stu-id="97054-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="97054-125">En esta sección se proporciona información sobre los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="97054-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="97054-126">Mostrar caché de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="97054-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="97054-127">Mostrar valores predeterminados de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="97054-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="97054-128">Contextos de dispositivo de pantalla comunes</span><span class="sxs-lookup"><span data-stu-id="97054-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="97054-129">Contextos de dispositivo de pantalla privada</span><span class="sxs-lookup"><span data-stu-id="97054-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="97054-130">Contextos de dispositivo de pantalla primaria</span><span class="sxs-lookup"><span data-stu-id="97054-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="97054-131">La clase muestra contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="97054-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="97054-132">Ventana Mostrar contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="97054-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="97054-133">Contextos de dispositivo de pantalla primaria</span><span class="sxs-lookup"><span data-stu-id="97054-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



