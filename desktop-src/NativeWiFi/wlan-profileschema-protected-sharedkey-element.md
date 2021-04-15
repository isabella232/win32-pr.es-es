---
description: Indica si una clave compartida está cifrada.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento Protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677331"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="4b8f7-103">Elemento Protected (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="4b8f7-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="4b8f7-104">El elemento Protected (sharedKey) indica si una clave compartida está cifrada.</span><span class="sxs-lookup"><span data-stu-id="4b8f7-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="4b8f7-105">El elemento se define mediante el elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4b8f7-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8f7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b8f7-106">Remarks</span></span>

<span data-ttu-id="4b8f7-107">En Windows Vista y Windows Server 2008, **Protected** siempre tiene el valor true si el perfil se recuperó del almacén de perfiles (por ejemplo, mediante una llamada a [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span><span class="sxs-lookup"><span data-stu-id="4b8f7-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="4b8f7-108">En el caso de los perfiles pensados para usarse en Windows XP con Service Pack 3 (SP3) o la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2), **Protected** debe tener un valor de false.</span><span class="sxs-lookup"><span data-stu-id="4b8f7-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="4b8f7-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4b8f7-109">Examples</span></span>

<span data-ttu-id="4b8f7-110">Para ver los perfiles de ejemplo que usan el elemento **protegido** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="4b8f7-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8f7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b8f7-111">Requirements</span></span>



| <span data-ttu-id="4b8f7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8f7-112">Requirement</span></span> | <span data-ttu-id="4b8f7-113">Value</span><span class="sxs-lookup"><span data-stu-id="4b8f7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4b8f7-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b8f7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8f7-115">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="4b8f7-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b8f7-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b8f7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8f7-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b8f7-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="4b8f7-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4b8f7-118">Redistributable</span></span><br/>          | <span data-ttu-id="4b8f7-119">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="4b8f7-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4b8f7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b8f7-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b8f7-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="4b8f7-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4b8f7-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="4b8f7-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="4b8f7-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="4b8f7-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4b8f7-124">**sharedKey (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="4b8f7-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




