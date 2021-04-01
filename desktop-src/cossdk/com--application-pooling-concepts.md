---
description: La agrupación de aplicaciones COM+ permite escalar los procesos de un solo subproceso, de manera similar a la forma en que la agrupación de subprocesos permite escalar objetos de un solo subproceso.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceptos de agrupación de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907103"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="2bd1c-103">Conceptos de agrupación de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="2bd1c-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="2bd1c-104">La agrupación de aplicaciones COM+ permite escalar los procesos de un solo subproceso, de manera similar a la forma en que la agrupación de subprocesos permite escalar objetos de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="2bd1c-105">La agrupación de aplicaciones también puede ayudar a recuperarse de los errores en procesos únicos proporcionando otros procesos en ejecución capaces de controlar las activaciones.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="2bd1c-106">Las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="2bd1c-107">Todos los métodos de la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) admiten la agrupación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="2bd1c-108">La agrupación de aplicaciones COM+ se puede configurar por aplicación mediante la propiedad ConcurrentApps del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) en la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd1c-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="2bd1c-109">ConcurrentApps es un valor entero que especifica el número máximo de procesos Dllhost simultáneos que deben iniciarse para realizar activaciones de servicio para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="2bd1c-110">Esta propiedad se puede establecer mediante la herramienta de administración de servicios de componentes o mediante programación.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="2bd1c-111">Si la propiedad ConcurrentApps se establece en 1, que es el valor predeterminado, se deshabilita el servicio de agrupación de aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bd1c-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bd1c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd1c-113">Tareas de agrupación de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="2bd1c-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="2bd1c-114">Conceptos de reciclaje de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="2bd1c-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



