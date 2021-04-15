---
description: El nombre de dominio del proveedor de red doméstica del dispositivo, que identifica al operador de la red.
ms.assetid: 7676e1d8-a414-401f-989c-9f60068b92d8
title: Elemento DomainName (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DomainName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 670fc91771ee0a47cd7f16f617d052df2e567b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677426"
---
# <a name="domainname-hotspot2-element"></a><span data-ttu-id="7f056-103">Elemento DomainName (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="7f056-103">DomainName (Hotspot2) Element</span></span>

<span data-ttu-id="7f056-104">El nombre de dominio del proveedor de red doméstica del dispositivo, que identifica al operador de la red.</span><span class="sxs-lookup"><span data-stu-id="7f056-104">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span>

``` syntax
<xs:element name="DomainName"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="7f056-105">El elemento se define mediante el elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7f056-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

 

 



