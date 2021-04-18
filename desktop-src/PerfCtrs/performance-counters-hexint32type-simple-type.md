---
description: Define un tipo hexadecimal de 4 bytes.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo simple de HexInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667282"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="38ced-103">Tipo simple de HexInt32Type (contadores de rendimiento)</span><span class="sxs-lookup"><span data-stu-id="38ced-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="38ced-104">Define un tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="38ced-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="38ced-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="38ced-105">Patterns</span></span>

<span data-ttu-id="38ced-106">El tipo simple **HexInt32Type** es **xs: String** , que está restringido por el patrón siguiente:</span><span class="sxs-lookup"><span data-stu-id="38ced-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="38ced-107">El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="38ced-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="38ced-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ced-108">Requirements</span></span>



| <span data-ttu-id="38ced-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ced-109">Requirement</span></span> | <span data-ttu-id="38ced-110">Value</span><span class="sxs-lookup"><span data-stu-id="38ced-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38ced-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38ced-111">Minimum supported client</span></span><br/> | <span data-ttu-id="38ced-112">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="38ced-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38ced-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38ced-113">Minimum supported server</span></span><br/> | <span data-ttu-id="38ced-114">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="38ced-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




