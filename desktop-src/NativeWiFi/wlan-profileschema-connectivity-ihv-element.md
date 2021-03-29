---
description: Contiene la configuración de conectividad relacionada con IHV. No está implementado actualmente.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: Elemento Connectivity (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811462"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="b4666-104">Elemento Connectivity (IHV)</span><span class="sxs-lookup"><span data-stu-id="b4666-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="b4666-105">El elemento de conectividad (IHV) contiene la configuración de conectividad relacionada con IHV.</span><span class="sxs-lookup"><span data-stu-id="b4666-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="b4666-106">No está implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b4666-106">It is not currently implemented.</span></span>

<span data-ttu-id="b4666-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="b4666-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b4666-108">El elemento está definido por el elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b4666-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4666-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4666-109">Requirements</span></span>



| <span data-ttu-id="b4666-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4666-110">Requirement</span></span> | <span data-ttu-id="b4666-111">Value</span><span class="sxs-lookup"><span data-stu-id="b4666-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4666-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4666-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b4666-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4666-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4666-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4666-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b4666-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4666-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4666-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4666-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4666-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="b4666-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b4666-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="b4666-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="b4666-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="b4666-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b4666-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="b4666-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




