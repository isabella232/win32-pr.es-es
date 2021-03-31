---
title: Elemento GroupId (principalType)
description: Especifica el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Elemento GroupId Programador de tareas
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079635"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="6064c-104">Elemento GroupId (principalType)</span><span class="sxs-lookup"><span data-stu-id="6064c-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="6064c-105">Especifica el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6064c-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="6064c-106">El elemento **GROUPID** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6064c-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6064c-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6064c-107">Parent element</span></span>



| <span data-ttu-id="6064c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6064c-108">Element</span></span>                                                                  | <span data-ttu-id="6064c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6064c-109">Derived from</span></span>                                                           | <span data-ttu-id="6064c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6064c-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6064c-111">**Principal**</span><span class="sxs-lookup"><span data-stu-id="6064c-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="6064c-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="6064c-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="6064c-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6064c-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6064c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6064c-114">Remarks</span></span>

<span data-ttu-id="6064c-115">No se puede especificar un identificador de grupo y un identificador de usuario al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6064c-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="6064c-116">Especifique los elementos [**userid**](taskschedulerschema-userid-principaltype-element.md) o **GROUPID** , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="6064c-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="6064c-117">Para el desarrollo de scripts, el identificador de grupo de la entidad de seguridad se especifica mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="6064c-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="6064c-118">En el desarrollo de C++, el identificador de grupo de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal:: GROUPID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .</span><span class="sxs-lookup"><span data-stu-id="6064c-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="6064c-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6064c-119">Examples</span></span>

<span data-ttu-id="6064c-120">Para obtener un ejemplo completo del XML de una tarea que usa este elemento, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="6064c-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6064c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6064c-121">Requirements</span></span>



| <span data-ttu-id="6064c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6064c-122">Requirement</span></span> | <span data-ttu-id="6064c-123">Value</span><span class="sxs-lookup"><span data-stu-id="6064c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6064c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6064c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6064c-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6064c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6064c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6064c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6064c-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6064c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6064c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6064c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6064c-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6064c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





