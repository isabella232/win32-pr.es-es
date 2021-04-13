---
title: Tipo complejo de principalType
description: Define el atributo, los elementos secundarios y la información de secuenciación para el elemento principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- tipo complejo de principalType Programador de tareas
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492059"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="c99d4-104">Tipo complejo de principalType</span><span class="sxs-lookup"><span data-stu-id="c99d4-104">principalType Complex Type</span></span>

<span data-ttu-id="c99d4-105">Define el atributo, los elementos secundarios y la información de secuenciación para el elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c99d4-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c99d4-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c99d4-106">Child elements</span></span>



| <span data-ttu-id="c99d4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c99d4-107">Element</span></span>                                                                                             | <span data-ttu-id="c99d4-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c99d4-108">Type</span></span>                                                                                     | <span data-ttu-id="c99d4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c99d4-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c99d4-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c99d4-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="c99d4-111">string</span><span class="sxs-lookup"><span data-stu-id="c99d4-111">string</span></span>                                                                                   | <span data-ttu-id="c99d4-112">Especifica el nombre de la entidad de seguridad que se muestra en la Programador de tareas interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="c99d4-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="c99d4-113">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="c99d4-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="c99d4-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c99d4-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="c99d4-115">Especifica el identificador del grupo de usuarios necesario para ejecutar tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c99d4-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="c99d4-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="c99d4-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="c99d4-118">Especifica el método de inicio de sesión de seguridad necesario para ejecutar tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c99d4-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="c99d4-119">**ProcessTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="c99d4-120">**processTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="c99d4-121">Especifica los tipos de identificador de seguridad (SID) de proceso que pueden ser utilizados por las tareas.</span><span class="sxs-lookup"><span data-stu-id="c99d4-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="c99d4-122">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="c99d4-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="c99d4-123">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="c99d4-124">Especifica los privilegios necesarios para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="c99d4-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="c99d4-125">**Nivel**</span><span class="sxs-lookup"><span data-stu-id="c99d4-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="c99d4-126">**runLevelType**</span><span class="sxs-lookup"><span data-stu-id="c99d4-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="c99d4-127">Especifica el nivel de permiso en el que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="c99d4-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="c99d4-128">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="c99d4-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="c99d4-129">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c99d4-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="c99d4-130">Especifica el identificador de usuario necesario para ejecutar tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c99d4-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="c99d4-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="c99d4-131">Attributes</span></span>



| <span data-ttu-id="c99d4-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="c99d4-132">Name</span></span> | <span data-ttu-id="c99d4-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c99d4-133">Type</span></span> | <span data-ttu-id="c99d4-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c99d4-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="c99d4-135">id</span><span class="sxs-lookup"><span data-stu-id="c99d4-135">id</span></span>   | <span data-ttu-id="c99d4-136">id</span><span class="sxs-lookup"><span data-stu-id="c99d4-136">ID</span></span>   | <span data-ttu-id="c99d4-137">Especifica el identificador de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c99d4-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c99d4-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c99d4-138">Requirements</span></span>



| <span data-ttu-id="c99d4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99d4-139">Requirement</span></span> | <span data-ttu-id="c99d4-140">Value</span><span class="sxs-lookup"><span data-stu-id="c99d4-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c99d4-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c99d4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c99d4-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c99d4-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c99d4-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c99d4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c99d4-144">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c99d4-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c99d4-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c99d4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99d4-146">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c99d4-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c99d4-147">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c99d4-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





