---
description: Identifica el IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Elemento OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677336"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="32412-103">Elemento OUIHeader (IHV)</span><span class="sxs-lookup"><span data-stu-id="32412-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="32412-104">El elemento OUIHeader (IHV) identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="32412-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="32412-105">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="32412-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="32412-106">El elemento está definido por el elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="32412-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="32412-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="32412-107">Child elements</span></span>



| <span data-ttu-id="32412-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="32412-108">Element</span></span>                                                   | <span data-ttu-id="32412-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="32412-109">Type</span></span> | <span data-ttu-id="32412-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="32412-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32412-111">**OUI**</span><span class="sxs-lookup"><span data-stu-id="32412-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="32412-112">Contiene un hexBinary de 3 bytes que identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="32412-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="32412-113">**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="32412-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="32412-114">Contiene un hexBinary de 1 byte que se usa para diferenciar las NIC del mismo IHV.</span><span class="sxs-lookup"><span data-stu-id="32412-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="32412-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32412-115">Requirements</span></span>



| <span data-ttu-id="32412-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="32412-116">Requirement</span></span> | <span data-ttu-id="32412-117">Value</span><span class="sxs-lookup"><span data-stu-id="32412-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32412-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32412-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32412-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="32412-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32412-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32412-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32412-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="32412-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32412-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="32412-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="32412-123">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="32412-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="32412-124">**IHV**</span><span class="sxs-lookup"><span data-stu-id="32412-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="32412-125">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="32412-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="32412-126">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="32412-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




