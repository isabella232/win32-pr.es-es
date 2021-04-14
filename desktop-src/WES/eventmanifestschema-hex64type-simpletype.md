---
title: Tipo simple de HexInt64Type
description: Define un tipo hexadecimal de 8 bytes. | Tipo simple de HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- HexInt64Type de tipo simple de registro
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424208"
---
# <a name="hexint64type-simple-type"></a><span data-ttu-id="7959b-105">Tipo simple de HexInt64Type</span><span class="sxs-lookup"><span data-stu-id="7959b-105">HexInt64Type Simple Type</span></span>

<span data-ttu-id="7959b-106">Define un tipo hexadecimal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="7959b-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7959b-107">Patrones</span><span class="sxs-lookup"><span data-stu-id="7959b-107">Patterns</span></span>

<span data-ttu-id="7959b-108">El tipo simple **HexInt64Type** es una [cadena](/dotnet/api/system.string) restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="7959b-108">The **HexInt64Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="7959b-109">El valor puede contener de 1 a dieciséis caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361004fe190).</span><span class="sxs-lookup"><span data-stu-id="7959b-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="7959b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7959b-110">Requirements</span></span>



| <span data-ttu-id="7959b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7959b-111">Requirement</span></span> | <span data-ttu-id="7959b-112">Value</span><span class="sxs-lookup"><span data-stu-id="7959b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7959b-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7959b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7959b-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7959b-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7959b-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7959b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7959b-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7959b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

