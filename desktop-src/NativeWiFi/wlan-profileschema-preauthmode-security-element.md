---
description: Indica si el cliente usará la autenticación previa.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Elemento preAuthMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677332"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="22738-103">Elemento preAuthMode (Security)</span><span class="sxs-lookup"><span data-stu-id="22738-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="22738-104">El elemento preAuthMode (Security) indica si el cliente usará la autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="22738-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="22738-105">La autenticación previa es necesaria para la itinerancia rápida segura de WPA2.</span><span class="sxs-lookup"><span data-stu-id="22738-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="22738-106">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="22738-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="22738-107">Si **PMKCacheMode** está habilitado y este elemento no está presente, el valor predeterminado es "Disabled".</span><span class="sxs-lookup"><span data-stu-id="22738-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="22738-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="22738-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="22738-109">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="22738-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="22738-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22738-110">Requirements</span></span>



| <span data-ttu-id="22738-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="22738-111">Requirement</span></span> | <span data-ttu-id="22738-112">Value</span><span class="sxs-lookup"><span data-stu-id="22738-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22738-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22738-113">Minimum supported client</span></span><br/> | <span data-ttu-id="22738-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22738-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22738-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22738-115">Minimum supported server</span></span><br/> | <span data-ttu-id="22738-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="22738-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22738-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="22738-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="22738-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="22738-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="22738-119">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="22738-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="22738-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="22738-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="22738-121">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="22738-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




