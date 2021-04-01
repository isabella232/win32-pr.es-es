---
title: Elemento Data (comHandlerType)
description: Especifica datos adicionales asociados al controlador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Programador de tareas de elementos de datos
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996846"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="f4949-104">Elemento Data (comHandlerType)</span><span class="sxs-lookup"><span data-stu-id="f4949-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="f4949-105">Especifica datos adicionales asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="f4949-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="f4949-106">El elemento de **datos** se define mediante el tipo complejo de [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f4949-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f4949-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f4949-107">Parent element</span></span>



| <span data-ttu-id="f4949-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4949-108">Element</span></span>                                                                  | <span data-ttu-id="f4949-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f4949-109">Derived from</span></span>                                                             | <span data-ttu-id="f4949-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4949-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="f4949-111">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="f4949-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="f4949-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="f4949-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="f4949-113">Especifica una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="f4949-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f4949-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4949-114">Remarks</span></span>

<span data-ttu-id="f4949-115">Las aplicaciones definen los datos del controlador mediante la propiedad [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de la interfaz [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="f4949-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4949-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4949-116">Requirements</span></span>



| <span data-ttu-id="f4949-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4949-117">Requirement</span></span> | <span data-ttu-id="f4949-118">Value</span><span class="sxs-lookup"><span data-stu-id="f4949-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4949-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4949-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4949-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4949-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4949-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4949-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4949-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4949-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4949-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4949-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4949-124">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="f4949-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





