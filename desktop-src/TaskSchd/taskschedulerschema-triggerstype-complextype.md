---
title: Tipo complejo de triggersType
description: Define el grupo (triggerGroup) para todos los elementos del desencadenador.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- tipo complejo de triggersType Programador de tareas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686221"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="11f56-104">Tipo complejo de triggersType</span><span class="sxs-lookup"><span data-stu-id="11f56-104">triggersType Complex Type</span></span>

<span data-ttu-id="11f56-105">Define el grupo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) para todos los elementos del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="11f56-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="11f56-106">El grupo [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene la lista de desencadenadores que se pueden usar en una tarea.</span><span class="sxs-lookup"><span data-stu-id="11f56-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="11f56-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f56-107">Requirements</span></span>



| <span data-ttu-id="11f56-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f56-108">Requirement</span></span> | <span data-ttu-id="11f56-109">Value</span><span class="sxs-lookup"><span data-stu-id="11f56-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11f56-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f56-110">Minimum supported client</span></span><br/> | <span data-ttu-id="11f56-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11f56-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11f56-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f56-112">Minimum supported server</span></span><br/> | <span data-ttu-id="11f56-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11f56-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11f56-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="11f56-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f56-115">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11f56-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





