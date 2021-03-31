---
description: Contiene el SSID de una LAN inalámbrica.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: nombre (SSID) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911897"
---
# <a name="name-ssid-element"></a><span data-ttu-id="243d8-103">nombre (SSID) (elemento)</span><span class="sxs-lookup"><span data-stu-id="243d8-103">name (SSID) Element</span></span>

<span data-ttu-id="243d8-104">El elemento Name (SSID) contiene el SSID de una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="243d8-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
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
```

<span data-ttu-id="243d8-105">El elemento se define mediante el elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="243d8-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="243d8-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="243d8-106">Remarks</span></span>

<span data-ttu-id="243d8-107">Los nombres distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="243d8-107">Names are case-sensitive.</span></span>

<span data-ttu-id="243d8-108">Aunque los elementos [**Hex**](wlan-profileschema-hex-ssid-element.md) y **Name** son opcionales, al menos un elemento **Hex** o **Name** debe aparecer como elemento secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="243d8-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="243d8-109">Cuando la información de perfil se convierte en un SSID, el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) se convierte en el SSID (si existe) y se omite el elemento de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="243d8-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="243d8-110">Si el elemento **Hex** no está presente, el elemento de **nombre** se convierte en un SSID mediante la conversión de Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="243d8-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="243d8-111">Cuando se almacena un SSID en un perfil, siempre se genera el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) .</span><span class="sxs-lookup"><span data-stu-id="243d8-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="243d8-112">El elemento **Name** solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas.</span><span class="sxs-lookup"><span data-stu-id="243d8-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="243d8-113">Es posible que se pierda parte de la información del SSID original cuando se convierte en un **nombre**.</span><span class="sxs-lookup"><span data-stu-id="243d8-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="243d8-114">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** No se muestran los caracteres de escape XML, como &.</span><span class="sxs-lookup"><span data-stu-id="243d8-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="243d8-115">Evite usar caracteres de escape XML en nombres SSID para perfiles implementados en Windows XP con SP3 y API LAN inalámbrica para Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="243d8-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="243d8-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="243d8-116">Examples</span></span>

<span data-ttu-id="243d8-117">Para ver los perfiles de ejemplo que usan el elemento **Name** , vea [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="243d8-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="243d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="243d8-118">Requirements</span></span>



| <span data-ttu-id="243d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="243d8-119">Requirement</span></span> | <span data-ttu-id="243d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="243d8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="243d8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="243d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="243d8-122">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="243d8-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="243d8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="243d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="243d8-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="243d8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="243d8-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="243d8-125">Redistributable</span></span><br/>          | <span data-ttu-id="243d8-126">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="243d8-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="243d8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="243d8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="243d8-128">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="243d8-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="243d8-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="243d8-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="243d8-130">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="243d8-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="243d8-131">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="243d8-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




