---
description: Debido a las diferencias arquitectónicas subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el esquema de Perfil de WLAN \_ y el material de referencia de esquema de Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidad con perfiles inalámbricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545678"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="60718-103">Compatibilidad con perfiles inalámbricos</span><span class="sxs-lookup"><span data-stu-id="60718-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="60718-104">Debido a las diferencias arquitectónicas subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el [ \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md) y el material de referencia de esquema de [Onex](onexschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="60718-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="60718-105">Todos los perfiles que cumplen con los requisitos de Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2 también se pueden usar en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="60718-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="60718-106">\_Compatibilidad con perfiles de WLAN</span><span class="sxs-lookup"><span data-stu-id="60718-106">WLAN\_profile Support</span></span>

<span data-ttu-id="60718-107">Los siguientes \_ elementos de Perfil de WLAN no se admiten en Windows XP con SP3 o la API de LAN inalámbrica para Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="60718-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="60718-108">Conectividad (IHV)</span><span class="sxs-lookup"><span data-stu-id="60718-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="60718-109">IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="60718-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="60718-110">OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="60718-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="60718-111">phyType (conectividad)</span><span class="sxs-lookup"><span data-stu-id="60718-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="60718-112">PMKCacheMode (seguridad)</span><span class="sxs-lookup"><span data-stu-id="60718-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="60718-113">PMKCacheSize (seguridad)</span><span class="sxs-lookup"><span data-stu-id="60718-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="60718-114">PMKCacheTTL (seguridad)</span><span class="sxs-lookup"><span data-stu-id="60718-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="60718-115">preAuthMode (seguridad)</span><span class="sxs-lookup"><span data-stu-id="60718-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="60718-116">preAuthThrottle (seguridad)</span><span class="sxs-lookup"><span data-stu-id="60718-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="60718-117">seguridad (IHV)</span><span class="sxs-lookup"><span data-stu-id="60718-117">security (IHV)</span></span>
-   <span data-ttu-id="60718-118">tipo (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="60718-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="60718-119">useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="60718-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="60718-120">En la tabla siguiente se muestran los elementos de Perfil de WLAN \_ con valores restringidos para Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="60718-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="60718-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="60718-121">Element</span></span>                                                                               | <span data-ttu-id="60718-122">Restricción</span><span class="sxs-lookup"><span data-stu-id="60718-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60718-123">**nombre (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="60718-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="60718-124">El elemento Name se omite cuando el perfil se guarda en el almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="60718-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="60718-125">El nombre del perfil se deriva automáticamente del SSID de la red.</span><span class="sxs-lookup"><span data-stu-id="60718-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="60718-126">En el caso de los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red.</span><span class="sxs-lookup"><span data-stu-id="60718-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="60718-127">En el caso de los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="60718-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="60718-128">**protegido (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="60718-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="60718-129">Debe tener un valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="60718-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="60718-130">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="60718-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="60718-131">Restringido a un elemento [**SSID secundario (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="60718-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="60718-132">Compatibilidad con OneX</span><span class="sxs-lookup"><span data-stu-id="60718-132">OneX Support</span></span>

<span data-ttu-id="60718-133">Solo se admite el elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) en Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="60718-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="60718-134">Otros elementos OneX, si están presentes en un perfil, se omitirán.</span><span class="sxs-lookup"><span data-stu-id="60718-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60718-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60718-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60718-136">Acerca de la API nativa WiFi</span><span class="sxs-lookup"><span data-stu-id="60718-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="60718-137">Compatibilidad con la API WiFi nativa en Windows XP</span><span class="sxs-lookup"><span data-stu-id="60718-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



