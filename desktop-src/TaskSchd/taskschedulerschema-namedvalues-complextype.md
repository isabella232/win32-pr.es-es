---
title: Tipo complejo de namedValues
description: Define un par nombre-valor en el que el nombre está asociado con el valor.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- tipo complejo de namedValues Programador de tareas
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802773"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="ac573-104">Tipo complejo de namedValues</span><span class="sxs-lookup"><span data-stu-id="ac573-104">namedValues Complex Type</span></span>

<span data-ttu-id="ac573-105">Define un par nombre-valor en el que el nombre está asociado con el valor.</span><span class="sxs-lookup"><span data-stu-id="ac573-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ac573-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac573-106">Child elements</span></span>



| <span data-ttu-id="ac573-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ac573-107">Element</span></span>                                                        | <span data-ttu-id="ac573-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac573-108">Type</span></span>                                                | <span data-ttu-id="ac573-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac573-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac573-110">**Value**</span><span class="sxs-lookup"><span data-stu-id="ac573-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="ac573-111">**namedValue**</span><span class="sxs-lookup"><span data-stu-id="ac573-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="ac573-112">Especifica el valor que está asociado a un nombre en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="ac573-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ac573-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac573-113">Requirements</span></span>



| <span data-ttu-id="ac573-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac573-114">Requirement</span></span> | <span data-ttu-id="ac573-115">Value</span><span class="sxs-lookup"><span data-stu-id="ac573-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac573-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac573-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac573-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac573-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac573-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac573-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac573-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac573-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





