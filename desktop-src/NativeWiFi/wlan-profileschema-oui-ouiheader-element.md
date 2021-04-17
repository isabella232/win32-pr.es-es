---
description: Contiene un hexBinary de 3 bytes que identifica el IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Elemento OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686695"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="abe61-103">Elemento OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="abe61-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="abe61-104">El elemento OUI (OUIHeader) contiene un hexBinary de 3 bytes que identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="abe61-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="abe61-105">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="abe61-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="abe61-106">El elemento se define mediante el elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="abe61-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe61-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abe61-107">Requirements</span></span>



| <span data-ttu-id="abe61-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe61-108">Requirement</span></span> | <span data-ttu-id="abe61-109">Value</span><span class="sxs-lookup"><span data-stu-id="abe61-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="abe61-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abe61-110">Minimum supported client</span></span><br/> | <span data-ttu-id="abe61-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="abe61-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="abe61-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abe61-112">Minimum supported server</span></span><br/> | <span data-ttu-id="abe61-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="abe61-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abe61-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="abe61-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="abe61-115">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="abe61-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="abe61-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="abe61-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="abe61-117">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="abe61-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="abe61-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="abe61-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




