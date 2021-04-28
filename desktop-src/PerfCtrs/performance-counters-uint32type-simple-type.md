---
description: 'Tipo simple UInt32Type (contadores de rendimiento): define un tipo entero sin signo.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simple UInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114583"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="9c4b1-103">Tipo simple UInt32Type (contadores de rendimiento)</span><span class="sxs-lookup"><span data-stu-id="9c4b1-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="9c4b1-104">Define un tipo entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="9c4b1-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c4b1-105">Remarks</span></span>

<span data-ttu-id="9c4b1-106">Puede especificar el valor como un entero de 4 bytes o un valor hexadecimal en el intervalo comprendido entre 0 y 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4b1-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c4b1-107">Requirements</span></span>



| <span data-ttu-id="9c4b1-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c4b1-108">Requirement</span></span> | <span data-ttu-id="9c4b1-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9c4b1-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c4b1-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c4b1-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4b1-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c4b1-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c4b1-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c4b1-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4b1-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c4b1-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




