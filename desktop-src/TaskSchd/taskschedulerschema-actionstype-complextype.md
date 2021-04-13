---
title: Tipo complejo de actionsType
description: Define los elementos secundarios y el atributo para el elemento actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- tipo complejo de actionsType Programador de tareas
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422486"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="f4052-104">Tipo complejo de actionsType</span><span class="sxs-lookup"><span data-stu-id="f4052-104">actionsType Complex Type</span></span>

<span data-ttu-id="f4052-105">Define los elementos secundarios y el atributo para el elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f4052-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="f4052-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4052-106">Attributes</span></span>



| <span data-ttu-id="f4052-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4052-107">Name</span></span>    | <span data-ttu-id="f4052-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4052-108">Type</span></span>  | <span data-ttu-id="f4052-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4052-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4052-110">Context</span><span class="sxs-lookup"><span data-stu-id="f4052-110">Context</span></span> | <span data-ttu-id="f4052-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="f4052-111">IDREF</span></span> | <span data-ttu-id="f4052-112">Identificador de la entidad de seguridad utilizada que es el contexto de seguridad para las acciones de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f4052-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f4052-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4052-113">Requirements</span></span>



| <span data-ttu-id="f4052-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4052-114">Requirement</span></span> | <span data-ttu-id="f4052-115">Value</span><span class="sxs-lookup"><span data-stu-id="f4052-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4052-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4052-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4052-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4052-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4052-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4052-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4052-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4052-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4052-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4052-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4052-121">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f4052-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f4052-122">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f4052-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





