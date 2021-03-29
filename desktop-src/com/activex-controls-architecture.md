---
title: Arquitectura de controles ActiveX
description: La tecnología de controles ActiveX se basa en una base de muchos objetos de nivel inferior e interfaces en OLE. Las interfaces exactas disponibles en un control varían con sus capacidades. En esta sección se examina de cerca las capacidades que puede proporcionar un control.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775090"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="a27ec-105">Arquitectura de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="a27ec-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="a27ec-106">La tecnología de controles ActiveX se basa en una base de muchos objetos de nivel inferior e interfaces en OLE.</span><span class="sxs-lookup"><span data-stu-id="a27ec-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="a27ec-107">Las interfaces exactas disponibles en un control varían con sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="a27ec-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="a27ec-108">En esta sección se examina de cerca las capacidades que puede proporcionar un control.</span><span class="sxs-lookup"><span data-stu-id="a27ec-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="a27ec-109">Los controles ActiveX se utilizan para proporcionar los bloques de creación para crear interfaces de usuario en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a27ec-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="a27ec-110">Por ejemplo, un botón que inicia alguna acción en la aplicación contenedora cuando se hace clic en él es un control simple.</span><span class="sxs-lookup"><span data-stu-id="a27ec-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="a27ec-111">Los siguientes aspectos están implicados en la prestación de estos bloques de creación de la interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="a27ec-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="a27ec-112">Un control se puede incrustar dentro de su cliente de contenedor para admitir algunas actividades de interfaz de usuario en el cliente.</span><span class="sxs-lookup"><span data-stu-id="a27ec-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="a27ec-113">Por lo tanto, un control debe proporcionar una representación visual de sí mismo cuando está incrustada en el contenedor y debe proporcionar una manera de guardar su estado, por ejemplo, sus valores de propiedad y su posición dentro de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="a27ec-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="a27ec-114">El cliente debe admitir ser un contenedor con objetos incrustados en él.</span><span class="sxs-lookup"><span data-stu-id="a27ec-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="a27ec-115">Al activar el control con un teclado o un mouse, el usuario final inicia alguna acción en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a27ec-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="a27ec-116">Por lo tanto, un control debe responder a la actividad del teclado y debe poder comunicarse con su cliente para que pueda notificar a su contenedor sus actividades y desencadenar eventos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="a27ec-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="a27ec-117">El cliente también proporciona normalmente un lenguaje de programación a través del cual el usuario final puede iniciar acciones proporcionadas por las propiedades y los métodos del control.</span><span class="sxs-lookup"><span data-stu-id="a27ec-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="a27ec-118">Por lo tanto, un control debe admitir también la automatización y un conjunto de características en tiempo de diseño frente al tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a27ec-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="a27ec-119">Como consecuencia de su rol en la prestación de bloques de creación de la interfaz de usuario, un control suele admitir características en las siguientes áreas mediante tecnologías OLE, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a27ec-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="a27ec-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propiedades y métodos</span><span class="sxs-lookup"><span data-stu-id="a27ec-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-121">Al igual que cualquier objeto OLE, un control puede proporcionar gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="a27ec-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="a27ec-122">El contenedor puede proporcionar propiedades ambiente adicionales y puede admitir la extensión de las propiedades del control a través de la agregación.</span><span class="sxs-lookup"><span data-stu-id="a27ec-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="a27ec-123">Estas características se sitúan en la automatización OLE, las páginas de propiedades, los objetos conectables y las tecnologías de control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a27ec-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a27ec-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="a27ec-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-125">Además de proporcionar propiedades y métodos, un control ActiveX también puede proporcionar interfaces de salida para notificar a su cliente los eventos.</span><span class="sxs-lookup"><span data-stu-id="a27ec-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="a27ec-126">El cliente debe admitir el control de estos eventos.</span><span class="sxs-lookup"><span data-stu-id="a27ec-126">The client must support handling of these events.</span></span> <span data-ttu-id="a27ec-127">Estas características utilizan la automatización OLE y los objetos conectables.</span><span class="sxs-lookup"><span data-stu-id="a27ec-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="a27ec-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Representación visual</span><span class="sxs-lookup"><span data-stu-id="a27ec-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-129">Un control puede admitir la posición y la presentación en su contenedor.</span><span class="sxs-lookup"><span data-stu-id="a27ec-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="a27ec-130">El contenedor coloca el control y determina su tamaño.</span><span class="sxs-lookup"><span data-stu-id="a27ec-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="a27ec-131">Estas características utilizan tecnología de documentos compuestos, incluida la tecnología OLE de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="a27ec-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="a27ec-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Control de teclado</span><span class="sxs-lookup"><span data-stu-id="a27ec-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-133">Un control puede responder a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control.</span><span class="sxs-lookup"><span data-stu-id="a27ec-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="a27ec-134">El contenedor administra la actividad del teclado de todos sus controles incrustados.</span><span class="sxs-lookup"><span data-stu-id="a27ec-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="a27ec-135">Estas características utilizan tecnologías de control y de documentos compuestos.</span><span class="sxs-lookup"><span data-stu-id="a27ec-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a27ec-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span><span class="sxs-lookup"><span data-stu-id="a27ec-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-137">Un control puede guardar su estado.</span><span class="sxs-lookup"><span data-stu-id="a27ec-137">A control can save its state.</span></span> <span data-ttu-id="a27ec-138">El cliente administra la persistencia de sus controles incrustados.</span><span class="sxs-lookup"><span data-stu-id="a27ec-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="a27ec-139">Estas características utilizan tecnologías de almacenamiento estructurado y persistencia de objetos.</span><span class="sxs-lookup"><span data-stu-id="a27ec-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a27ec-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registro y licencias</span><span class="sxs-lookup"><span data-stu-id="a27ec-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="a27ec-141">Un control suele admitir el registro automático y crea un conjunto de entradas del registro cuando se crea una instancia.</span><span class="sxs-lookup"><span data-stu-id="a27ec-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="a27ec-142">También se puede conceder una licencia a un control para ayudar a evitar el uso no autorizado.</span><span class="sxs-lookup"><span data-stu-id="a27ec-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="a27ec-143">La mayoría de estas características implican el control y su contenedor de cliente.</span><span class="sxs-lookup"><span data-stu-id="a27ec-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a27ec-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a27ec-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a27ec-145">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="a27ec-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




