---
title: Tipo simple de dayOfMonthType
description: Define los valores posibles para especificar un día del mes.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Programador de tareas de tipo simple dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533891"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="706ca-104">Tipo simple de dayOfMonthType</span><span class="sxs-lookup"><span data-stu-id="706ca-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="706ca-105">Define los valores posibles para especificar un día del mes.</span><span class="sxs-lookup"><span data-stu-id="706ca-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="706ca-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="706ca-106">Patterns</span></span>

<span data-ttu-id="706ca-107">El tipo simple **dayOfMonthType** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="706ca-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="706ca-108">Especifica el día del 1 al 31 del mes o siempre es el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="706ca-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="706ca-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706ca-109">Requirements</span></span>



| <span data-ttu-id="706ca-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="706ca-110">Requirement</span></span> | <span data-ttu-id="706ca-111">Value</span><span class="sxs-lookup"><span data-stu-id="706ca-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="706ca-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="706ca-112">Minimum supported client</span></span><br/> | <span data-ttu-id="706ca-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="706ca-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="706ca-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="706ca-114">Minimum supported server</span></span><br/> | <span data-ttu-id="706ca-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="706ca-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="706ca-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="706ca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706ca-117">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="706ca-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="706ca-118">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="706ca-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





