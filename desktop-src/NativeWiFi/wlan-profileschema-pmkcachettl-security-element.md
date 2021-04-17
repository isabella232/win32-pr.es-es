---
description: Indica el período de tiempo, en minutos, que se conservará una caché PMK.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Elemento PMKCacheTTL (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677333"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="8ed74-103">Elemento PMKCacheTTL (Security)</span><span class="sxs-lookup"><span data-stu-id="8ed74-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="8ed74-104">El elemento PMKCacheTTL (Security) indica el período de tiempo, en minutos, que se conservará una caché PMK.</span><span class="sxs-lookup"><span data-stu-id="8ed74-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="8ed74-105">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8ed74-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="8ed74-106">El almacenamiento en caché PMK se describe en la especificación [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="8ed74-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="8ed74-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ed74-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8ed74-108">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ed74-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed74-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ed74-109">Requirements</span></span>



| <span data-ttu-id="8ed74-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed74-110">Requirement</span></span> | <span data-ttu-id="8ed74-111">Value</span><span class="sxs-lookup"><span data-stu-id="8ed74-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ed74-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed74-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed74-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed74-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ed74-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed74-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed74-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed74-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ed74-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed74-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ed74-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="8ed74-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8ed74-118">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="8ed74-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="8ed74-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ed74-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8ed74-120">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="8ed74-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




