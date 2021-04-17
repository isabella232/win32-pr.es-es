---
title: Detección de objetos innecesarios
description: Si usa inspeccionar para examinar un control simple, como un botón de presionado de aceptar en el accesorio de WordPad de Microsoft, puede ver que estos objetos de ventana primario también contienen varios objetos secundarios invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704587"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="ab0e2-103">Detección de objetos innecesarios</span><span class="sxs-lookup"><span data-stu-id="ab0e2-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="ab0e2-104">Si usa [inspeccionar](inspect-objects.md) para examinar un control simple, como un botón de presionado de aceptar en el accesorio de WordPad de Microsoft, puede ver que estos objetos de ventana primario también contienen varios objetos secundarios invisibles.</span><span class="sxs-lookup"><span data-stu-id="ab0e2-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="ab0e2-105">Estos objetos invisibles tienen el mismo nombre de clase de ventana que el control y tienen la [propiedad State](state-property.md) de [**State \_ System \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ab0e2-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="ab0e2-106">En la tabla siguiente se enumeran los objetos secundarios invisibles que crea Microsoft Active Accessibility para el control.</span><span class="sxs-lookup"><span data-stu-id="ab0e2-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="ab0e2-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab0e2-107">Name</span></span>          | <span data-ttu-id="ab0e2-108">Role</span><span class="sxs-lookup"><span data-stu-id="ab0e2-108">Role</span></span>                                                                  | <span data-ttu-id="ab0e2-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="ab0e2-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="ab0e2-110">Integrado</span><span class="sxs-lookup"><span data-stu-id="ab0e2-110">"System"</span></span>      | [<span data-ttu-id="ab0e2-111">**\_barra de menús del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="ab0e2-112">0</span><span class="sxs-lookup"><span data-stu-id="ab0e2-112">0</span></span>          |
| <span data-ttu-id="ab0e2-113">None</span><span class="sxs-lookup"><span data-stu-id="ab0e2-113">None</span></span>          | [<span data-ttu-id="ab0e2-114">**\_TITLEBAR del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="ab0e2-115">5</span><span class="sxs-lookup"><span data-stu-id="ab0e2-115">5</span></span>          |
| <span data-ttu-id="ab0e2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab0e2-116">"Application"</span></span> | [<span data-ttu-id="ab0e2-117">**\_barra de menús del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="ab0e2-118">0</span><span class="sxs-lookup"><span data-stu-id="ab0e2-118">0</span></span>          |
| <span data-ttu-id="ab0e2-119">Vertical</span><span class="sxs-lookup"><span data-stu-id="ab0e2-119">"Vertical"</span></span>    | [<span data-ttu-id="ab0e2-120">**\_barra de desplazamiento del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="ab0e2-121">5</span><span class="sxs-lookup"><span data-stu-id="ab0e2-121">5</span></span>          |
| <span data-ttu-id="ab0e2-122">Horizontal</span><span class="sxs-lookup"><span data-stu-id="ab0e2-122">"Horizontal"</span></span>  | [<span data-ttu-id="ab0e2-123">**\_barra de desplazamiento del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="ab0e2-124">5</span><span class="sxs-lookup"><span data-stu-id="ab0e2-124">5</span></span>          |
| <span data-ttu-id="ab0e2-125">"Cuadro de tamaño"</span><span class="sxs-lookup"><span data-stu-id="ab0e2-125">"Size Box"</span></span>    | [<span data-ttu-id="ab0e2-126">**\_control del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="ab0e2-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="ab0e2-127">0</span><span class="sxs-lookup"><span data-stu-id="ab0e2-127">0</span></span>          |



 

<span data-ttu-id="ab0e2-128">Los desarrolladores de cliente deben identificar y filtrar estos objetos de ventana primarios y los objetos secundarios invisibles, ya que no proporcionan información significativa a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="ab0e2-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




