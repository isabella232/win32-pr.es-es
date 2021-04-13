---
title: Privilege (elemento requiredPrivilegesType)
description: Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Elemento Privilege Programador de tareas
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492280"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="4e0be-104">Privilege (elemento requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="4e0be-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="4e0be-105">Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e0be-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="4e0be-106">El elemento **Privilege** se define mediante el tipo complejo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4e0be-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4e0be-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4e0be-107">Parent element</span></span>



| <span data-ttu-id="4e0be-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4e0be-108">Element</span></span>                                                                                             | <span data-ttu-id="4e0be-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="4e0be-109">Derived from</span></span>                                                                             | <span data-ttu-id="4e0be-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e0be-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e0be-111">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="4e0be-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="4e0be-112">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="4e0be-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="4e0be-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="4e0be-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4e0be-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e0be-114">Remarks</span></span>

<span data-ttu-id="4e0be-115">En el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="4e0be-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="4e0be-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e0be-116">Examples</span></span>

<span data-ttu-id="4e0be-117">En el código XML siguiente se define un elemento de configuración que especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e0be-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="4e0be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e0be-118">Requirements</span></span>



| <span data-ttu-id="4e0be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e0be-119">Requirement</span></span> | <span data-ttu-id="4e0be-120">Value</span><span class="sxs-lookup"><span data-stu-id="4e0be-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4e0be-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e0be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0be-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e0be-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4e0be-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e0be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0be-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e0be-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e0be-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e0be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0be-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="4e0be-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





