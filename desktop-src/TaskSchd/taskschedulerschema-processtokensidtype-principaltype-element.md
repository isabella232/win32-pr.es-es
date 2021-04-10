---
title: Elemento ProcessTokenSidType (principalType)
description: Especifica el tipo de identificación de seguridad (SID) del proceso de la tarea.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Programador de tareas del elemento ProcessTokenSidType
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150603"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="496f3-104">Elemento ProcessTokenSidType (principalType)</span><span class="sxs-lookup"><span data-stu-id="496f3-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="496f3-105">Especifica el tipo de identificación de seguridad (SID) del proceso de la tarea.</span><span class="sxs-lookup"><span data-stu-id="496f3-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="496f3-106">El elemento **ProcessTokenSidType** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="496f3-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="496f3-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="496f3-107">Parent element</span></span>



| <span data-ttu-id="496f3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="496f3-108">Element</span></span>                                                                  | <span data-ttu-id="496f3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="496f3-109">Derived from</span></span>                                                           | <span data-ttu-id="496f3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="496f3-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="496f3-111">**Principal**</span><span class="sxs-lookup"><span data-stu-id="496f3-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="496f3-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="496f3-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="496f3-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="496f3-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="496f3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="496f3-114">Remarks</span></span>

<span data-ttu-id="496f3-115">En el desarrollo de C++, el tipo de SID de proceso se especifica mediante la propiedad [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .</span><span class="sxs-lookup"><span data-stu-id="496f3-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="496f3-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="496f3-116">Examples</span></span>

<span data-ttu-id="496f3-117">El siguiente código XML define el tipo de SID del proceso de la tarea.</span><span class="sxs-lookup"><span data-stu-id="496f3-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="496f3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="496f3-118">Requirements</span></span>



| <span data-ttu-id="496f3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="496f3-119">Requirement</span></span> | <span data-ttu-id="496f3-120">Value</span><span class="sxs-lookup"><span data-stu-id="496f3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="496f3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="496f3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="496f3-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="496f3-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="496f3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="496f3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="496f3-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="496f3-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="496f3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="496f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496f3-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="496f3-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





