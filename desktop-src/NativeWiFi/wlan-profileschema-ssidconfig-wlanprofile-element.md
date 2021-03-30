---
description: Contiene uno o más SSID para LAN inalámbricas.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910357"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="d7cbf-103">Elemento SSIDConfig (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="d7cbf-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="d7cbf-104">El elemento SSIDConfig (WLANProfile) contiene uno o más SSID para LAN inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="nonBroadcast"
                type="boolean"
                minOccurs="0"
             />
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

<span data-ttu-id="d7cbf-105">El elemento **SSIDConfig** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d7cbf-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d7cbf-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7cbf-106">Child elements</span></span>



| <span data-ttu-id="d7cbf-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7cbf-107">Element</span></span>                                                                    | <span data-ttu-id="d7cbf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7cbf-108">Type</span></span>                                                              | <span data-ttu-id="d7cbf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7cbf-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7cbf-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="d7cbf-111">Contiene el SSID de una LAN inalámbrica en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d7cbf-112">**name**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="d7cbf-113">Contiene el nombre (distingue mayúsculas de minúsculas) del SSID de una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="d7cbf-114">**Difusión**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="d7cbf-115">boolean</span><span class="sxs-lookup"><span data-stu-id="d7cbf-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="d7cbf-116">Indica si la red difunde su SSID.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="d7cbf-117">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="d7cbf-118">El valor predeterminado es **true** si este elemento no está presente.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="d7cbf-119">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en IBSS, este valor debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="d7cbf-120">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="d7cbf-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="d7cbf-122">Contiene un SSID para una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="d7cbf-123">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Como máximo, un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) puede aparecer en un perfil.</span><span class="sxs-lookup"><span data-stu-id="d7cbf-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="d7cbf-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7cbf-124">Examples</span></span>

<span data-ttu-id="d7cbf-125">Para ver los perfiles de ejemplo que usan el elemento **SSIDConfig** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d7cbf-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7cbf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7cbf-126">Requirements</span></span>



| <span data-ttu-id="d7cbf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7cbf-127">Requirement</span></span> | <span data-ttu-id="d7cbf-128">Value</span><span class="sxs-lookup"><span data-stu-id="d7cbf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d7cbf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7cbf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d7cbf-130">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d7cbf-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7cbf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7cbf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d7cbf-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7cbf-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d7cbf-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d7cbf-133">Redistributable</span></span><br/>          | <span data-ttu-id="d7cbf-134">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="d7cbf-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d7cbf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7cbf-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7cbf-136">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d7cbf-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d7cbf-138">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d7cbf-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d7cbf-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
