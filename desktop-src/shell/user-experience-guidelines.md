---
description: La responsabilidad principal de cualquier elemento del panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración.
title: Directrices de la experiencia de usuario
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997917"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="1324a-103">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="1324a-103">User Experience Guidelines</span></span>

<span data-ttu-id="1324a-104">La responsabilidad principal de cualquier elemento del panel de control es mostrar una ventana que permita al usuario ver y manipular la configuración.</span><span class="sxs-lookup"><span data-stu-id="1324a-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="1324a-105">Vea las [directrices de experiencia del usuario (UX)](../uxguide/winenv-ctrl-panels.md) de los paneles de control para el comportamiento y el diseño de los elementos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1324a-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="1324a-106">Las instrucciones descritas en ese tema muestran un método de flujo de tareas para organizar un elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1324a-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="1324a-107">Esto coloca la configuración más importante en una página principal.</span><span class="sxs-lookup"><span data-stu-id="1324a-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="1324a-108">Los valores de configuración usados con menos frecuencia se colocan en páginas de radio o se accede a ellos desde los vínculos de un panel lateral.</span><span class="sxs-lookup"><span data-stu-id="1324a-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="1324a-109">El panel de control incluye muchos elementos que siguen estas instrucciones, como el centro de accesibilidad y el centro de redes y recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="1324a-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="1324a-110">Otros elementos del panel de control usan el formato de hoja de propiedades de cuadro de diálogo con pestañas como en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="1324a-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="1324a-111">Entre los ejemplos se incluyen el elemento de mouse y las opciones de Internet.</span><span class="sxs-lookup"><span data-stu-id="1324a-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="1324a-112">El uso del formato de hoja de propiedades debe ser discontinuo.</span><span class="sxs-lookup"><span data-stu-id="1324a-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="1324a-113">Si crea nuevos elementos del panel de control, debe seguir las instrucciones del flujo de tareas.</span><span class="sxs-lookup"><span data-stu-id="1324a-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="1324a-114">En el pasado, los elementos del panel de control se empaquetaban como archivos. cpl.</span><span class="sxs-lookup"><span data-stu-id="1324a-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="1324a-115">Eso ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="1324a-115">That is no longer necessary.</span></span> <span data-ttu-id="1324a-116">Los nuevos elementos del panel de control deben implementarse como un archivo. exe independiente o como una opción de marca de línea de comandos para el archivo ejecutable principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1324a-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="1324a-117">En los sistemas de 64 bits, los elementos del panel de control de 32 bits se muestran en el panel de control cuando se selecciona la opción de **carpeta ver elementos del panel de control de 32 bits** .</span><span class="sxs-lookup"><span data-stu-id="1324a-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="1324a-118">Los elementos de 32 bits deben estar ubicados en la carpeta% SystemRoot% \\ SysWOW64 que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="1324a-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="1324a-119">No requieren ningún registro adicional.</span><span class="sxs-lookup"><span data-stu-id="1324a-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1324a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1324a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1324a-121">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="1324a-122">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1324a-123">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="1324a-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="1324a-124">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="1324a-125">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1324a-126">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="1324a-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1324a-127">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="1324a-128">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="1324a-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="1324a-129">Acceder al panel de control en modo seguro</span><span class="sxs-lookup"><span data-stu-id="1324a-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



