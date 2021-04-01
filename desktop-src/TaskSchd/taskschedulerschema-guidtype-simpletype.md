---
title: tipo simple de guidType (Programador de tareas)
description: Define el patrón para los GUID válidos.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- Programador de tareas de tipo simple guidType
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150850"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="5a142-104">tipo simple de guidType (Programador de tareas)</span><span class="sxs-lookup"><span data-stu-id="5a142-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="5a142-105">Define el patrón para los GUID válidos.</span><span class="sxs-lookup"><span data-stu-id="5a142-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5a142-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="5a142-106">Patterns</span></span>

<span data-ttu-id="5a142-107">El tipo simple **guidType** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="5a142-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="5a142-108">Número único de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="5a142-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a142-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a142-109">Requirements</span></span>



| <span data-ttu-id="5a142-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a142-110">Requirement</span></span> | <span data-ttu-id="5a142-111">Value</span><span class="sxs-lookup"><span data-stu-id="5a142-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a142-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a142-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5a142-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a142-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a142-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a142-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5a142-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a142-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a142-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a142-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a142-117">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5a142-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5a142-118">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5a142-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





