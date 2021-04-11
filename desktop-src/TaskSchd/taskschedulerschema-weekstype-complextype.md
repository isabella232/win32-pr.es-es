---
title: Tipo complejo de weeksType
description: Define el elemento secundario y la información de secuenciación para el elemento Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- tipo complejo de weeksType Programador de tareas
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150842"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="028a1-104">Tipo complejo de weeksType</span><span class="sxs-lookup"><span data-stu-id="028a1-104">weeksType Complex Type</span></span>

<span data-ttu-id="028a1-105">Define el elemento secundario y la información de secuenciación para el elemento [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="028a1-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="028a1-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="028a1-106">Child elements</span></span>



| <span data-ttu-id="028a1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="028a1-107">Element</span></span>                                                    | <span data-ttu-id="028a1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="028a1-108">Type</span></span>                                                        | <span data-ttu-id="028a1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="028a1-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="028a1-110">**Semana**</span><span class="sxs-lookup"><span data-stu-id="028a1-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="028a1-111">**weekType**</span><span class="sxs-lookup"><span data-stu-id="028a1-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="028a1-112">Especifica la semana en la que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="028a1-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="028a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="028a1-113">Requirements</span></span>



| <span data-ttu-id="028a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="028a1-114">Requirement</span></span> | <span data-ttu-id="028a1-115">Value</span><span class="sxs-lookup"><span data-stu-id="028a1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="028a1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="028a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="028a1-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="028a1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="028a1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="028a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="028a1-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="028a1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="028a1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="028a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028a1-121">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="028a1-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





