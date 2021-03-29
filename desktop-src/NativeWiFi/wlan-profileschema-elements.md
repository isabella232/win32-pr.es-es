---
description: El esquema de Perfil de WLAN \_ define los siguientes elementos.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile elementos de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810381"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="ea44e-103">Elementos de esquema de Perfil de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="ea44e-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="ea44e-104">El esquema de Perfil de WLAN \_ define los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="ea44e-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="ea44e-105">La mayoría de los elementos se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v1` , excepto en el caso de [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), que se encuentra en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="ea44e-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="ea44e-106">En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil.</span><span class="sxs-lookup"><span data-stu-id="ea44e-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="ea44e-107">Se aplica el orden de los elementos.</span><span class="sxs-lookup"><span data-stu-id="ea44e-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="ea44e-108">No todos los elementos están en cada perfil, ya que algunos elementos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ea44e-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="ea44e-109">En esta lista no se muestran todos los elementos posibles que pueden aparecer en un perfil inalámbrico, ya que los elementos se pueden agregar en **xs: cualquier** punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="ea44e-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="ea44e-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="ea44e-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="ea44e-111">**nombre (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="ea44e-112">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="ea44e-113">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="ea44e-114">**Hex (SSID)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="ea44e-115">**nombre (SSID)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="ea44e-116">**nondifusión (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="ea44e-117">**Hotspot2 (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="ea44e-118">**NombreDeDominio (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="ea44e-119">**NAIRealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="ea44e-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="ea44e-121">**RoamingConsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="ea44e-122">**connectionType (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="ea44e-123">**connectionMode (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="ea44e-124">**AutoSwitch (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="ea44e-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="ea44e-126">**Conectividad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="ea44e-127">**phyType (conectividad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="ea44e-128">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="ea44e-129">**authEncryption (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="ea44e-130">**autenticación (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="ea44e-131">**cifrado (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="ea44e-132">**useOneX (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="ea44e-133">**FIPSMode (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="ea44e-134">**sharedKey (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="ea44e-135">**keyType (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="ea44e-136">**protegido (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="ea44e-137">**keyMaterial (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="ea44e-138">**keyIndex (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="ea44e-139">**PMKCacheMode (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="ea44e-140">**PMKCacheTTL (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="ea44e-141">**PMKCacheSize (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="ea44e-142">**preAuthMode (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="ea44e-143">**preAuthThrottle (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="ea44e-144">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="ea44e-145">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="ea44e-146">**OUI (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="ea44e-147">**tipo (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="ea44e-148">**Conectividad (IHV)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="ea44e-149">**seguridad (IHV)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="ea44e-150">**useMSOneX (IHV)**</span><span class="sxs-lookup"><span data-stu-id="ea44e-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



