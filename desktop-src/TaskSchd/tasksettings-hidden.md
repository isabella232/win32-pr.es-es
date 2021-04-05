---
title: Propiedad TaskSettings. Hidden
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Propiedad Hidden Programador de tareas
- Propiedad Hidden Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803205"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="93c37-106">Propiedad TaskSettings. Hidden</span><span class="sxs-lookup"><span data-stu-id="93c37-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="93c37-107">En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="93c37-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="93c37-108">Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador principal" que hace que todas las tareas sean visibles en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="93c37-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="93c37-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="93c37-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c37-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93c37-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="93c37-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="93c37-111">Property value</span></span>

<span data-ttu-id="93c37-112">Si **es true**, el valor indica que la tarea no estará visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="93c37-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="93c37-113">Si **es false**, la tarea estará visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="93c37-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="93c37-114">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="93c37-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c37-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93c37-115">Remarks</span></span>

<span data-ttu-id="93c37-116">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**oculto (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="93c37-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c37-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93c37-117">Requirements</span></span>



| <span data-ttu-id="93c37-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c37-118">Requirement</span></span> | <span data-ttu-id="93c37-119">Value</span><span class="sxs-lookup"><span data-stu-id="93c37-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93c37-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93c37-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93c37-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="93c37-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="93c37-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93c37-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93c37-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="93c37-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93c37-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="93c37-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="93c37-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93c37-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93c37-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93c37-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c37-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c37-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c37-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="93c37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c37-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="93c37-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





