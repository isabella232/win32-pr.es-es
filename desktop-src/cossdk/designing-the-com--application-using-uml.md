---
description: El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación inicial.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Diseñar la aplicación COM+ mediante UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423316"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="eb469-103">Diseñar la aplicación COM+ mediante UML</span><span class="sxs-lookup"><span data-stu-id="eb469-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="eb469-104">El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación inicial.</span><span class="sxs-lookup"><span data-stu-id="eb469-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="eb469-105">El Lenguaje unificado de modelado (UML) es clave para este desarrollo de diseño.</span><span class="sxs-lookup"><span data-stu-id="eb469-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="eb469-106">UML es una notación de modelado para los datos y procesos de la aplicación que combina los procedimientos recomendados del sector del software.</span><span class="sxs-lookup"><span data-stu-id="eb469-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="eb469-107">Dado que el UML divide la aplicación en tres vistas que reflejan la aplicación, así como su empaquetado e implementación, la notación de modelado se amplía bien para admitir el modelado empresarial.</span><span class="sxs-lookup"><span data-stu-id="eb469-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="eb469-108">UML trata tres vistas de la aplicación, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="eb469-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="eb469-109">La vista estática, que está modelada por la información tomada de los escenarios de usuario y los diagramas de clases.</span><span class="sxs-lookup"><span data-stu-id="eb469-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="eb469-110">Vista dinámica, que se modela mediante diagramas de secuencia, colaboración y transición de estado.</span><span class="sxs-lookup"><span data-stu-id="eb469-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="eb469-111">La vista funcional, que es la narrativa más tradicional descriptivo con el pseudocódigo y las especificaciones.</span><span class="sxs-lookup"><span data-stu-id="eb469-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="eb469-112">La información de estas vistas se puede recopilar siguiendo los tres pasos de diseño que funcionan bien con el UML.</span><span class="sxs-lookup"><span data-stu-id="eb469-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="eb469-113">Antes de escribir una sola línea de código, debe crear los siguientes modelos:</span><span class="sxs-lookup"><span data-stu-id="eb469-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="eb469-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modelo conceptual</span><span class="sxs-lookup"><span data-stu-id="eb469-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="eb469-115">Decida qué componentes y servicios son necesarios.</span><span class="sxs-lookup"><span data-stu-id="eb469-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="eb469-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modelo lógico</span><span class="sxs-lookup"><span data-stu-id="eb469-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="eb469-117">Determine el nivel de diseño lógico al que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="eb469-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="eb469-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modelo físico</span><span class="sxs-lookup"><span data-stu-id="eb469-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="eb469-119">Determine dónde residen los componentes físicamente y cómo se van a codificar.</span><span class="sxs-lookup"><span data-stu-id="eb469-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="eb469-120">Estos modelos se pueden usar con las herramientas de casos basados en UML.</span><span class="sxs-lookup"><span data-stu-id="eb469-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="eb469-121">Para obtener más información sobre estos tres modelos de diseño, vea los temas siguientes en esta sección:</span><span class="sxs-lookup"><span data-stu-id="eb469-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="eb469-122">El modelo conceptual: requisitos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="eb469-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="eb469-123">El modelo lógico: definición y planeación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="eb469-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="eb469-124">El modelo físico: arquitectura de la aplicación</span><span class="sxs-lookup"><span data-stu-id="eb469-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="eb469-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb469-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb469-126">Hipótesis y principios de diseño de COM+</span><span class="sxs-lookup"><span data-stu-id="eb469-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="eb469-127">Sugerencias de diseño generales para el uso de COM+</span><span class="sxs-lookup"><span data-stu-id="eb469-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="eb469-128">Optimizar interacciones con el nivel de lógica de negocios de COM+</span><span class="sxs-lookup"><span data-stu-id="eb469-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="eb469-129">Otras herramientas de Microsoft para compilar aplicaciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="eb469-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



