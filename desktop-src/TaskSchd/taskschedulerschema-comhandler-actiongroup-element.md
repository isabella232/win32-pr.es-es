---
title: Elemento comhandler (actionGroup)
description: Especifica una acción que activa un controlador.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento comhandler Programador de tareas
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996847"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="5e7ae-104">Elemento comhandler (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="5e7ae-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="5e7ae-105">Especifica una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="5e7ae-106">[**ActionGroup**](taskschedulerschema-actiongroup-group.md) define el elemento **comhandler** .</span><span class="sxs-lookup"><span data-stu-id="5e7ae-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="5e7ae-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5e7ae-107">Parent element</span></span>



| <span data-ttu-id="5e7ae-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e7ae-108">Element</span></span>                                                         | <span data-ttu-id="5e7ae-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5e7ae-109">Derived from</span></span>                                                       | <span data-ttu-id="5e7ae-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e7ae-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5e7ae-111">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="5e7ae-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="5e7ae-113">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5e7ae-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e7ae-114">Child elements</span></span>



| <span data-ttu-id="5e7ae-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e7ae-115">Element</span></span>                                                               | <span data-ttu-id="5e7ae-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e7ae-116">Type</span></span>                                                         | <span data-ttu-id="5e7ae-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e7ae-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="5e7ae-118">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="5e7ae-119">**guidType**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="5e7ae-120">Especifica el identificador de la clase de controlador.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="5e7ae-121">**Data**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="5e7ae-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5e7ae-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="5e7ae-123">Especifica datos adicionales asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5e7ae-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e7ae-124">Remarks</span></span>

<span data-ttu-id="5e7ae-125">Las aplicaciones definen una acción del controlador COM mediante la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="5e7ae-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="5e7ae-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e7ae-126">Attributes</span></span>

<span data-ttu-id="5e7ae-127">El atributo siguiente se define mediante el tipo complejo [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7ae-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="5e7ae-128">ID: identificador de la acción realizada por la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="5e7ae-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5e7ae-129">Examples</span></span>

<span data-ttu-id="5e7ae-130">En el código XML siguiente se define una acción de controlador COM.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="5e7ae-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e7ae-131">Requirements</span></span>



| <span data-ttu-id="5e7ae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7ae-132">Requirement</span></span> | <span data-ttu-id="5e7ae-133">Value</span><span class="sxs-lookup"><span data-stu-id="5e7ae-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e7ae-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e7ae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e7ae-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e7ae-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e7ae-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e7ae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e7ae-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e7ae-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e7ae-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e7ae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7ae-139">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5e7ae-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





