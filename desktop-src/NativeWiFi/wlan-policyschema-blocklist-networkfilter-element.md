---
description: Especifica la lista de redes LAN inalámbricas a las que un equipo no debe conectarse.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Elemento de listas de bloqueo (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000893"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="7abad-103">Elemento de listas de bloqueo (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="7abad-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="7abad-104">El elemento de lista de bloqueo (networkFilter) especifica la lista de redes LAN inalámbricas a las que un equipo no debe conectarse.</span><span class="sxs-lookup"><span data-stu-id="7abad-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
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

<span data-ttu-id="7abad-105">El elemento de listas de **bloqueo** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7abad-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7abad-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7abad-106">Child elements</span></span>



| <span data-ttu-id="7abad-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7abad-107">Element</span></span>                                                        | <span data-ttu-id="7abad-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7abad-108">Type</span></span>                                                                     | <span data-ttu-id="7abad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abad-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="7abad-110">**Storage**</span><span class="sxs-lookup"><span data-stu-id="7abad-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="7abad-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="7abad-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="7abad-112">La red bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7abad-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7abad-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abad-113">Requirements</span></span>



| <span data-ttu-id="7abad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abad-114">Requirement</span></span> | <span data-ttu-id="7abad-115">Value</span><span class="sxs-lookup"><span data-stu-id="7abad-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7abad-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7abad-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7abad-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7abad-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7abad-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7abad-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7abad-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7abad-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="7abad-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="7abad-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7abad-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="7abad-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="7abad-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="7abad-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7abad-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="7abad-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




