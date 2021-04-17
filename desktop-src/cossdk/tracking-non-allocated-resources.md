---
description: Seguimiento de recursos no asignados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Seguimiento de recursos no asignados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705357"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="9b028-103">Seguimiento de recursos no asignados</span><span class="sxs-lookup"><span data-stu-id="9b028-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="9b028-104">El administrador dispensador puede realizar el seguimiento de un recurso que no está inventariado, en función del conocimiento de la duración del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b028-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="9b028-105">Cuando se libera un recurso del que se ha realizado un seguimiento, se destruye y, por lo tanto, no se devuelve al inventario.</span><span class="sxs-lookup"><span data-stu-id="9b028-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="9b028-106">Este modo de solo seguimiento para los recursos que son económicos para crear y destruir es más útil que almacenarlos en el inventario.</span><span class="sxs-lookup"><span data-stu-id="9b028-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="9b028-107">Este modo también es útil para administrar un dispensador de memoria o para un recurso que es difícil de inventariar porque hay demasiados tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9b028-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="9b028-108">En el modo de solo seguimiento, un dispensador de recursos crea directamente un recurso solicitado en lugar de solicitar al administrador dispensado que asigne uno de inventario.</span><span class="sxs-lookup"><span data-stu-id="9b028-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="9b028-109">Antes de devolver este recurso al componente de la aplicación solicitante, el dispensador de recursos indica al administrador dispensador que realice un seguimiento del recurso, lo que garantiza que incluso si el componente no tiene que liberar el recurso, el administrador del dispensador lo hará cuando la duración del componente sea superior.</span><span class="sxs-lookup"><span data-stu-id="9b028-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b028-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b028-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b028-111">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="9b028-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



