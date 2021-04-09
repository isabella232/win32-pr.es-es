---
title: Tipo simple de priorityType
description: Define los valores mínimo y máximo para el elemento Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- Programador de tareas de tipo simple priorityType
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079615"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="0d3b2-104">Tipo simple de priorityType</span><span class="sxs-lookup"><span data-stu-id="0d3b2-104">priorityType Simple Type</span></span>

<span data-ttu-id="0d3b2-105">Define los valores mínimo y máximo para el elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0d3b2-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="0d3b2-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="0d3b2-106">Enumeration values</span></span>

<span data-ttu-id="0d3b2-107">El tipo simple **priorityType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="0d3b2-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="0d3b2-108">Value</span><span class="sxs-lookup"><span data-stu-id="0d3b2-108">Value</span></span> | <span data-ttu-id="0d3b2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d3b2-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="0d3b2-110">0</span><span class="sxs-lookup"><span data-stu-id="0d3b2-110">0</span></span>     | <span data-ttu-id="0d3b2-111">Entero mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="0d3b2-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="0d3b2-112">10</span><span class="sxs-lookup"><span data-stu-id="0d3b2-112">10</span></span>    | <span data-ttu-id="0d3b2-113">Entero máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="0d3b2-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0d3b2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3b2-114">Requirements</span></span>



| <span data-ttu-id="0d3b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3b2-115">Requirement</span></span> | <span data-ttu-id="0d3b2-116">Value</span><span class="sxs-lookup"><span data-stu-id="0d3b2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d3b2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3b2-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d3b2-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d3b2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3b2-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d3b2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d3b2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3b2-122">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0d3b2-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0d3b2-123">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0d3b2-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





