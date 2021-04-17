---
title: DisplayName (principalType), elemento
description: Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Programador de tareas
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535500"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="ce2d1-104">DisplayName (principalType), elemento</span><span class="sxs-lookup"><span data-stu-id="ce2d1-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="ce2d1-105">Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="ce2d1-106">El elemento **displayName** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2d1-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce2d1-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ce2d1-107">Parent element</span></span>



| <span data-ttu-id="ce2d1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce2d1-108">Element</span></span>                                                                  | <span data-ttu-id="ce2d1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ce2d1-109">Derived from</span></span>                                                           | <span data-ttu-id="ce2d1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce2d1-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ce2d1-111">**Principal**</span><span class="sxs-lookup"><span data-stu-id="ce2d1-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ce2d1-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ce2d1-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ce2d1-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce2d1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce2d1-114">Remarks</span></span>

<span data-ttu-id="ce2d1-115">Para el desarrollo de scripting, el nombre para mostrar de la entidad de seguridad se especifica mediante la propiedad [**principal. DisplayName**](principal-displayname.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2d1-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="ce2d1-116">En el desarrollo de C++, el nombre para mostrar de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .</span><span class="sxs-lookup"><span data-stu-id="ce2d1-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ce2d1-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ce2d1-117">Examples</span></span>

<span data-ttu-id="ce2d1-118">En el código XML siguiente se define un con un identificador de grupo y un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="ce2d1-119">En el código XML siguiente se define una entidad de seguridad mediante un identificador de usuario y un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="ce2d1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce2d1-120">Requirements</span></span>



| <span data-ttu-id="ce2d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2d1-121">Requirement</span></span> | <span data-ttu-id="ce2d1-122">Value</span><span class="sxs-lookup"><span data-stu-id="ce2d1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce2d1-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2d1-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce2d1-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce2d1-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2d1-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce2d1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce2d1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce2d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2d1-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ce2d1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





