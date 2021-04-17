---
title: Tipo simple HexInt32Type (esquema EventManifest)
description: Define un tipo hexadecimal de 4 bytes. | Tipo simple HexInt32Type (esquema EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- HexInt32Type de tipo simple de registro
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698098"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="93025-105">Tipo simple HexInt32Type (esquema EventManifest)</span><span class="sxs-lookup"><span data-stu-id="93025-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="93025-106">Define un tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="93025-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="93025-107">Patrones</span><span class="sxs-lookup"><span data-stu-id="93025-107">Patterns</span></span>

<span data-ttu-id="93025-108">El tipo simple **HexInt32Type** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="93025-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="93025-109">El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="93025-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="93025-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93025-110">Requirements</span></span>



| <span data-ttu-id="93025-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="93025-111">Requirement</span></span> | <span data-ttu-id="93025-112">Value</span><span class="sxs-lookup"><span data-stu-id="93025-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93025-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93025-113">Minimum supported client</span></span><br/> | <span data-ttu-id="93025-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="93025-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93025-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93025-115">Minimum supported server</span></span><br/> | <span data-ttu-id="93025-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="93025-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





