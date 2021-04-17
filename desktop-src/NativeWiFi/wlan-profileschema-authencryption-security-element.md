---
description: Especifica el par de autenticación y cifrado que se usará para este perfil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677537"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="801ac-103">Elemento authEncryption (Security)</span><span class="sxs-lookup"><span data-stu-id="801ac-103">authEncryption (security) Element</span></span>

<span data-ttu-id="801ac-104">El elemento authEncryption (Security) especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="801ac-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
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

<span data-ttu-id="801ac-105">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="801ac-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="801ac-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="801ac-106">Child elements</span></span>



| <span data-ttu-id="801ac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="801ac-107">Element</span></span>                                                                            | <span data-ttu-id="801ac-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="801ac-108">Type</span></span>                                                              | <span data-ttu-id="801ac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="801ac-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="801ac-110">**autenticación**</span><span class="sxs-lookup"><span data-stu-id="801ac-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="801ac-111">Especifica el método de autenticación que se debe usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="801ac-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="801ac-112">**cifra**</span><span class="sxs-lookup"><span data-stu-id="801ac-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="801ac-113">Establece el cifrado de datos que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="801ac-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="801ac-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="801ac-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="801ac-115">boolean</span><span class="sxs-lookup"><span data-stu-id="801ac-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="801ac-116">Indica si se usa 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="801ac-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="801ac-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="801ac-117">Remarks</span></span>

<span data-ttu-id="801ac-118">El elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del elemento **authEncryption** .</span><span class="sxs-lookup"><span data-stu-id="801ac-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="801ac-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="801ac-119">Examples</span></span>

<span data-ttu-id="801ac-120">Para ver los perfiles de ejemplo que usan el elemento **authEncryption** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="801ac-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="801ac-121">Para ver un perfil de ejemplo que usa el elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) , vea [ejemplo de Perfil de FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="801ac-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="801ac-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="801ac-122">Requirements</span></span>



| <span data-ttu-id="801ac-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="801ac-123">Requirement</span></span> | <span data-ttu-id="801ac-124">Value</span><span class="sxs-lookup"><span data-stu-id="801ac-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="801ac-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="801ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="801ac-126">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="801ac-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="801ac-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="801ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="801ac-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="801ac-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="801ac-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="801ac-129">Redistributable</span></span><br/>          | <span data-ttu-id="801ac-130">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="801ac-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="801ac-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="801ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801ac-132">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="801ac-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="801ac-133">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="801ac-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="801ac-134">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="801ac-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="801ac-135">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="801ac-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="801ac-136">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="801ac-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
