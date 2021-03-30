---
title: Interfaz IReconcileInitiator
description: Expone métodos que proporcionan el reconciliador del maletín con los medios para notificar al iniciador de su progreso, establecer un objeto de terminación y solicitar una versión determinada de un documento. El iniciador es responsable de la implementación de esta interfaz.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Interfaz IReconcileInitiator características del entorno heredado de Windows
- Interfaz IReconcileInitiator características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802348"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="9cc65-106">Interfaz IReconcileInitiator</span><span class="sxs-lookup"><span data-stu-id="9cc65-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="9cc65-107">Expone métodos que proporcionan el reconciliador del maletín con los medios para notificar al iniciador de su progreso, establecer un objeto de terminación y solicitar una versión determinada de un documento.</span><span class="sxs-lookup"><span data-stu-id="9cc65-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="9cc65-108">El iniciador es responsable de la implementación de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="9cc65-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="9cc65-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9cc65-109">Members</span></span>

<span data-ttu-id="9cc65-110">La interfaz **IReconcileInitiator** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9cc65-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9cc65-111">**IReconcileInitiator** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9cc65-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="9cc65-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9cc65-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9cc65-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9cc65-113">Methods</span></span>

<span data-ttu-id="9cc65-114">La interfaz **IReconcileInitiator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9cc65-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="9cc65-115">Método</span><span class="sxs-lookup"><span data-stu-id="9cc65-115">Method</span></span>                                                                 | <span data-ttu-id="9cc65-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cc65-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cc65-117">**SetAbortCallback**</span><span class="sxs-lookup"><span data-stu-id="9cc65-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="9cc65-118">Establece el objeto a través del cual el iniciador puede finalizar de forma asincrónica una conciliación.</span><span class="sxs-lookup"><span data-stu-id="9cc65-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="9cc65-119">Un reconciliador de maletín normalmente establece este objeto para las reconciliaciones que son largas o que implican la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="9cc65-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="9cc65-120">**SetProgressFeedback**</span><span class="sxs-lookup"><span data-stu-id="9cc65-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="9cc65-121">Indica la cantidad de progreso que ha realizado el reconciliador del maletín para completar la conciliación.</span><span class="sxs-lookup"><span data-stu-id="9cc65-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="9cc65-122">La cantidad es una fracción y se calcula como el cociente de los parámetros *ulProgress* y *ulProgressMax* .</span><span class="sxs-lookup"><span data-stu-id="9cc65-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="9cc65-123">Los reconciliadores deben llamar a este método periódicamente durante su proceso de conciliación.</span><span class="sxs-lookup"><span data-stu-id="9cc65-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9cc65-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cc65-124">Requirements</span></span>



| <span data-ttu-id="9cc65-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc65-125">Requirement</span></span> | <span data-ttu-id="9cc65-126">Value</span><span class="sxs-lookup"><span data-stu-id="9cc65-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc65-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cc65-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc65-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9cc65-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9cc65-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cc65-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc65-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cc65-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9cc65-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cc65-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc65-132"><dt>Shell32.dll (versión 4,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc65-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

