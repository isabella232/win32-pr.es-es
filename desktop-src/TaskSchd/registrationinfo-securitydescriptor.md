---
title: RegistrationInfo. SecurityDescriptor (propiedad)
description: En el caso de scripting, obtiene o establece el descriptor de seguridad de la tarea.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propiedad SecurityDescriptor Programador de tareas
- Propiedad SecurityDescriptor Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685840"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="d9c28-106">RegistrationInfo. SecurityDescriptor (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d9c28-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="d9c28-107">En el caso de scripting, obtiene o establece el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9c28-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="d9c28-108">Si se proporciona un descriptor de seguridad diferente durante el registro de la tarea, reemplazará el conjunto de descriptores de seguridad por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d9c28-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c28-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9c28-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="d9c28-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9c28-110">Property value</span></span>

<span data-ttu-id="d9c28-111">Descriptor de seguridad asociado a la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9c28-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c28-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9c28-112">Remarks</span></span>

<span data-ttu-id="d9c28-113">Al leer o escribir XML para una tarea, el descriptor de seguridad de la tarea se especifica mediante el elemento [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d9c28-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c28-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9c28-114">Requirements</span></span>



| <span data-ttu-id="d9c28-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9c28-115">Requirement</span></span> | <span data-ttu-id="d9c28-116">Value</span><span class="sxs-lookup"><span data-stu-id="d9c28-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c28-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9c28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c28-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9c28-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9c28-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9c28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c28-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9c28-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9c28-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9c28-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9c28-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9c28-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9c28-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9c28-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9c28-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9c28-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c28-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9c28-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c28-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d9c28-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





