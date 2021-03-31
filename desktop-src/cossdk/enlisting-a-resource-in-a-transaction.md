---
description: Dar de alta un recurso en una transacción
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Dar de alta un recurso en una transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423496"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="d0640-103">Dar de alta un recurso en una transacción</span><span class="sxs-lookup"><span data-stu-id="d0640-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="d0640-104">Una vez que se asigna un recurso, pero justo antes de devolver el recurso al dispensador de recursos, el administrador dispensador comprueba con COM+ si el objeto que realiza la llamada se ejecuta dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="d0640-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="d0640-105">Si el objeto que realiza la llamada se ejecuta dentro de una transacción, el administrador dispensador vuelve a llamar al dispensador de recursos y le pide que dé de alta el recurso en la transacción.</span><span class="sxs-lookup"><span data-stu-id="d0640-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="d0640-106">Después, el recurso se devuelve al dispensador de recursos, que, a continuación, lo devuelve a la instancia de que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="d0640-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="d0640-107">El dispensador de recursos debe ser capaz de dar de alta en una transacción OLE con el Coordinador de transacciones distribuidas (DTC).</span><span class="sxs-lookup"><span data-stu-id="d0640-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="d0640-108">La inscripción de transacciones es opcional cuando un dispensador de recursos dispensado en recursos no transaccionales, como la memoria o los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d0640-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="d0640-109">Cuando se completa una transacción, COM+ notifica al administrador del dispensado si se ha confirmado o anulado.</span><span class="sxs-lookup"><span data-stu-id="d0640-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="d0640-110">A continuación, el administrador del dispensador notifica a cada titular de recursos que los recursos que se hayan dado de alta en esta transacción se pueden pasar ahora a inventario general.</span><span class="sxs-lookup"><span data-stu-id="d0640-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0640-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0640-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0640-112">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="d0640-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="d0640-113">Estados de recursos agrupados disponibles para el dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="d0640-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="d0640-114">Proceso de asignación de recursos del dispensador de recursos</span><span class="sxs-lookup"><span data-stu-id="d0640-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



