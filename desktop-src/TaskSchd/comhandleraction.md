---
title: Objeto ComHandlerAction
description: Objeto de scripting que representa una acción que activa un controlador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Acción del controlador COM Programador de tareas, objeto
- Objeto ComHandlerAction Programador de tareas
- Programador de tareas de objeto ComHandlerAction, descrito
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488938"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="f3211-106">Objeto ComHandlerAction</span><span class="sxs-lookup"><span data-stu-id="f3211-106">ComHandlerAction object</span></span>

<span data-ttu-id="f3211-107">Objeto de scripting que representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="f3211-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="f3211-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3211-108">Members</span></span>

<span data-ttu-id="f3211-109">El objeto **ComHandlerAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3211-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="f3211-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3211-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3211-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3211-111">Properties</span></span>

<span data-ttu-id="f3211-112">El objeto **ComHandlerAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3211-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="f3211-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3211-113">Property</span></span>                                               | <span data-ttu-id="f3211-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f3211-114">Access type</span></span>           | <span data-ttu-id="f3211-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3211-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3211-116">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="f3211-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="f3211-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3211-117">Read/write</span></span><br/> | <span data-ttu-id="f3211-118">Obtiene o establece el identificador de la clase de controlador.</span><span class="sxs-lookup"><span data-stu-id="f3211-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="f3211-119">**Data**</span><span class="sxs-lookup"><span data-stu-id="f3211-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="f3211-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3211-120">Read/write</span></span><br/> | <span data-ttu-id="f3211-121">Obtiene o establece datos adicionales que están asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="f3211-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="f3211-122">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="f3211-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="f3211-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3211-123">Read/write</span></span><br/> | <span data-ttu-id="f3211-124">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="f3211-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f3211-125">Obtiene o establece el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="f3211-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="f3211-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3211-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="f3211-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3211-127">Read-only</span></span><br/>  | <span data-ttu-id="f3211-128">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="f3211-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f3211-129">Obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="f3211-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="f3211-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3211-130">Remarks</span></span>

<span data-ttu-id="f3211-131">Los controladores COM deben implementar la interfaz [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para que el programador de tareas inicie y detenga el controlador.</span><span class="sxs-lookup"><span data-stu-id="f3211-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="f3211-132">A su vez, el controlador COM usa los métodos del objeto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar el estado de vuelta al programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="f3211-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="f3211-133">Al leer o escribir XML, se especifica una acción de controlador COM en el elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="f3211-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3211-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3211-134">Requirements</span></span>



| <span data-ttu-id="f3211-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3211-135">Requirement</span></span> | <span data-ttu-id="f3211-136">Value</span><span class="sxs-lookup"><span data-stu-id="f3211-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3211-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3211-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3211-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3211-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3211-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3211-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3211-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3211-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3211-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f3211-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3211-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f3211-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f3211-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3211-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3211-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3211-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3211-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3211-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3211-146">**TaskHandlerStatus**</span><span class="sxs-lookup"><span data-stu-id="f3211-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="f3211-147">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f3211-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="f3211-148">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f3211-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





