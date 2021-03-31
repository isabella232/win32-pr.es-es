---
description: Diseñar para la implementación
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Diseñar para la implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496037"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="57901-103">Diseñar para la implementación</span><span class="sxs-lookup"><span data-stu-id="57901-103">Designing for Deployment</span></span>

<span data-ttu-id="57901-104">Planear el ámbito de las aplicaciones COM+ es una tarea de diseño importante que debería tener en cuenta en un momento anterior.</span><span class="sxs-lookup"><span data-stu-id="57901-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="57901-105">Los sistemas distribuidos que están pensados para ejecutarse con COM+ deben diseñarse para su implementación con la menor cantidad de configuración individual y para usar cada proceso de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="57901-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="57901-106">También se pueden usar técnicas que le permitirán obtener un rendimiento óptimo al implementar una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="57901-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="57901-107">(Para obtener más información, consulte [implementación de una comunicación más rápida](deploying-for-faster-communication.md)).</span><span class="sxs-lookup"><span data-stu-id="57901-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="57901-108">Cuando se ve con la herramienta administrativa Servicios de componentes, cada aplicación COM+ aparece como una carpeta en la que se agrupan lógicamente los conjuntos de componentes.</span><span class="sxs-lookup"><span data-stu-id="57901-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="57901-109">Aunque puede desplazar componentes individuales entre carpetas de **componentes** de aplicaciones com+ (es decir, de una aplicación a otra), varios servicios establecidos en el nivel de aplicación com+, como la seguridad, pueden ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="57901-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="57901-110">Esta configuración del servicio puede afectar a la portabilidad.</span><span class="sxs-lookup"><span data-stu-id="57901-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="57901-111">Una aplicación de servidor COM+ define un límite de proceso</span><span class="sxs-lookup"><span data-stu-id="57901-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="57901-112">Al crear una nueva aplicación de servidor COM+, realmente está definiendo un nuevo límite de proceso.</span><span class="sxs-lookup"><span data-stu-id="57901-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="57901-113">(Observe la excepción para las aplicaciones de biblioteca que se explican a continuación). Este proceso se convierte en la instancia de la aplicación de control de los componentes contenidos en la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="57901-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="57901-114">Todos estos componentes se ejecutan en proceso en una nueva instancia del programa ejecutable COM+ cada vez que un programa llama a una aplicación COM+ por primera vez.</span><span class="sxs-lookup"><span data-stu-id="57901-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="57901-115">Esto significa que todos los componentes de una determinada carpeta de **componentes** de la aplicación com+ se ejecutan en un único espacio de proceso que actúa como servidor DCOM.</span><span class="sxs-lookup"><span data-stu-id="57901-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="57901-116">Dentro de la aplicación COM+, COM+ administra la memoria, la coordinación con la Coordinador de transacciones distribuidas (DTC), la activación de la instancia del componente Just-in-Time, la detección y recuperación de bloqueos y la seguridad basada en roles.</span><span class="sxs-lookup"><span data-stu-id="57901-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="57901-117">Llamar a través de los límites de la aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="57901-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="57901-118">Dado que cada aplicación COM+ se implementa normalmente como un ejecutable independiente, el efecto de dividir una aplicación distribuida en varias aplicaciones COM+ presenta llamadas COM fuera de proceso cuando los componentes de una aplicación COM+ llaman a los componentes de otra aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="57901-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="57901-119">Esto introduce una degradación del rendimiento debido a la carga adicional de calcular las referencias de los parámetros COM entre los procesos.</span><span class="sxs-lookup"><span data-stu-id="57901-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="57901-120">No hay nada inherentemente incurrido al incurrir en esta penalización de rendimiento. solo tiene que tener en cuenta que se va a producir.</span><span class="sxs-lookup"><span data-stu-id="57901-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="57901-121">En función del tiempo de respuesta requerido, el número de usuarios que solicitarán simultáneamente los servicios empresariales y la carga de inicio agregada que cada componente agrega a cada aplicación COM+, es posible que el impacto de rendimiento atribuible a las llamadas entre aplicaciones sea aceptable.</span><span class="sxs-lookup"><span data-stu-id="57901-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="57901-122">Una posibilidad de eliminar la reducción del rendimiento de la llamada a través de los límites de la aplicación COM+ es marcar una aplicación COM+ determinada como aplicación de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="57901-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="57901-123">Una aplicación de biblioteca COM+ se ejecuta en el proceso del cliente que la crea.</span><span class="sxs-lookup"><span data-stu-id="57901-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="57901-124">Por supuesto, ningún aumento de rendimiento tiene un costo de cero.</span><span class="sxs-lookup"><span data-stu-id="57901-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="57901-125">En este caso, el equilibrio implica las limitaciones de las aplicaciones de biblioteca COM+.</span><span class="sxs-lookup"><span data-stu-id="57901-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="57901-126">Aunque una aplicación de biblioteca puede utilizar la seguridad basada en roles, no admite componentes en cola ni acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="57901-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57901-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57901-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57901-128">Implementación para una comunicación más rápida</span><span class="sxs-lookup"><span data-stu-id="57901-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="57901-129">Diseño para disponibilidad</span><span class="sxs-lookup"><span data-stu-id="57901-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="57901-130">Diseño para la escalabilidad</span><span class="sxs-lookup"><span data-stu-id="57901-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="57901-131">Diseñar para la seguridad</span><span class="sxs-lookup"><span data-stu-id="57901-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



