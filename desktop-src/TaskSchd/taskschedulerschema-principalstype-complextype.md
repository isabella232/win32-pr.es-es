---
title: Tipo complejo de principalsType
description: Define el elemento secundario del elemento de entidades de seguridad.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- tipo complejo de principalsType Programador de tareas
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996029"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="f6969-104">Tipo complejo de principalsType</span><span class="sxs-lookup"><span data-stu-id="f6969-104">principalsType Complex Type</span></span>

<span data-ttu-id="f6969-105">Define el elemento secundario del elemento de [**entidades**](taskschedulerschema-principals-tasktype-element.md) de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f6969-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f6969-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6969-106">Child elements</span></span>



| <span data-ttu-id="f6969-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6969-107">Element</span></span>                                                                  | <span data-ttu-id="f6969-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6969-108">Type</span></span>                                                                   | <span data-ttu-id="f6969-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6969-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f6969-110">**Principal**</span><span class="sxs-lookup"><span data-stu-id="f6969-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="f6969-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="f6969-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="f6969-112">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f6969-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f6969-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6969-113">Requirements</span></span>



| <span data-ttu-id="f6969-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6969-114">Requirement</span></span> | <span data-ttu-id="f6969-115">Value</span><span class="sxs-lookup"><span data-stu-id="f6969-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6969-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6969-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6969-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6969-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6969-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6969-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6969-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6969-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





