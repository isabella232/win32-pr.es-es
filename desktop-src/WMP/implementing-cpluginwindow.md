---
title: Implementación de CPluginWindow
description: Implementación de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Complementos de Media Player de Windows, clase CPluginWindow
- complementos, clase CPluginWindow
- Complementos de la interfaz de usuario, clase CPluginWindow
- Complementos de la interfaz de usuario, clase CPluginWindow
- Clase CPluginWindow
- Guía de programación, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774610"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="71cb0-109">Implementación de CPluginWindow</span><span class="sxs-lookup"><span data-stu-id="71cb0-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="71cb0-110">La clase CPluginWindow proporciona la interfaz de usuario al complemento.</span><span class="sxs-lookup"><span data-stu-id="71cb0-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="71cb0-111">En el caso del complemento de la interfaz de usuario de búsqueda, esta clase contiene el código del botón **Buscar** y el código que inicia la página Buscar cuando se hace clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="71cb0-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="71cb0-112">El asistente proporciona una implementación básica de CPluginWindow en el archivo de encabezado CPluginWindow. h.</span><span class="sxs-lookup"><span data-stu-id="71cb0-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="71cb0-113">Para simplificar las cosas, el complemento de la interfaz de usuario de búsqueda modificará este archivo directamente, aunque las adiciones extensas se colocarían normalmente en un archivo CPluginWindow. cpp independiente.</span><span class="sxs-lookup"><span data-stu-id="71cb0-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="71cb0-114">En las secciones siguientes se describe lo que debe hacer para implementar CPluginWindow:</span><span class="sxs-lookup"><span data-stu-id="71cb0-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="71cb0-115">El mapa de mensajes</span><span class="sxs-lookup"><span data-stu-id="71cb0-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="71cb0-116">Constructor</span><span class="sxs-lookup"><span data-stu-id="71cb0-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="71cb0-117">El método OnPaint</span><span class="sxs-lookup"><span data-stu-id="71cb0-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="71cb0-118">Método alcrear</span><span class="sxs-lookup"><span data-stu-id="71cb0-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="71cb0-119">Método de búsqueda</span><span class="sxs-lookup"><span data-stu-id="71cb0-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="71cb0-120">El método LaunchPage</span><span class="sxs-lookup"><span data-stu-id="71cb0-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="71cb0-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71cb0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71cb0-122">**Guía de programación de complementos de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="71cb0-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




