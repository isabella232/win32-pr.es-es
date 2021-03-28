---
description: De forma predeterminada, a partir de los elementos del panel de control de Windows Vista no se muestran cuando Windows se ejecuta en modo seguro.
title: Acceder al panel de control en modo seguro
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984367"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="d3260-103">Acceder al panel de control en modo seguro</span><span class="sxs-lookup"><span data-stu-id="d3260-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="d3260-104">De forma predeterminada, a partir de los elementos del panel de control de Windows Vista no se muestran cuando Windows se ejecuta en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="d3260-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="d3260-105">Para que se pueda ver un nuevo elemento del panel de control en modo seguro, se pueden establecer los valores del registro adecuados para el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="d3260-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="d3260-106">Los valores se interpretan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d3260-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="d3260-107">Value</span><span class="sxs-lookup"><span data-stu-id="d3260-107">Value</span></span> | <span data-ttu-id="d3260-108">Significado</span><span class="sxs-lookup"><span data-stu-id="d3260-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="d3260-109">1</span><span class="sxs-lookup"><span data-stu-id="d3260-109">1</span></span>     | <span data-ttu-id="d3260-110">El elemento debe aparecer solo en el modo seguro mínimo.</span><span class="sxs-lookup"><span data-stu-id="d3260-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="d3260-111">2</span><span class="sxs-lookup"><span data-stu-id="d3260-111">2</span></span>     | <span data-ttu-id="d3260-112">El elemento debe aparecer en modo seguro solo si está habilitada la red.</span><span class="sxs-lookup"><span data-stu-id="d3260-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="d3260-113">3</span><span class="sxs-lookup"><span data-stu-id="d3260-113">3</span></span>     | <span data-ttu-id="d3260-114">El elemento siempre debe aparecer en cualquier forma de modo seguro.</span><span class="sxs-lookup"><span data-stu-id="d3260-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="d3260-115">En este ejemplo se muestran las entradas necesarias para un elemento implementado como un archivo. cpl o. dll.</span><span class="sxs-lookup"><span data-stu-id="d3260-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="d3260-116">Especifica que el elemento debe aparecer en modo seguro con funciones de red.</span><span class="sxs-lookup"><span data-stu-id="d3260-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="d3260-117">En este ejemplo se muestran las entradas necesarias para un elemento implementado como un archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="d3260-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="d3260-118">Especifica que el elemento debe aparecer en cualquier forma de modo seguro.</span><span class="sxs-lookup"><span data-stu-id="d3260-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="d3260-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3260-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3260-120">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="d3260-121">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="d3260-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="d3260-122">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d3260-123">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="d3260-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="d3260-124">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="d3260-125">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d3260-126">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="d3260-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d3260-127">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="d3260-128">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="d3260-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



