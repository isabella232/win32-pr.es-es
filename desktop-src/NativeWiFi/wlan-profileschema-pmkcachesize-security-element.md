---
description: Especifica el número de entradas en la caché de PMK en el cliente.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Elemento PMKCacheSize (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677334"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="91400-103">Elemento PMKCacheSize (Security)</span><span class="sxs-lookup"><span data-stu-id="91400-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="91400-104">El elemento PMKCacheSize (Security) especifica el número de entradas en la caché de PMK en el cliente.</span><span class="sxs-lookup"><span data-stu-id="91400-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="91400-105">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="91400-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="91400-106">Si **PMKCacheMode** está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="91400-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="91400-107">El almacenamiento en caché PMK se describe en la especificación [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="91400-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="91400-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="91400-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="91400-109">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="91400-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="91400-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91400-110">Requirements</span></span>



| <span data-ttu-id="91400-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="91400-111">Requirement</span></span> | <span data-ttu-id="91400-112">Value</span><span class="sxs-lookup"><span data-stu-id="91400-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91400-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91400-113">Minimum supported client</span></span><br/> | <span data-ttu-id="91400-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91400-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91400-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91400-115">Minimum supported server</span></span><br/> | <span data-ttu-id="91400-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91400-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91400-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="91400-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="91400-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="91400-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="91400-119">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="91400-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="91400-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="91400-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="91400-121">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="91400-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




