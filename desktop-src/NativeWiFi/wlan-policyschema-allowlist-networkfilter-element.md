---
description: Especifica la lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Elemento permitidos (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686492"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="bc31e-103">Elemento permitidos (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="bc31e-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="bc31e-104">El elemento permitidos (networkFilter) especifica la lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.</span><span class="sxs-lookup"><span data-stu-id="bc31e-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
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

<span data-ttu-id="bc31e-105">El elemento **permitidos** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bc31e-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bc31e-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bc31e-106">Child elements</span></span>



| <span data-ttu-id="bc31e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc31e-107">Element</span></span>                                                        | <span data-ttu-id="bc31e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc31e-108">Type</span></span>                                                                     | <span data-ttu-id="bc31e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc31e-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="bc31e-110">**Storage**</span><span class="sxs-lookup"><span data-stu-id="bc31e-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="bc31e-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="bc31e-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="bc31e-112">La red a la que se puede conectar la máquina.</span><span class="sxs-lookup"><span data-stu-id="bc31e-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bc31e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc31e-113">Requirements</span></span>



| <span data-ttu-id="bc31e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc31e-114">Requirement</span></span> | <span data-ttu-id="bc31e-115">Value</span><span class="sxs-lookup"><span data-stu-id="bc31e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc31e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc31e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc31e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc31e-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc31e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc31e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc31e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc31e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc31e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc31e-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc31e-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="bc31e-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bc31e-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="bc31e-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="bc31e-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="bc31e-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bc31e-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="bc31e-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




