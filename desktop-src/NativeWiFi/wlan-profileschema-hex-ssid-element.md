---
description: Contiene el SSID de una LAN inalámbrica en formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento Hex (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686917"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="ab4a9-103">Elemento Hex (SSID)</span><span class="sxs-lookup"><span data-stu-id="ab4a9-103">hex (SSID) Element</span></span>

<span data-ttu-id="ab4a9-104">El elemento Hex (SSID) contiene el SSID de una LAN inalámbrica en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ab4a9-105">El elemento se define mediante el elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ab4a9-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab4a9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab4a9-106">Remarks</span></span>

<span data-ttu-id="ab4a9-107">Aunque los elementos **Hex** y [**Name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ab4a9-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="ab4a9-108">Cuando la información de perfil se convierte en un SSID, el elemento **Hex** se convierte en el SSID (si existe) y se omite el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ab4a9-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="ab4a9-109">Si el elemento **Hex** no está presente, el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión de Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="ab4a9-110">Cuando se almacena un SSID en un perfil, siempre se genera el elemento **Hex** .</span><span class="sxs-lookup"><span data-stu-id="ab4a9-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="ab4a9-111">El elemento [**Name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="ab4a9-112">Es posible que se pierda parte de la información del SSID original cuando se convierte en un [**nombre**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="ab4a9-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ab4a9-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ab4a9-113">Examples</span></span>

<span data-ttu-id="ab4a9-114">Para ver un perfil de ejemplo que usa el elemento **Hex** , vea [ejemplo de Perfil de FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ab4a9-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab4a9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab4a9-115">Requirements</span></span>



| <span data-ttu-id="ab4a9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab4a9-116">Requirement</span></span> | <span data-ttu-id="ab4a9-117">Value</span><span class="sxs-lookup"><span data-stu-id="ab4a9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ab4a9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab4a9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab4a9-119">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ab4a9-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ab4a9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab4a9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab4a9-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab4a9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ab4a9-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ab4a9-122">Redistributable</span></span><br/>          | <span data-ttu-id="ab4a9-123">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ab4a9-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ab4a9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab4a9-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab4a9-125">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ab4a9-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ab4a9-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="ab4a9-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="ab4a9-127">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ab4a9-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ab4a9-128">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="ab4a9-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




