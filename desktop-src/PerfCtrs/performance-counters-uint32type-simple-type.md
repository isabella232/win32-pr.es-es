---
description: Define un tipo entero sin signo.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simple de UInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667267"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="a129b-103">Tipo simple de UInt32Type (contadores de rendimiento)</span><span class="sxs-lookup"><span data-stu-id="a129b-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="a129b-104">Define un tipo entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="a129b-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="a129b-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a129b-105">Remarks</span></span>

<span data-ttu-id="a129b-106">Puede especificar el valor como un entero de 4 bytes o un valor hexadecimal en el intervalo comprendido entre 0 y 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="a129b-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="a129b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a129b-107">Requirements</span></span>



| <span data-ttu-id="a129b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a129b-108">Requirement</span></span> | <span data-ttu-id="a129b-109">Value</span><span class="sxs-lookup"><span data-stu-id="a129b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a129b-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a129b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a129b-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a129b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a129b-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a129b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a129b-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a129b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




