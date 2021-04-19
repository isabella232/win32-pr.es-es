---
description: Contiene información de claves compartidas.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677991"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="40b69-103">Elemento sharedKey (Security)</span><span class="sxs-lookup"><span data-stu-id="40b69-103">sharedKey (security) Element</span></span>

<span data-ttu-id="40b69-104">El elemento sharedKey (Security) contiene información de claves compartidas.</span><span class="sxs-lookup"><span data-stu-id="40b69-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="40b69-105">Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.</span><span class="sxs-lookup"><span data-stu-id="40b69-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="keyType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="networkKey"
                         />
                        <xs:enumeration
                            value="passPhrase"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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

<span data-ttu-id="40b69-106">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="40b69-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="40b69-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40b69-107">Child elements</span></span>



| <span data-ttu-id="40b69-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="40b69-108">Element</span></span>                                                                 | <span data-ttu-id="40b69-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="40b69-109">Type</span></span>                                                              | <span data-ttu-id="40b69-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40b69-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40b69-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="40b69-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="40b69-112">string</span><span class="sxs-lookup"><span data-stu-id="40b69-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="40b69-113">Contiene la clave o frase de contraseña de la red.</span><span class="sxs-lookup"><span data-stu-id="40b69-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="40b69-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="40b69-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="40b69-115">Tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="40b69-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="40b69-116">**protected**</span><span class="sxs-lookup"><span data-stu-id="40b69-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="40b69-117">boolean</span><span class="sxs-lookup"><span data-stu-id="40b69-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="40b69-118">Indica si la clave está cifrada.</span><span class="sxs-lookup"><span data-stu-id="40b69-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="40b69-119">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="40b69-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="40b69-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40b69-120">Remarks</span></span>

<span data-ttu-id="40b69-121">En Windows Vista y Windows Server 2008, los datos asociados con el elemento **sharedKey** se cifran antes de guardarse en el almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="40b69-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="40b69-122">En el caso de Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2, los datos no se cifran.</span><span class="sxs-lookup"><span data-stu-id="40b69-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="40b69-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="40b69-123">Examples</span></span>

<span data-ttu-id="40b69-124">Para ver los perfiles de ejemplo que usan el elemento **sharedKey** , vea ejemplo [de perfil sin difusión](non-broadcast-profile-sample.md), ejemplo de perfil [de WPA-Personal](wpa-personal-profile-sample.md)y [ejemplo de perfil WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="40b69-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40b69-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40b69-125">Requirements</span></span>



| <span data-ttu-id="40b69-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="40b69-126">Requirement</span></span> | <span data-ttu-id="40b69-127">Value</span><span class="sxs-lookup"><span data-stu-id="40b69-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="40b69-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40b69-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40b69-129">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="40b69-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="40b69-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40b69-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40b69-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="40b69-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="40b69-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="40b69-132">Redistributable</span></span><br/>          | <span data-ttu-id="40b69-133">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="40b69-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="40b69-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="40b69-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="40b69-135">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="40b69-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="40b69-136">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="40b69-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="40b69-137">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="40b69-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="40b69-138">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="40b69-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
