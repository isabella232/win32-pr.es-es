---
description: Determina el comportamiento de itinerancia de una red conectada automáticamente cuando una red más preferida está dentro del alcance.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: AutoSwitch (WLANProfile) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908339"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="9f218-103">AutoSwitch (WLANProfile) (elemento)</span><span class="sxs-lookup"><span data-stu-id="9f218-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="9f218-104">El elemento AutoSwitch (WLANProfile) determina el comportamiento de itinerancia de una red conectada automáticamente cuando una red más preferida está dentro del alcance.</span><span class="sxs-lookup"><span data-stu-id="9f218-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="9f218-105">.</span><span class="sxs-lookup"><span data-stu-id="9f218-105">.</span></span> <span data-ttu-id="9f218-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9f218-106">This element is optional.</span></span>

<span data-ttu-id="9f218-107">Si AutoSwitch es "true" y [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", se debe intentar una conexión a una red preferida cada vez que una red más favorita entra en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="9f218-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="9f218-108">Una red más preferida es la que se ordena más arriba en la lista de redes inalámbricas preferidas.</span><span class="sxs-lookup"><span data-stu-id="9f218-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="9f218-109">Este intento de conexión se produce cuando se conecta a otra red.</span><span class="sxs-lookup"><span data-stu-id="9f218-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="9f218-110">Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "auto", este valor puede ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="9f218-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="9f218-111">Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) se establece en "manual", este valor debe establecerse en "false".</span><span class="sxs-lookup"><span data-stu-id="9f218-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="9f218-112">Este elemento no tiene ningún efecto en una red conectada manualmente.</span><span class="sxs-lookup"><span data-stu-id="9f218-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="9f218-113">Un valor de AutoSwitch establecido en "true" da como resultado una mayor frecuencia de detección periódica de nuevas redes.</span><span class="sxs-lookup"><span data-stu-id="9f218-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="9f218-114">Esto puede producir una mayor contaminación de la frecuencia de radio de estos exámenes periódicos y el mayor consumo de energía que usa el adaptador de red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="9f218-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="9f218-115">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="9f218-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="9f218-116">Estos cambios están diseñados para reducir la contaminación de la radiofrecuencia, el consumo de energía y la interrupción del tráfico en tiempo real a través de redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="9f218-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="9f218-117">La configuración predeterminada de **AutoSwitch** cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9f218-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="9f218-118">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="9f218-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="9f218-119">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f218-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="9f218-120">Se recomienda que el valor del elemento **AutoSwitch** que usa una aplicación en un perfil de LAN inalámbrica se establezca en "false" para reducir la frecuencia de detección periódica de nuevas redes, a menos que sea absolutamente necesario que una aplicación establezca este valor en "true".</span><span class="sxs-lookup"><span data-stu-id="9f218-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="9f218-121">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="9f218-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="9f218-122">El elemento **AutoSwitch** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9f218-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9f218-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f218-123">Examples</span></span>

<span data-ttu-id="9f218-124">Para ver los perfiles de ejemplo que usan el elemento **AutoSwitch** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9f218-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f218-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f218-125">Requirements</span></span>



| <span data-ttu-id="9f218-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f218-126">Requirement</span></span> | <span data-ttu-id="9f218-127">Value</span><span class="sxs-lookup"><span data-stu-id="9f218-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f218-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f218-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f218-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9f218-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f218-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f218-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f218-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f218-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f218-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f218-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f218-133">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="9f218-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9f218-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="9f218-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="9f218-135">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="9f218-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9f218-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="9f218-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




