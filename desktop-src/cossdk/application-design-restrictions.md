---
description: Algunas aplicaciones están diseñadas de forma que evita que se instalen varias instancias de la aplicación en un equipo.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restricciones de diseño de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686436"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="bee46-103">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bee46-103">Application Design Restrictions</span></span>

<span data-ttu-id="bee46-104">Algunas aplicaciones están diseñadas de forma que evita que se instalen varias instancias de la aplicación en un equipo.</span><span class="sxs-lookup"><span data-stu-id="bee46-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="bee46-105">Con este tipo de limitación, una aplicación no puede usar la característica de particiones.</span><span class="sxs-lookup"><span data-stu-id="bee46-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="bee46-106">Es posible que sea necesario modificar las siguientes características de diseño de aplicaciones antes de que se puedan usar particiones para esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="bee46-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="bee46-107">Tablas y matrices</span><span class="sxs-lookup"><span data-stu-id="bee46-107">Tables and Arrays</span></span>

<span data-ttu-id="bee46-108">Algunas aplicaciones crean tablas de base de datos, tablas en memoria o matrices que usan un CLSID como clave de registro única.</span><span class="sxs-lookup"><span data-stu-id="bee46-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="bee46-109">En un equipo sin particiones, esta clave del registro suele ser Computer/CLSID (un CLSID por equipo).</span><span class="sxs-lookup"><span data-stu-id="bee46-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="bee46-110">Por el contrario, en un equipo con particiones, esta clave del registro es el identificador de equipo/partición/ID. de aplicación/CLSID (varias instancias de un CLSID por equipo).</span><span class="sxs-lookup"><span data-stu-id="bee46-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="bee46-111">Dado que la característica particiones permite que existan varias instancias de un CLSID en un equipo, las aplicaciones que contienen elementos de diseño que requieren un CLSID único por equipo podrían verse afectadas negativamente.</span><span class="sxs-lookup"><span data-stu-id="bee46-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="bee46-112">Recursos globales</span><span class="sxs-lookup"><span data-stu-id="bee46-112">Global Resources</span></span>

<span data-ttu-id="bee46-113">Algunas aplicaciones usan recursos globales como memoria compartida, archivos de datos y entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="bee46-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="bee46-114">Esto podría causar problemas si se ejecutan varias instancias de este tipo de aplicación simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="bee46-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="bee46-115">Por ejemplo, si un componente utiliza memoria compartida para interactuar con otros componentes, deberá modificar el componente para que cada instancia del componente asigne su propia memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="bee46-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="bee46-116">Bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="bee46-116">Type Libraries</span></span>

<span data-ttu-id="bee46-117">Las bibliotecas de tipos proporcionan información sobre las interfaces y los métodos de un componente.</span><span class="sxs-lookup"><span data-stu-id="bee46-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="bee46-118">Esta información se usa para varios propósitos, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bee46-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="bee46-119">Serialización de datos entre componentes cuando se realizan llamadas de función</span><span class="sxs-lookup"><span data-stu-id="bee46-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="bee46-120">Ayuda de los componentes en cola de COM+ y los servicios de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="bee46-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="bee46-121">Proporcionar la información correcta en un editor de Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bee46-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="bee46-122">Las referencias a una biblioteca de tipos se instalan en el registro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="bee46-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="bee46-123">Al desarrollar aplicaciones que se invocarán desde particiones, es importante que se instale la versión más reciente de una biblioteca de tipos en el registro.</span><span class="sxs-lookup"><span data-stu-id="bee46-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="bee46-124">Esto garantiza que el editor de Visual Basic que se utiliza obtendrá información precisa sobre los métodos disponibles para ese componente.</span><span class="sxs-lookup"><span data-stu-id="bee46-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee46-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bee46-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee46-126">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="bee46-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="bee46-127">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="bee46-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="bee46-128">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="bee46-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="bee46-129">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="bee46-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



