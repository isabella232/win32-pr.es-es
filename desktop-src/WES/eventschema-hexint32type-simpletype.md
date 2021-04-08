---
title: HexInt32Type (tipo simple) (esquema de eventos)
description: Define un tipo hexadecimal de 4 bytes. | HexInt32Type (tipo simple) (esquema de eventos)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
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
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003586"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="05d05-105">HexInt32Type (tipo simple) (esquema de eventos)</span><span class="sxs-lookup"><span data-stu-id="05d05-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="05d05-106">Define un tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="05d05-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="05d05-107">Patrones</span><span class="sxs-lookup"><span data-stu-id="05d05-107">Patterns</span></span>

<span data-ttu-id="05d05-108">El tipo simple **HexInt32Type** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="05d05-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="05d05-109">El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="05d05-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="05d05-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05d05-110">Requirements</span></span>



| <span data-ttu-id="05d05-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d05-111">Requirement</span></span> | <span data-ttu-id="05d05-112">Value</span><span class="sxs-lookup"><span data-stu-id="05d05-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05d05-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05d05-113">Minimum supported client</span></span><br/> | <span data-ttu-id="05d05-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="05d05-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05d05-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05d05-115">Minimum supported server</span></span><br/> | <span data-ttu-id="05d05-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="05d05-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





