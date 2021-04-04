---
description: Contiene un SSID para una LAN inalámbrica.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (elemento SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910649"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="3fff7-103">SSID (elemento SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="3fff7-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="3fff7-104">El elemento SSID (SSIDConfig) contiene un SSID para una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="3fff7-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="3fff7-105">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Como máximo, un elemento **SSID** puede aparecer en un perfil.</span><span class="sxs-lookup"><span data-stu-id="3fff7-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="name"
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
                            value="32"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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

<span data-ttu-id="3fff7-106">El elemento **SSID** se define mediante el elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3fff7-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3fff7-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3fff7-107">Child elements</span></span>



| <span data-ttu-id="3fff7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fff7-108">Element</span></span>                                              | <span data-ttu-id="3fff7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fff7-109">Type</span></span> | <span data-ttu-id="3fff7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fff7-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="3fff7-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="3fff7-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="3fff7-112">Contiene el SSID de una LAN inalámbrica en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3fff7-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="3fff7-113">**name**</span><span class="sxs-lookup"><span data-stu-id="3fff7-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="3fff7-114">Contiene el SSID para una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="3fff7-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="3fff7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fff7-115">Remarks</span></span>

<span data-ttu-id="3fff7-116">Aunque los elementos [**Hex**](wlan-profileschema-hex-ssid-element.md) y [**Name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del elemento **SSID** .</span><span class="sxs-lookup"><span data-stu-id="3fff7-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="3fff7-117">Cuando la información de perfil se convierte en un SSID, el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) se convierte en el SSID (si existe) y se omite el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3fff7-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="3fff7-118">Si el elemento **Hex** no está presente, el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión de Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="3fff7-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="3fff7-119">Cuando se almacena un SSID en un perfil, siempre se genera el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3fff7-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="3fff7-120">El elemento [**Name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas.</span><span class="sxs-lookup"><span data-stu-id="3fff7-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="3fff7-121">Es posible que se pierda parte de la información del SSID original cuando se convierte en un [**nombre**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="3fff7-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3fff7-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3fff7-122">Examples</span></span>

<span data-ttu-id="3fff7-123">Para ver los perfiles de ejemplo que usan el elemento **SSID** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3fff7-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fff7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fff7-124">Requirements</span></span>



| <span data-ttu-id="3fff7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fff7-125">Requirement</span></span> | <span data-ttu-id="3fff7-126">Value</span><span class="sxs-lookup"><span data-stu-id="3fff7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3fff7-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fff7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3fff7-128">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3fff7-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3fff7-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fff7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3fff7-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fff7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="3fff7-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3fff7-131">Redistributable</span></span><br/>          | <span data-ttu-id="3fff7-132">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="3fff7-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3fff7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fff7-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fff7-134">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="3fff7-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3fff7-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="3fff7-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3fff7-136">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="3fff7-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3fff7-137">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="3fff7-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




