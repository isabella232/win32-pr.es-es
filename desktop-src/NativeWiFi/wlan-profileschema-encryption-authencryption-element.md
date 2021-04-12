---
description: Especifica el tipo de cifrado de datos que se va a usar para conectarse a una LAN inalámbrica.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Elemento Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154576"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="0dfc9-103">Elemento Encryption (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="0dfc9-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="0dfc9-104">El elemento Encryption (authEncryption) especifica el tipo de cifrado de datos que se va a usar para conectarse a una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="0dfc9-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
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
```

<span data-ttu-id="0dfc9-105">El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0dfc9-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfc9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dfc9-106">Remarks</span></span>

<span data-ttu-id="0dfc9-107">Cuando el elemento de **cifrado** tiene un valor de WEP, [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) debe establecerse en **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="0dfc9-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="0dfc9-108">El método de cifrado AES se especifica en las especificaciones de [802.1 x](https://ieeexplore.ieee.org/document/1438730) y [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="0dfc9-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="0dfc9-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0dfc9-109">Examples</span></span>

<span data-ttu-id="0dfc9-110">Para ver los perfiles de ejemplo que usan el elemento de **cifrado** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0dfc9-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dfc9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dfc9-111">Requirements</span></span>



| <span data-ttu-id="0dfc9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dfc9-112">Requirement</span></span> | <span data-ttu-id="0dfc9-113">Value</span><span class="sxs-lookup"><span data-stu-id="0dfc9-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0dfc9-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dfc9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0dfc9-115">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0dfc9-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0dfc9-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dfc9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0dfc9-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dfc9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="0dfc9-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0dfc9-118">Redistributable</span></span><br/>          | <span data-ttu-id="0dfc9-119">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="0dfc9-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0dfc9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dfc9-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="0dfc9-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="0dfc9-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0dfc9-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="0dfc9-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="0dfc9-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="0dfc9-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0dfc9-124">**authEncryption (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="0dfc9-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




