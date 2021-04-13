---
description: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496325"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="8f331-103">Estados de recursos agrupados disponibles para el dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8f331-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="8f331-104">En cualquier momento, un recurso está en uso o no está en uso y se da de alta o no se ha dado de alta en una transacción.</span><span class="sxs-lookup"><span data-stu-id="8f331-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="8f331-105">Esto produce cuatro posibles estados de recursos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8f331-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="8f331-106">**Recursos en inventario dado de baja.**</span><span class="sxs-lookup"><span data-stu-id="8f331-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="8f331-107">Un recurso que no está en uso por un objeto y que no está dado de alta en una transacción se encuentra en un inventario dado de baja.</span><span class="sxs-lookup"><span data-stu-id="8f331-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="8f331-108">Un recurso de inventario general está disponible para su asignación.</span><span class="sxs-lookup"><span data-stu-id="8f331-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="8f331-109">**Recursos en inventario dado de alta.**</span><span class="sxs-lookup"><span data-stu-id="8f331-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="8f331-110">Un recurso que no está en uso por un objeto pero está dado de alta en una transacción está en el inventario dado de alta.</span><span class="sxs-lookup"><span data-stu-id="8f331-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="8f331-111">Este tipo de recurso solo está disponible para la asignación a objetos que se ejecutan en la misma transacción.</span><span class="sxs-lookup"><span data-stu-id="8f331-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="8f331-112">Un recurso se desplaza desde el inventario dado de alta hasta el inventario de bajada cuando COM+ notifica al administrador dispensador de que la transacción se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8f331-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="8f331-113">**Recursos en uso dado de baja.**</span><span class="sxs-lookup"><span data-stu-id="8f331-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="8f331-114">Si un recurso se asigna a un objeto y la instancia no se está ejecutando en una transacción o el dispensador de recursos ha identificado el recurso como no transaccional, este recurso tiene el uso dado de baja.</span><span class="sxs-lookup"><span data-stu-id="8f331-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="8f331-115">**Recursos en uso dado de alta.**</span><span class="sxs-lookup"><span data-stu-id="8f331-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="8f331-116">Si un recurso se asigna a un objeto, la instancia se está ejecutando en una transacción y el dispensador de recursos ha dado de alta correctamente el recurso en la transacción, el recurso está en uso dado de alta.</span><span class="sxs-lookup"><span data-stu-id="8f331-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f331-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f331-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f331-118">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8f331-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="8f331-119">Dar de alta un recurso en una transacción</span><span class="sxs-lookup"><span data-stu-id="8f331-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



