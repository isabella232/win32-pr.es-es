---
title: Tipo simple de CountType
description: Define un tipo de recuento que se utiliza para especificar el número de elementos de una matriz.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- CountType de tipo simple de registro
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804028"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="f5b62-104">Tipo simple de CountType</span><span class="sxs-lookup"><span data-stu-id="f5b62-104">CountType Simple Type</span></span>

<span data-ttu-id="f5b62-105">Define un tipo de recuento que se utiliza para especificar el número de elementos de una matriz.</span><span class="sxs-lookup"><span data-stu-id="f5b62-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="f5b62-106">El valor se puede especificar como un valor XS: unsignedShort o como una cadena que hace referencia al nombre del nodo elemento de datos que contiene el valor Short unsiged.</span><span class="sxs-lookup"><span data-stu-id="f5b62-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="f5b62-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b62-107">Requirements</span></span>



| <span data-ttu-id="f5b62-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b62-108">Requirement</span></span> | <span data-ttu-id="f5b62-109">Value</span><span class="sxs-lookup"><span data-stu-id="f5b62-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5b62-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b62-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b62-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b62-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5b62-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b62-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b62-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b62-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





