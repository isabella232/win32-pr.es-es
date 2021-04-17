---
title: Objeto TaskNamedValuePair
description: Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Objeto TaskNamedValuePair Programador de tareas
- Programador de tareas de objeto TaskNamedValuePair, descrito
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685886"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="c1bca-105">Objeto TaskNamedValuePair</span><span class="sxs-lookup"><span data-stu-id="c1bca-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="c1bca-106">Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.</span><span class="sxs-lookup"><span data-stu-id="c1bca-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="c1bca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1bca-107">Members</span></span>

<span data-ttu-id="c1bca-108">El objeto **TaskNamedValuePair** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c1bca-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="c1bca-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1bca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1bca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1bca-110">Properties</span></span>

<span data-ttu-id="c1bca-111">El objeto **TaskNamedValuePair** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c1bca-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="c1bca-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1bca-112">Property</span></span>                                             | <span data-ttu-id="c1bca-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1bca-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1bca-114">**Name**</span><span class="sxs-lookup"><span data-stu-id="c1bca-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="c1bca-115">Obtiene o establece el nombre asociado a un valor en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="c1bca-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="c1bca-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="c1bca-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="c1bca-117">Obtiene o establece el valor asociado a un nombre en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="c1bca-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1bca-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1bca-118">Remarks</span></span>

<span data-ttu-id="c1bca-119">Al leer o escribir su propio XML para una tarea, se especifica un par de nombre y valor mediante el elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="c1bca-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1bca-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1bca-120">Requirements</span></span>



| <span data-ttu-id="c1bca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bca-121">Requirement</span></span> | <span data-ttu-id="c1bca-122">Value</span><span class="sxs-lookup"><span data-stu-id="c1bca-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bca-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1bca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1bca-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c1bca-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c1bca-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1bca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1bca-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1bca-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1bca-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c1bca-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1bca-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1bca-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1bca-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1bca-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1bca-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1bca-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1bca-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1bca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bca-132">**TaskNamedValueCollection**</span><span class="sxs-lookup"><span data-stu-id="c1bca-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





