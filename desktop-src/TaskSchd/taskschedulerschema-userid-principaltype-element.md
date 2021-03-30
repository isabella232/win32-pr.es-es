---
title: UserId (principalType), elemento
description: Especifica el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- UserId, elemento Programador de tareas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422621"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="804b3-104">UserId (principalType), elemento</span><span class="sxs-lookup"><span data-stu-id="804b3-104">UserId (principalType) Element</span></span>

<span data-ttu-id="804b3-105">Especifica el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="804b3-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="804b3-106">El elemento **userid** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="804b3-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="804b3-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="804b3-107">Parent element</span></span>



| <span data-ttu-id="804b3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="804b3-108">Element</span></span>                                                                  | <span data-ttu-id="804b3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="804b3-109">Derived from</span></span>                                                           | <span data-ttu-id="804b3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="804b3-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="804b3-111">**Principal**</span><span class="sxs-lookup"><span data-stu-id="804b3-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="804b3-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="804b3-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="804b3-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="804b3-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="804b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="804b3-114">Remarks</span></span>

<span data-ttu-id="804b3-115">El elemento **userid** y el elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="804b3-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="804b3-116">No se puede especificar un identificador de usuario y un identificador de grupo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="804b3-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="804b3-117">Especifique el **userid** o el elemento [**GROUPID**](taskschedulerschema-groupid-principaltype-element.md) , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="804b3-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="804b3-118">Para el desarrollo de scripts, el identificador de usuario se especifica mediante la propiedad [**principal. userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="804b3-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="804b3-119">En el desarrollo de C++, el identificador de usuario se especifica mediante la propiedad [**IPrincipal:: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="804b3-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="804b3-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="804b3-120">Examples</span></span>

<span data-ttu-id="804b3-121">En el código XML siguiente se define un principio mediante un identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="804b3-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="804b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804b3-122">Requirements</span></span>



| <span data-ttu-id="804b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="804b3-123">Requirement</span></span> | <span data-ttu-id="804b3-124">Value</span><span class="sxs-lookup"><span data-stu-id="804b3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="804b3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="804b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="804b3-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="804b3-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="804b3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="804b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="804b3-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="804b3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="804b3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="804b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804b3-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="804b3-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





