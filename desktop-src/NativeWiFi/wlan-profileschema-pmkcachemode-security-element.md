---
description: Indica si se usará el almacenamiento en caché PMK.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154111"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="53c15-103">Elemento PMKCacheMode (Security)</span><span class="sxs-lookup"><span data-stu-id="53c15-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="53c15-104">El elemento PMKCacheMode (Security) indica si se usará el almacenamiento en caché PMK.</span><span class="sxs-lookup"><span data-stu-id="53c15-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="53c15-105">Este elemento solo es válido para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="53c15-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="53c15-106">El almacenamiento en caché PMK se describe en la especificación [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="53c15-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="53c15-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="53c15-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="53c15-108">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="53c15-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c15-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53c15-109">Requirements</span></span>



| <span data-ttu-id="53c15-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c15-110">Requirement</span></span> | <span data-ttu-id="53c15-111">Value</span><span class="sxs-lookup"><span data-stu-id="53c15-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53c15-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53c15-112">Minimum supported client</span></span><br/> | <span data-ttu-id="53c15-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53c15-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53c15-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53c15-114">Minimum supported server</span></span><br/> | <span data-ttu-id="53c15-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53c15-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53c15-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="53c15-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="53c15-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="53c15-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="53c15-118">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="53c15-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="53c15-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="53c15-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="53c15-120">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="53c15-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




