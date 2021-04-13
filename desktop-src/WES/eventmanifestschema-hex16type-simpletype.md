---
title: Tipo simple de HexInt16Type
description: Define un tipo hexadecimal de 2 bytes.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type de tipo simple de registro
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492556"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="cd54f-104">Tipo simple de HexInt16Type</span><span class="sxs-lookup"><span data-stu-id="cd54f-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="cd54f-105">Define un tipo hexadecimal de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="cd54f-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="cd54f-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="cd54f-106">Patterns</span></span>

<span data-ttu-id="cd54f-107">El tipo simple **HexInt16Type** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="cd54f-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="cd54f-108">El valor puede contener de uno a cuatro caracteres hexadecimales (por ejemplo, 0xA o 0xac7b).</span><span class="sxs-lookup"><span data-stu-id="cd54f-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd54f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd54f-109">Requirements</span></span>



| <span data-ttu-id="cd54f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd54f-110">Requirement</span></span> | <span data-ttu-id="cd54f-111">Value</span><span class="sxs-lookup"><span data-stu-id="cd54f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd54f-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd54f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cd54f-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cd54f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd54f-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd54f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cd54f-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd54f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





