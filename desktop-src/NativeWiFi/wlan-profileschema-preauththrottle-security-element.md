---
description: Especifica el número de intentos de autenticación previa para intentar en los AP vecinos.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541030"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="076f5-103">Elemento preAuthThrottle (Security)</span><span class="sxs-lookup"><span data-stu-id="076f5-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="076f5-104">El elemento preAuthThrottle (Security) especifica el número de intentos de autenticación previa para probar en APs vecinos.</span><span class="sxs-lookup"><span data-stu-id="076f5-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="076f5-105">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="076f5-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="076f5-106">Si **PMKCacheMode** está habilitado y este elemento no está presente, el número de intentos predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="076f5-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="076f5-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="076f5-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="076f5-108">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="076f5-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="076f5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076f5-109">Requirements</span></span>



| <span data-ttu-id="076f5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="076f5-110">Requirement</span></span> | <span data-ttu-id="076f5-111">Value</span><span class="sxs-lookup"><span data-stu-id="076f5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="076f5-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="076f5-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="076f5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="076f5-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="076f5-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="076f5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="076f5-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="076f5-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="076f5-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="076f5-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="076f5-118">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="076f5-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="076f5-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="076f5-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="076f5-120">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="076f5-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




