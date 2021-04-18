---
description: Indica si se va a conectar a una red oculta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonbroadcast (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677535"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="fb313-103">Elemento nonbroadcast (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="fb313-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="fb313-104">El elemento nonbroadcast (SSIDConfig) indica si se va a conectar a una red oculta.</span><span class="sxs-lookup"><span data-stu-id="fb313-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="fb313-105">Si una red no emite su SSID, se denomina red oculta.</span><span class="sxs-lookup"><span data-stu-id="fb313-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="fb313-106">Si se establecen varios SSID en el perfil, todos deben tener el mismo valor de no difusión.</span><span class="sxs-lookup"><span data-stu-id="fb313-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="fb313-107">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **ESS**, este valor puede ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="fb313-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="fb313-108">Si este elemento no está presente, el valor predeterminado es "false".</span><span class="sxs-lookup"><span data-stu-id="fb313-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="fb313-109">Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en **IBSS**, este valor debe ser "false".</span><span class="sxs-lookup"><span data-stu-id="fb313-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="fb313-110">Si este elemento no está presente, el valor predeterminado es "false".</span><span class="sxs-lookup"><span data-stu-id="fb313-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="fb313-111">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="fb313-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="fb313-112">El elemento se define mediante el elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fb313-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fb313-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fb313-113">Examples</span></span>

<span data-ttu-id="fb313-114">Para ver un perfil de ejemplo que usa el elemento de no **difusión** , vea [ejemplo de perfil sin difusión](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fb313-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb313-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb313-115">Requirements</span></span>



| <span data-ttu-id="fb313-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb313-116">Requirement</span></span> | <span data-ttu-id="fb313-117">Value</span><span class="sxs-lookup"><span data-stu-id="fb313-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb313-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb313-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb313-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb313-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb313-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb313-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb313-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb313-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb313-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb313-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb313-123">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="fb313-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fb313-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="fb313-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fb313-125">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="fb313-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fb313-126">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="fb313-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




