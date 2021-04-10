---
description: La clave para un buen diseño es planear. Si no está familiarizado con el diseño de una aplicación de tres niveles, consulte la sección titulada diseñar la aplicación COM+ con UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Sugerencias de diseño generales para el uso de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153024"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="1eaf6-104">Sugerencias de diseño generales para el uso de COM+</span><span class="sxs-lookup"><span data-stu-id="1eaf6-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="1eaf6-105">La clave para un buen diseño es planear.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-105">The key to good design is planning.</span></span> <span data-ttu-id="1eaf6-106">Si no está familiarizado con el diseño de una aplicación de tres niveles, consulte la sección titulada [diseñar la aplicación com+ con UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="1eaf6-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="1eaf6-107">La forma en que se crean los componentes COM que componen el nivel intermedio de la aplicación COM+ puede afectar drásticamente al rendimiento, la escalabilidad y la facilidad de implementación.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="1eaf6-108">En los temas siguientes se proporcionan consideraciones de diseño y sugerencias de implementación que debe conocer al diseñar componentes COM.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="1eaf6-109">Tema</span><span class="sxs-lookup"><span data-stu-id="1eaf6-109">Topic</span></span>                                                                   | <span data-ttu-id="1eaf6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1eaf6-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1eaf6-111">Diseño para la escalabilidad</span><span class="sxs-lookup"><span data-stu-id="1eaf6-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="1eaf6-112">Sugiere formas de aumentar la escalabilidad de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="1eaf6-113">Diseño para disponibilidad</span><span class="sxs-lookup"><span data-stu-id="1eaf6-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="1eaf6-114">Describe los servicios que puede usar para mejorar la disponibilidad de la funcionalidad de nivel intermedio en las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="1eaf6-115">Diseñar para la seguridad</span><span class="sxs-lookup"><span data-stu-id="1eaf6-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="1eaf6-116">Describe las formas de configurar la seguridad de forma más eficaz para una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="1eaf6-117">Diseñar para la implementación</span><span class="sxs-lookup"><span data-stu-id="1eaf6-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="1eaf6-118">Describe formas de minimizar los problemas de implementación al diseñar una aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="1eaf6-119">Además, asegúrese de ver cómo [mejorar el rendimiento con la agrupación de objetos](improving-performance-with-object-pooling.md) para las formas de usar la agrupación de objetos de la manera más eficaz.</span><span class="sxs-lookup"><span data-stu-id="1eaf6-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eaf6-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1eaf6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eaf6-121">Hipótesis y principios de diseño de COM+</span><span class="sxs-lookup"><span data-stu-id="1eaf6-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="1eaf6-122">Diseñar la aplicación COM+ mediante UML</span><span class="sxs-lookup"><span data-stu-id="1eaf6-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="1eaf6-123">Optimizar interacciones con el nivel de lógica de negocios de COM+</span><span class="sxs-lookup"><span data-stu-id="1eaf6-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="1eaf6-124">Otras herramientas de Microsoft para compilar aplicaciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="1eaf6-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




