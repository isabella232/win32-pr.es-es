---
description: Especifica el estándar de LAN inalámbrica 802,11 usado en una LAN inalámbrica.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686694"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="5a487-103">Elemento phyType (Connectivity)</span><span class="sxs-lookup"><span data-stu-id="5a487-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="5a487-104">El elemento phyType (conectividad) especifica el estándar de LAN inalámbrica 802,11 usado en una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="5a487-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="5a487-105">Puede especificar varios **phyType** s.</span><span class="sxs-lookup"><span data-stu-id="5a487-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="5a487-106">Si no se especifica **phyType** , el perfil se puede usar para conectarse a cualquier **phyType**.</span><span class="sxs-lookup"><span data-stu-id="5a487-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="5a487-107">El valor "n" solo se admite en Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a487-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="5a487-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="5a487-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5a487-109">El elemento se define mediante el elemento de [**Conectividad**](wlan-profileschema-connectivity-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5a487-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a487-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a487-110">Requirements</span></span>



| <span data-ttu-id="5a487-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a487-111">Requirement</span></span> | <span data-ttu-id="5a487-112">Value</span><span class="sxs-lookup"><span data-stu-id="5a487-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a487-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a487-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5a487-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a487-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a487-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a487-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5a487-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a487-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a487-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a487-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a487-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="5a487-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5a487-119">**Conectividad**</span><span class="sxs-lookup"><span data-stu-id="5a487-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="5a487-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a487-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5a487-121">**Conectividad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="5a487-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




