---
title: Tipo simple de UInt8Type
description: Define un tipo de byte sin signo.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- UInt8Type de tipo simple de registro
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695921"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="6b721-104">Tipo simple de UInt8Type</span><span class="sxs-lookup"><span data-stu-id="6b721-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="6b721-105">Define un tipo de byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="6b721-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="6b721-106">El valor se puede especificar como un entero de 1 byte o un valor hexadecimal en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="6b721-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="6b721-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b721-107">Requirements</span></span>



| <span data-ttu-id="6b721-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b721-108">Requirement</span></span> | <span data-ttu-id="6b721-109">Value</span><span class="sxs-lookup"><span data-stu-id="6b721-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b721-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b721-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6b721-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b721-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b721-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b721-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6b721-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b721-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





