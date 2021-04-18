---
description: Establecer el bit Done
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Establecer el bit Done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705358"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="77c95-103">Establecer el bit Done</span><span class="sxs-lookup"><span data-stu-id="77c95-103">Setting the Done Bit</span></span>

<span data-ttu-id="77c95-104">COM+ desactivará un objeto activado en JIT en función del estado de una propiedad de contexto, el bit Done, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="77c95-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="77c95-105">Cuando el bit Done está establecido en true, COM+ desactiva el objeto cuando se devuelve la llamada al método actual.</span><span class="sxs-lookup"><span data-stu-id="77c95-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="77c95-106">Cuando el bit Done está establecido en false, el objeto permanece activo cuando se devuelve la llamada al método actual.</span><span class="sxs-lookup"><span data-stu-id="77c95-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="77c95-107">De forma predeterminada, el bit done se establece en false cuando se crea un objeto y se inicializa su contexto.</span><span class="sxs-lookup"><span data-stu-id="77c95-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="77c95-108">(Cualquier objeto activado en JIT se crea en su propio contexto para que tenga su propio bit de finalización). Sin embargo, puede cambiar esta configuración predeterminada en función de cada método mediante la propiedad auto-done.</span><span class="sxs-lookup"><span data-stu-id="77c95-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="77c95-109">Puede establecer el bit Done de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="77c95-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="77c95-110">Usar [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="77c95-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="77c95-111">Usar [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="77c95-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="77c95-112">Usar la propiedad auto-Done</span><span class="sxs-lookup"><span data-stu-id="77c95-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="77c95-113">Usar IContextState</span><span class="sxs-lookup"><span data-stu-id="77c95-113">Using IContextState</span></span>

<span data-ttu-id="77c95-114">Puede usar [**IContextState:: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) para establecer el bit done en true o false.</span><span class="sxs-lookup"><span data-stu-id="77c95-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="77c95-115">Puede usar [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) para obtener el estado actual del bit Done desde el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="77c95-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="77c95-116">Usar IObjectContext</span><span class="sxs-lookup"><span data-stu-id="77c95-116">Using IObjectContext</span></span>

<span data-ttu-id="77c95-117">Puede usar los métodos siguientes en [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para establecer el bit Done mientras configura simultáneamente el bit coherente que se usa para votar en transacciones:</span><span class="sxs-lookup"><span data-stu-id="77c95-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="77c95-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) indica que ha terminado y que ha votado para confirmar la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="77c95-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="77c95-119">Establece el bit Done y el bit coherente en true.</span><span class="sxs-lookup"><span data-stu-id="77c95-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="77c95-120">El [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) indica que ha terminado y termina la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="77c95-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="77c95-121">Establece el bit done en true y el bit coherente en false.</span><span class="sxs-lookup"><span data-stu-id="77c95-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="77c95-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) señala que no ha terminado pero que ha votado para confirmar la transacción.</span><span class="sxs-lookup"><span data-stu-id="77c95-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="77c95-123">Establece el bit done en false y el bit coherente en true.</span><span class="sxs-lookup"><span data-stu-id="77c95-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="77c95-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) indica que no está listo y que vota no confirmar la transacción en este momento, normalmente porque el estado es incoherente.</span><span class="sxs-lookup"><span data-stu-id="77c95-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="77c95-125">Establece el bit Done y el bit coherente en false.</span><span class="sxs-lookup"><span data-stu-id="77c95-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77c95-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77c95-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c95-127">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="77c95-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="77c95-128">Habilitar la activación JIT para un componente</span><span class="sxs-lookup"><span data-stu-id="77c95-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="77c95-129">Agrupación de objetos y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="77c95-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="77c95-130">Transacciones y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="77c95-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



