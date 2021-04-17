---
description: Indica si la clave compartida será una clave de red o una frase de contraseña.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento keyType (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677961"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="3ef97-103">Elemento keyType (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="3ef97-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="3ef97-104">El elemento keyType (sharedKey) indica si la clave compartida será una clave de red o una frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="3ef97-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
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
```

<span data-ttu-id="3ef97-105">El elemento se define mediante el elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef97-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ef97-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ef97-106">Remarks</span></span>

<span data-ttu-id="3ef97-107">Cuando el elemento de [**cifrado**](wlan-profileschema-encryption-authencryption-element.md) tiene un valor de WEP, **KeyType** debe establecerse en **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="3ef97-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="3ef97-108">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3ef97-108">Examples</span></span>

<span data-ttu-id="3ef97-109">Para ver los perfiles de ejemplo que usan el elemento **KeyType** , vea ejemplo [de perfil sin difusión](non-broadcast-profile-sample.md), ejemplo de perfil [de WPA-Personal](wpa-personal-profile-sample.md)y [ejemplo de Perfil de WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3ef97-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef97-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ef97-110">Requirements</span></span>



| <span data-ttu-id="3ef97-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef97-111">Requirement</span></span> | <span data-ttu-id="3ef97-112">Value</span><span class="sxs-lookup"><span data-stu-id="3ef97-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3ef97-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef97-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef97-114">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3ef97-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3ef97-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef97-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef97-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ef97-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="3ef97-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3ef97-117">Redistributable</span></span><br/>          | <span data-ttu-id="3ef97-118">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="3ef97-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3ef97-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ef97-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ef97-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="3ef97-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3ef97-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="3ef97-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="3ef97-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ef97-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3ef97-123">**sharedKey (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="3ef97-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




