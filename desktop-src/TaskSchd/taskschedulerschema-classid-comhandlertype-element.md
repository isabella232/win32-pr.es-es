---
title: ClassId (comHandlerType), elemento
description: Especifica el identificador de la clase de controlador.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassId (Programador de tareas del elemento)
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493132"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="d9519-104">ClassId (comHandlerType), elemento</span><span class="sxs-lookup"><span data-stu-id="d9519-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="d9519-105">Especifica el identificador de la clase de controlador.</span><span class="sxs-lookup"><span data-stu-id="d9519-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="d9519-106">El elemento **ClassID** se define mediante el tipo complejo [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d9519-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d9519-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d9519-107">Parent element</span></span>



| <span data-ttu-id="d9519-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9519-108">Element</span></span>                                                                  | <span data-ttu-id="d9519-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d9519-109">Derived from</span></span>                                                             | <span data-ttu-id="d9519-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9519-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="d9519-111">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="d9519-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="d9519-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="d9519-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="d9519-113">Especifica una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="d9519-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9519-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9519-114">Remarks</span></span>

<span data-ttu-id="d9519-115">Las aplicaciones definen el identificador de clase mediante la propiedad [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) de la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="d9519-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9519-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9519-116">Requirements</span></span>



| <span data-ttu-id="d9519-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9519-117">Requirement</span></span> | <span data-ttu-id="d9519-118">Value</span><span class="sxs-lookup"><span data-stu-id="d9519-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9519-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9519-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9519-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9519-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9519-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9519-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9519-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9519-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9519-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9519-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9519-124">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="d9519-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





