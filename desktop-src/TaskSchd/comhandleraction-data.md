---
title: Propiedad ComHandlerAction. Data
description: Para scripting, obtiene o establece datos adicionales asociados al controlador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Programador de tareas de propiedades de datos
- Programador de tareas de propiedad de datos, objeto ComHandlerAction
- Programador de tareas de objeto ComHandlerAction, propiedad de datos
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422549"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="bef3b-106">Propiedad ComHandlerAction. Data</span><span class="sxs-lookup"><span data-stu-id="bef3b-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="bef3b-107">Para scripting, obtiene o establece datos adicionales asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="bef3b-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef3b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bef3b-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="bef3b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bef3b-109">Property value</span></span>

<span data-ttu-id="bef3b-110">Argumentos necesarios para el controlador.</span><span class="sxs-lookup"><span data-stu-id="bef3b-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="bef3b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bef3b-111">Remarks</span></span>

<span data-ttu-id="bef3b-112">Al leer o escribir XML, los datos de un controlador COM se especifican en el elemento de [**datos**](taskschedulerschema-data-comhandlertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="bef3b-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef3b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef3b-113">Requirements</span></span>



| <span data-ttu-id="bef3b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef3b-114">Requirement</span></span> | <span data-ttu-id="bef3b-115">Value</span><span class="sxs-lookup"><span data-stu-id="bef3b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bef3b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef3b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bef3b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bef3b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bef3b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef3b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bef3b-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bef3b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bef3b-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bef3b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="bef3b-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bef3b-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bef3b-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bef3b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef3b-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bef3b-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef3b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bef3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef3b-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="bef3b-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bef3b-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="bef3b-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





