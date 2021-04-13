---
title: Tipo complejo de requiredPrivilegesType
description: Define los elementos secundarios y la información de secuenciación para el elemento RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- tipo complejo de requiredPrivilegesType Programador de tareas
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493120"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="a1113-104">Tipo complejo de requiredPrivilegesType</span><span class="sxs-lookup"><span data-stu-id="a1113-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="a1113-105">Define los elementos secundarios y la información de secuenciación para el elemento [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1113-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a1113-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1113-106">Child elements</span></span>



| <span data-ttu-id="a1113-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a1113-107">Element</span></span>                                                                           | <span data-ttu-id="a1113-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1113-108">Type</span></span>                                                                  | <span data-ttu-id="a1113-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1113-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="a1113-110">**Privilegio**</span><span class="sxs-lookup"><span data-stu-id="a1113-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="a1113-111">**privilegeType**</span><span class="sxs-lookup"><span data-stu-id="a1113-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="a1113-112">Especifica los privilegios necesarios de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1113-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="a1113-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1113-113">Requirements</span></span>



| <span data-ttu-id="a1113-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1113-114">Requirement</span></span> | <span data-ttu-id="a1113-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1113-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a1113-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1113-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1113-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1113-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a1113-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1113-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1113-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1113-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1113-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1113-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1113-121">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a1113-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a1113-122">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a1113-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





