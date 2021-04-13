---
title: Tipo simple de HexInt8Type
description: Define un tipo hexadecimal de 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- HexInt8Type de tipo simple de registro
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493096"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="5dae0-104">Tipo simple de HexInt8Type</span><span class="sxs-lookup"><span data-stu-id="5dae0-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="5dae0-105">Define un tipo hexadecimal de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="5dae0-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5dae0-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="5dae0-106">Patterns</span></span>

<span data-ttu-id="5dae0-107">El tipo simple **HexInt8Type** es una [cadena](/dotnet/api/system.string) restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="5dae0-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="5dae0-108">El valor puede contener de uno a dos caracteres hexadecimales (por ejemplo, 0xA o 0xac).</span><span class="sxs-lookup"><span data-stu-id="5dae0-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dae0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dae0-109">Requirements</span></span>



| <span data-ttu-id="5dae0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dae0-110">Requirement</span></span> | <span data-ttu-id="5dae0-111">Value</span><span class="sxs-lookup"><span data-stu-id="5dae0-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5dae0-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dae0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5dae0-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5dae0-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5dae0-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dae0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5dae0-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5dae0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

