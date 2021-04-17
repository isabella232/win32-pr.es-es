---
description: Define la lista de redes permitidas y denegadas para las máquinas.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688328"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="b1c35-103">Elemento networkFilter (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="b1c35-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="b1c35-104">El elemento networkFilter (WLANPolicy) define la lista de redes permitidas y denegadas para las máquinas.</span><span class="sxs-lookup"><span data-stu-id="b1c35-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="b1c35-105">El elemento **networkFilter** se define mediante el elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c35-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b1c35-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1c35-106">Child elements</span></span>



| <span data-ttu-id="b1c35-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1c35-107">Element</span></span>                                                                    | <span data-ttu-id="b1c35-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1c35-108">Type</span></span>                                                                     | <span data-ttu-id="b1c35-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1c35-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1c35-110">**Permitidos**</span><span class="sxs-lookup"><span data-stu-id="b1c35-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="b1c35-111">La lista de redes LAN inalámbricas a las que se debe permitir que se conecte cualquier equipo.</span><span class="sxs-lookup"><span data-stu-id="b1c35-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="b1c35-112">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="b1c35-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="b1c35-113">La lista de redes LAN inalámbricas a las que una máquina no debe conectarse.</span><span class="sxs-lookup"><span data-stu-id="b1c35-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="b1c35-114">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="b1c35-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="b1c35-115">boolean</span><span class="sxs-lookup"><span data-stu-id="b1c35-115">boolean</span></span>                                                                  | <span data-ttu-id="b1c35-116">Especifica si el acceso a todas las redes de infraestructura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b1c35-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="b1c35-117">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="b1c35-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="b1c35-118">boolean</span><span class="sxs-lookup"><span data-stu-id="b1c35-118">boolean</span></span>                                                                  | <span data-ttu-id="b1c35-119">Especifica si el acceso a todas las redes ad hoc está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b1c35-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="b1c35-120">**Storage**</span><span class="sxs-lookup"><span data-stu-id="b1c35-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="b1c35-121">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="b1c35-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="b1c35-122">Una red permitida.</span><span class="sxs-lookup"><span data-stu-id="b1c35-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="b1c35-123">**Storage**</span><span class="sxs-lookup"><span data-stu-id="b1c35-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="b1c35-124">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="b1c35-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="b1c35-125">Una red bloqueada.</span><span class="sxs-lookup"><span data-stu-id="b1c35-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="b1c35-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1c35-126">Requirements</span></span>



| <span data-ttu-id="b1c35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c35-127">Requirement</span></span> | <span data-ttu-id="b1c35-128">Value</span><span class="sxs-lookup"><span data-stu-id="b1c35-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1c35-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1c35-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c35-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1c35-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1c35-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1c35-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c35-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1c35-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1c35-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1c35-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1c35-134">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="b1c35-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b1c35-135">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b1c35-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="b1c35-136">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="b1c35-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b1c35-137">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b1c35-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




