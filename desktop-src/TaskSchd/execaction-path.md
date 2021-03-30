---
title: ExecAction. Path (propiedad)
description: En el caso de scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Propiedad path Programador de tareas
- Propiedad path Programador de tareas, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801795"
---
# <a name="execactionpath-property"></a><span data-ttu-id="0a329-106">ExecAction. Path (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0a329-106">ExecAction.Path property</span></span>

<span data-ttu-id="0a329-107">En el caso de scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0a329-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a329-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a329-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="0a329-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0a329-109">Property value</span></span>

<span data-ttu-id="0a329-110">Ruta de acceso al archivo ejecutable que va a ejecutar la acción.</span><span class="sxs-lookup"><span data-stu-id="0a329-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a329-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a329-111">Remarks</span></span>

<span data-ttu-id="0a329-112">Esta acción realiza una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0a329-112">This action performs a command-line operation.</span></span> <span data-ttu-id="0a329-113">Por ejemplo, la acción podría ejecutar un script o iniciar un ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0a329-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="0a329-114">Al leer o escribir XML, la ruta de acceso de la operación de línea de comandos se especifica en el elemento [**Command**](taskschedulerschema-command-exectype-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0a329-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0a329-115">La ruta de acceso se comprueba para asegurarse de que es válida cuando se registra la tarea, no cuando se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0a329-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a329-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a329-116">Requirements</span></span>



| <span data-ttu-id="0a329-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a329-117">Requirement</span></span> | <span data-ttu-id="0a329-118">Value</span><span class="sxs-lookup"><span data-stu-id="0a329-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a329-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a329-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a329-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a329-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0a329-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a329-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a329-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a329-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a329-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a329-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a329-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a329-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a329-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a329-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a329-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a329-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a329-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a329-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a329-128">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="0a329-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="0a329-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0a329-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





