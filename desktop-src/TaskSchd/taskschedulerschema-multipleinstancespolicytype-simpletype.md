---
title: Tipo simple de multipleInstancesPolicyType
description: Define las constantes de directiva de instancia para el elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Programador de tareas de tipo simple multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996607"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="ba157-104">Tipo simple de multipleInstancesPolicyType</span><span class="sxs-lookup"><span data-stu-id="ba157-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="ba157-105">Define las constantes de directiva de instancia para el elemento [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ba157-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="ba157-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="ba157-106">Enumeration values</span></span>

<span data-ttu-id="ba157-107">El tipo simple **multipleInstancesPolicyType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ba157-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="ba157-108">Value</span><span class="sxs-lookup"><span data-stu-id="ba157-108">Value</span></span>        | <span data-ttu-id="ba157-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba157-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba157-110">Paralelo</span><span class="sxs-lookup"><span data-stu-id="ba157-110">Parallel</span></span>     | <span data-ttu-id="ba157-111">Inicia una nueva instancia mientras se está ejecutando una instancia existente.</span><span class="sxs-lookup"><span data-stu-id="ba157-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="ba157-112">Cola</span><span class="sxs-lookup"><span data-stu-id="ba157-112">Queue</span></span>        | <span data-ttu-id="ba157-113">Inicia una nueva instancia de la tarea después de que todas las demás instancias de la tarea se hayan completado.</span><span class="sxs-lookup"><span data-stu-id="ba157-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="ba157-114">IgnoreNew</span><span class="sxs-lookup"><span data-stu-id="ba157-114">IgnoreNew</span></span>    | <span data-ttu-id="ba157-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ba157-115">Default.</span></span> <span data-ttu-id="ba157-116">No inicia una nueva instancia si se está ejecutando una instancia existente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="ba157-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="ba157-117">StopExisting</span><span class="sxs-lookup"><span data-stu-id="ba157-117">StopExisting</span></span> | <span data-ttu-id="ba157-118">Detiene una instancia existente de la tarea antes de iniciar una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="ba157-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="ba157-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba157-119">Requirements</span></span>



| <span data-ttu-id="ba157-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba157-120">Requirement</span></span> | <span data-ttu-id="ba157-121">Value</span><span class="sxs-lookup"><span data-stu-id="ba157-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba157-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba157-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba157-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba157-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba157-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba157-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba157-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba157-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba157-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba157-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba157-127">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ba157-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ba157-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ba157-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





