---
description: Los elementos del panel de control deben estar registrados para que aparezcan en la ventana del panel de control.
title: Registrar elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156689"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="b5f65-103">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-103">Registering Control Panel Items</span></span>

<span data-ttu-id="b5f65-104">Los elementos del panel de control deben estar registrados para que aparezcan en la ventana del panel de control.</span><span class="sxs-lookup"><span data-stu-id="b5f65-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="b5f65-105">Si el elemento del panel de control se implementa como parte de un archivo. exe, se registra como un objeto de comando.</span><span class="sxs-lookup"><span data-stu-id="b5f65-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="b5f65-106">El registro es distinto si el elemento se implementa como un archivo. dll que exporta la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .</span><span class="sxs-lookup"><span data-stu-id="b5f65-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="b5f65-107">En estos temas se explican los requisitos específicos:</span><span class="sxs-lookup"><span data-stu-id="b5f65-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="b5f65-108">Cómo registrar elementos del panel de control ejecutable</span><span class="sxs-lookup"><span data-stu-id="b5f65-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="b5f65-109">Cómo registrar elementos del panel de control DLL</span><span class="sxs-lookup"><span data-stu-id="b5f65-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="b5f65-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5f65-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f65-111">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="b5f65-112">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="b5f65-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="b5f65-113">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="b5f65-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="b5f65-114">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="b5f65-115">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b5f65-116">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="b5f65-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b5f65-117">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="b5f65-118">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="b5f65-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="b5f65-119">Acceder al panel de control en modo seguro en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5f65-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
