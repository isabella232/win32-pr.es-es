---
title: Tipo complejo de namedValue
description: Define un nombre que está asociado a un valor en un par nombre-valor.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- tipo complejo de namedValue Programador de tareas
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996688"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="6b103-104">Tipo complejo de namedValue</span><span class="sxs-lookup"><span data-stu-id="6b103-104">namedValue Complex Type</span></span>

<span data-ttu-id="6b103-105">Define un nombre que está asociado a un valor en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="6b103-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="6b103-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b103-106">Attributes</span></span>



| <span data-ttu-id="6b103-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b103-107">Name</span></span> | <span data-ttu-id="6b103-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b103-108">Type</span></span>                                                                    | <span data-ttu-id="6b103-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b103-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6b103-110">name</span><span class="sxs-lookup"><span data-stu-id="6b103-110">name</span></span> | [<span data-ttu-id="6b103-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="6b103-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="6b103-112">Especifica el nombre que está asociado a un valor en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="6b103-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="6b103-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b103-113">Requirements</span></span>



| <span data-ttu-id="6b103-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b103-114">Requirement</span></span> | <span data-ttu-id="6b103-115">Value</span><span class="sxs-lookup"><span data-stu-id="6b103-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b103-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b103-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b103-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b103-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b103-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b103-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b103-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b103-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





