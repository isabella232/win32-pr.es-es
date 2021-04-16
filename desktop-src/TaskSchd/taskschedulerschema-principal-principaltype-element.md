---
title: Elemento principal (principalType)
description: Especifica las credenciales de seguridad para una entidad de seguridad.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Elemento principal Programador de tareas
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685882"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="9fda2-104">Elemento principal (principalType)</span><span class="sxs-lookup"><span data-stu-id="9fda2-104">Principal (principalType) Element</span></span>

<span data-ttu-id="9fda2-105">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9fda2-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="9fda2-106">Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="9fda2-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="9fda2-107">El elemento **principal** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9fda2-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9fda2-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9fda2-108">Parent element</span></span>



| <span data-ttu-id="9fda2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fda2-109">Element</span></span>                                                               | <span data-ttu-id="9fda2-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9fda2-110">Derived from</span></span>                                                             | <span data-ttu-id="9fda2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fda2-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="9fda2-112">**Entidades de seguridad**</span><span class="sxs-lookup"><span data-stu-id="9fda2-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="9fda2-113">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="9fda2-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="9fda2-114">Especifica las entidades de seguridad asociadas a la tarea.</span><span class="sxs-lookup"><span data-stu-id="9fda2-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="9fda2-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fda2-115">Child elements</span></span>



| <span data-ttu-id="9fda2-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fda2-116">Element</span></span>                                                                      | <span data-ttu-id="9fda2-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fda2-117">Type</span></span>                                                          | <span data-ttu-id="9fda2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fda2-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fda2-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="9fda2-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="9fda2-120">**string**</span><span class="sxs-lookup"><span data-stu-id="9fda2-120">**string**</span></span>                                                    | <span data-ttu-id="9fda2-121">Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9fda2-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="9fda2-122">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="9fda2-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="9fda2-123">**string**</span><span class="sxs-lookup"><span data-stu-id="9fda2-123">**string**</span></span>                                                    | <span data-ttu-id="9fda2-124">Especifica el identificador del grupo de usuarios necesario para ejecutar tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9fda2-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="9fda2-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="9fda2-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="9fda2-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="9fda2-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="9fda2-127">Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9fda2-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="9fda2-128">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="9fda2-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="9fda2-129">**string**</span><span class="sxs-lookup"><span data-stu-id="9fda2-129">**string**</span></span>                                                    | <span data-ttu-id="9fda2-130">Especifica el identificador de usuario necesario para ejecutar tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9fda2-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="9fda2-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fda2-131">Attributes</span></span>



| <span data-ttu-id="9fda2-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fda2-132">Name</span></span> | <span data-ttu-id="9fda2-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fda2-133">Type</span></span> | <span data-ttu-id="9fda2-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fda2-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="9fda2-135">Identificador</span><span class="sxs-lookup"><span data-stu-id="9fda2-135">Id</span></span>   | <span data-ttu-id="9fda2-136">id</span><span class="sxs-lookup"><span data-stu-id="9fda2-136">ID</span></span>   | <span data-ttu-id="9fda2-137">Identificador de la definición de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9fda2-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9fda2-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fda2-138">Remarks</span></span>

<span data-ttu-id="9fda2-139">Para el desarrollo de scripts, las credenciales de seguridad de una entidad de seguridad se especifican mediante el objeto [**principal**](principal.md) .</span><span class="sxs-lookup"><span data-stu-id="9fda2-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="9fda2-140">En el desarrollo de C++, las credenciales de seguridad de una entidad de seguridad se especifican mediante la interfaz [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .</span><span class="sxs-lookup"><span data-stu-id="9fda2-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="9fda2-141">Los elementos secundarios enumerados anteriormente se definen mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9fda2-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="9fda2-142">Para obtener información sobre la secuenciación de estos elementos secundarios, vea [**principalType**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="9fda2-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9fda2-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9fda2-143">Examples</span></span>

<span data-ttu-id="9fda2-144">En el código XML siguiente se define una entidad de seguridad con un identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="9fda2-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="9fda2-145">En el código XML siguiente se define una entidad de seguridad con un identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="9fda2-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="9fda2-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fda2-146">Requirements</span></span>



| <span data-ttu-id="9fda2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fda2-147">Requirement</span></span> | <span data-ttu-id="9fda2-148">Value</span><span class="sxs-lookup"><span data-stu-id="9fda2-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fda2-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fda2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9fda2-150">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fda2-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fda2-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fda2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9fda2-152">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fda2-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fda2-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fda2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fda2-154">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9fda2-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





