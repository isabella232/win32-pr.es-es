---
title: HexInt64Type (tipo simple) (esquema de eventos)
description: Define un tipo hexadecimal de 8 bytes. | HexInt64Type (tipo simple) (esquema de eventos)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
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
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698138"
---
# <a name="hexint64type-simple-type-event-schema"></a><span data-ttu-id="4d398-105">HexInt64Type (tipo simple) (esquema de eventos)</span><span class="sxs-lookup"><span data-stu-id="4d398-105">HexInt64Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="4d398-106">Define un tipo hexadecimal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="4d398-106">Defines an 8-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="4d398-107">Patrones</span><span class="sxs-lookup"><span data-stu-id="4d398-107">Patterns</span></span>

<span data-ttu-id="4d398-108">El tipo simple **HexInt64Type** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="4d398-108">The **HexInt64Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="4d398-109">El valor puede contener de 1 a dieciséis caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361004fe190).</span><span class="sxs-lookup"><span data-stu-id="4d398-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d398-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d398-110">Requirements</span></span>



| <span data-ttu-id="4d398-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d398-111">Requirement</span></span> | <span data-ttu-id="4d398-112">Value</span><span class="sxs-lookup"><span data-stu-id="4d398-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d398-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d398-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4d398-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4d398-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4d398-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d398-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4d398-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d398-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





