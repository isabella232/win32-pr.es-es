---
title: Tipo simple de weekType
description: Define los valores que se pueden usar en el elemento Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- Programador de tareas de tipo simple weekType
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150092"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="a4ed8-104">Tipo simple de weekType</span><span class="sxs-lookup"><span data-stu-id="a4ed8-104">weekType Simple Type</span></span>

<span data-ttu-id="a4ed8-105">Define los valores que se pueden usar en el elemento [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a4ed8-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="a4ed8-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="a4ed8-106">Patterns</span></span>

<span data-ttu-id="a4ed8-107">El tipo simple **weekType** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="a4ed8-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="a4ed8-108">Especifica el primer hasta la cuarta semana del mes (1-4) o siempre la última semana del mes.</span><span class="sxs-lookup"><span data-stu-id="a4ed8-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ed8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4ed8-109">Requirements</span></span>



| <span data-ttu-id="a4ed8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4ed8-110">Requirement</span></span> | <span data-ttu-id="a4ed8-111">Value</span><span class="sxs-lookup"><span data-stu-id="a4ed8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4ed8-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4ed8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ed8-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a4ed8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4ed8-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4ed8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ed8-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4ed8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4ed8-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4ed8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ed8-117">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a4ed8-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a4ed8-118">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a4ed8-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





