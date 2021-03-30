---
description: Contiene un hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Elemento Type (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910646"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="6c8cc-103">Elemento Type (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="6c8cc-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="6c8cc-104">El elemento Type (OUIHeader) contiene un hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.</span><span class="sxs-lookup"><span data-stu-id="6c8cc-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="6c8cc-105">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="6c8cc-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6c8cc-106">El elemento se define mediante el elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6c8cc-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8cc-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c8cc-107">Requirements</span></span>



| <span data-ttu-id="6c8cc-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8cc-108">Requirement</span></span> | <span data-ttu-id="6c8cc-109">Value</span><span class="sxs-lookup"><span data-stu-id="6c8cc-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c8cc-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c8cc-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8cc-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6c8cc-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c8cc-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c8cc-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8cc-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c8cc-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c8cc-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c8cc-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c8cc-115">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="6c8cc-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6c8cc-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="6c8cc-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="6c8cc-117">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="6c8cc-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6c8cc-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="6c8cc-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




