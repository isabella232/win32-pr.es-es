---
title: Propiedad ComHandlerAction. ClassId
description: Para scripting, obtiene o establece el identificador de la clase de controlador.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Propiedad ClassId Programador de tareas
- Propiedad ClassId Programador de tareas, objeto ComHandlerAction
- Programador de tareas objeto ComHandlerAction, propiedad ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801801"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="38345-106">Propiedad ComHandlerAction. ClassId</span><span class="sxs-lookup"><span data-stu-id="38345-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="38345-107">Para scripting, obtiene o establece el identificador de la clase de controlador.</span><span class="sxs-lookup"><span data-stu-id="38345-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="38345-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38345-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="38345-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="38345-109">Property value</span></span>

<span data-ttu-id="38345-110">Identificador de la clase que define el controlador que se va a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="38345-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="38345-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38345-111">Remarks</span></span>

<span data-ttu-id="38345-112">Al leer o escribir XML, la clase de un controlador COM se especifica en el elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="38345-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="38345-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38345-113">Requirements</span></span>



| <span data-ttu-id="38345-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="38345-114">Requirement</span></span> | <span data-ttu-id="38345-115">Value</span><span class="sxs-lookup"><span data-stu-id="38345-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38345-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38345-116">Minimum supported client</span></span><br/> | <span data-ttu-id="38345-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="38345-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="38345-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38345-118">Minimum supported server</span></span><br/> | <span data-ttu-id="38345-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="38345-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38345-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="38345-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="38345-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38345-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38345-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38345-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38345-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38345-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38345-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="38345-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38345-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="38345-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="38345-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="38345-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





