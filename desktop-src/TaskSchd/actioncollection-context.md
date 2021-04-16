---
title: ActionCollection. Context (propiedad)
description: En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Propiedad de contexto Programador de tareas
- Propiedad de contexto Programador de tareas, objeto ActionCollection
- Programador de tareas de objeto ActionCollection, propiedad de contexto
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686088"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="ac435-106">ActionCollection. Context (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ac435-106">ActionCollection.Context property</span></span>

<span data-ttu-id="ac435-107">En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.</span><span class="sxs-lookup"><span data-stu-id="ac435-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac435-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac435-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="ac435-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ac435-109">Property value</span></span>

<span data-ttu-id="ac435-110">Identificador de la entidad de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="ac435-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="ac435-111">El identificador que se especifica aquí debe coincidir con el identificador especificado en la propiedad ID de la interfaz IPrincipal que define la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ac435-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac435-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac435-112">Requirements</span></span>



| <span data-ttu-id="ac435-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac435-113">Requirement</span></span> | <span data-ttu-id="ac435-114">Value</span><span class="sxs-lookup"><span data-stu-id="ac435-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac435-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac435-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ac435-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac435-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ac435-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac435-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ac435-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac435-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac435-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ac435-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac435-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ac435-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ac435-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac435-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac435-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac435-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac435-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac435-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac435-124">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ac435-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="ac435-125">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="ac435-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





