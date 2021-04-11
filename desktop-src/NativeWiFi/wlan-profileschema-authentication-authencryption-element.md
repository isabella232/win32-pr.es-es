---
description: Especifica el método de autenticación que se va a usar para conectarse a la LAN inalámbrica.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Elemento Authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275801"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="262e5-103">Elemento Authentication (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="262e5-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="262e5-104">El elemento Authentication (authEncryption) especifica el método de autenticación que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="262e5-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="262e5-105">El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="262e5-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="262e5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="262e5-106">Remarks</span></span>

<span data-ttu-id="262e5-107">En la tabla siguiente se describen los valores de enumeración.</span><span class="sxs-lookup"><span data-stu-id="262e5-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="262e5-108">Value</span><span class="sxs-lookup"><span data-stu-id="262e5-108">Value</span></span>   | <span data-ttu-id="262e5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="262e5-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="262e5-110">abrir</span><span class="sxs-lookup"><span data-stu-id="262e5-110">open</span></span>    | <span data-ttu-id="262e5-111">Abra la autenticación 802,11.</span><span class="sxs-lookup"><span data-stu-id="262e5-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="262e5-112">shared</span><span class="sxs-lookup"><span data-stu-id="262e5-112">shared</span></span>  | <span data-ttu-id="262e5-113">Autenticación 802,11 compartida.</span><span class="sxs-lookup"><span data-stu-id="262e5-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="262e5-114">WPA</span><span class="sxs-lookup"><span data-stu-id="262e5-114">WPA</span></span>     | <span data-ttu-id="262e5-115">Autenticación WPA-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="262e5-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="262e5-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="262e5-116">WPAPSK</span></span>  | <span data-ttu-id="262e5-117">Autenticación WPA-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="262e5-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="262e5-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="262e5-118">WPA2</span></span>    | <span data-ttu-id="262e5-119">Autenticación WPA2-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="262e5-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="262e5-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="262e5-120">WPA2PSK</span></span> | <span data-ttu-id="262e5-121">Autenticación WPA2-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="262e5-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="262e5-122">Para obtener más información acerca de los métodos de autenticación de 802,11, consulte las especificaciones de [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)y [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="262e5-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="262e5-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="262e5-123">Examples</span></span>

<span data-ttu-id="262e5-124">Para ver los perfiles de ejemplo que usan el elemento de **autenticación** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="262e5-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="262e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="262e5-125">Requirements</span></span>



| <span data-ttu-id="262e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="262e5-126">Requirement</span></span> | <span data-ttu-id="262e5-127">Value</span><span class="sxs-lookup"><span data-stu-id="262e5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="262e5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="262e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="262e5-129">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="262e5-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="262e5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="262e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="262e5-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="262e5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="262e5-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="262e5-132">Redistributable</span></span><br/>          | <span data-ttu-id="262e5-133">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="262e5-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="262e5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="262e5-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="262e5-135">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="262e5-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="262e5-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="262e5-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="262e5-137">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="262e5-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="262e5-138">**authEncryption (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="262e5-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




