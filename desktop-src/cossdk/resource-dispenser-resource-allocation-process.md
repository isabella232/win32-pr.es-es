---
description: Proceso de asignación de recursos del dispensador de recursos
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Proceso de asignación de recursos del dispensador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274946"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="9ae2c-103">Proceso de asignación de recursos del dispensador de recursos</span><span class="sxs-lookup"><span data-stu-id="9ae2c-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="9ae2c-104">Cada vez que un dispensador de recursos asigna un recurso a su titular, ocurre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ae2c-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="9ae2c-105">El dispensador de recursos declara un identificador de tipo de recurso (**RESTYPID**), que describe el tipo de recurso necesario.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="9ae2c-106">El dispensador de recursos llama al método [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del titular, pasando este **RESTYPID**.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="9ae2c-107">El titular genera una lista de candidatos a partir de los recursos disponibles.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="9ae2c-108">Los candidatos son recursos que no están inscritos en una transacción o que ya están inscritos en la transacción del objeto que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="9ae2c-109">Estos candidatos se pasan individualmente al método [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , donde se clasifican (en una escala de 0 a 100) por el grado en que el recurso candidato coincide con el **RESTYPID** deseado.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="9ae2c-110">El titular elige el recurso que el dispensador de recursos es el más alto.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="9ae2c-111">El dispensador de recursos puede finalizar el bucle de clasificación al principio asignando al candidato una clasificación de recursos de 100 (un ajuste perfecto).</span><span class="sxs-lookup"><span data-stu-id="9ae2c-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="9ae2c-112">Normalmente, una clasificación de 100 se reserva para los recursos candidatos que ya están inscritos correctamente, a menos que el dispensador de recursos concluya que la inscripción es una operación económica.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="9ae2c-113">Si todos los recursos candidatos (si existen) se clasifican como 0 (inutilizables), se crea un nuevo recurso mediante una llamada a [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span><span class="sxs-lookup"><span data-stu-id="9ae2c-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="9ae2c-114">Si el recurso elegido anteriormente no está ya dado de alta en la transacción del objeto que realiza la llamada, se llama al método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del dispensador de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="9ae2c-115">La llamada al método [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) devuelve al dispensador de recursos con el recurso dado de alta.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ae2c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae2c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae2c-117">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="9ae2c-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="9ae2c-118">Dar de alta un recurso en una transacción</span><span class="sxs-lookup"><span data-stu-id="9ae2c-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="9ae2c-119">Seguimiento de recursos no asignados</span><span class="sxs-lookup"><span data-stu-id="9ae2c-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



