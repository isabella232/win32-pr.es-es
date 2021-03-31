---
title: Tipo simple UInt64Type (esquema EventManifest)
description: Define un tipo Long sin signo.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type de tipo simple de registro
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079326"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="02892-104">Tipo simple de UInt64Type</span><span class="sxs-lookup"><span data-stu-id="02892-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="02892-105">Define un tipo Long sin signo.</span><span class="sxs-lookup"><span data-stu-id="02892-105">Defines an unsigned long type.</span></span> <span data-ttu-id="02892-106">El valor se puede especificar como un entero de 8 bytes o como un valor hexadecimal en el intervalo comprendido entre 0 y 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="02892-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="02892-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02892-107">Requirements</span></span>



| <span data-ttu-id="02892-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="02892-108">Requirement</span></span> | <span data-ttu-id="02892-109">Value</span><span class="sxs-lookup"><span data-stu-id="02892-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02892-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02892-110">Minimum supported client</span></span><br/> | <span data-ttu-id="02892-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="02892-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02892-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02892-112">Minimum supported server</span></span><br/> | <span data-ttu-id="02892-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="02892-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





