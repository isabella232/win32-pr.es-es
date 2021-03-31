---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Especifica los privilegios necesarios para la tarea.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Programador de tareas del elemento RequiredPrivileges
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151177"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="9d29a-104">Elemento RequiredPrivileges (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="9d29a-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="9d29a-105">Especifica los privilegios necesarios para la tarea.</span><span class="sxs-lookup"><span data-stu-id="9d29a-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="9d29a-106">El elemento **RequiredPrivileges** se define mediante el tipo complejo de [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9d29a-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9d29a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9d29a-107">Parent element</span></span>



| <span data-ttu-id="9d29a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9d29a-108">Element</span></span>                                                                                  | <span data-ttu-id="9d29a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9d29a-109">Derived from</span></span>                                                           | <span data-ttu-id="9d29a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d29a-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9d29a-111">**Entidad de seguridad (principalType)**</span><span class="sxs-lookup"><span data-stu-id="9d29a-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="9d29a-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="9d29a-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="9d29a-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d29a-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9d29a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d29a-114">Remarks</span></span>

<span data-ttu-id="9d29a-115">En el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="9d29a-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9d29a-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9d29a-116">Examples</span></span>

<span data-ttu-id="9d29a-117">El siguiente código XML define el uso de un identificador de grupo y los privilegios necesarios.</span><span class="sxs-lookup"><span data-stu-id="9d29a-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="9d29a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d29a-118">Requirements</span></span>



| <span data-ttu-id="9d29a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d29a-119">Requirement</span></span> | <span data-ttu-id="9d29a-120">Value</span><span class="sxs-lookup"><span data-stu-id="9d29a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9d29a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d29a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d29a-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d29a-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9d29a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d29a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d29a-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d29a-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d29a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d29a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d29a-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9d29a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





