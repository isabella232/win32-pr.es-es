---
description: Se admite un subconjunto de la funcionalidad nativa de la API WiFi en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Compatibilidad con la API WiFi nativa en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360801"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="60dfe-103">Compatibilidad con la API WiFi nativa en Windows XP</span><span class="sxs-lookup"><span data-stu-id="60dfe-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="60dfe-104">Se admite un subconjunto de la funcionalidad nativa de la API WiFi en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="60dfe-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="60dfe-105">Esta funcionalidad se incluye de forma predeterminada en Windows XP con SP3.</span><span class="sxs-lookup"><span data-stu-id="60dfe-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="60dfe-106">En Windows XP con SP2, esta funcionalidad se puede agregar mediante la aplicación de una revisión, que se conoce como API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="60dfe-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="60dfe-107">Para obtener más información o descargar la revisión, consulte "los desarrolladores no pueden crear programas cliente inalámbricos que administren perfiles inalámbricos y conexiones a través del servicio de configuración inalámbrica rápida en Microsoft Windows XP Service Pack 2 (SP2)" en la Knowledge base de ayuda y soporte técnico en [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="60dfe-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="60dfe-108">Debido a las diferencias arquitectónicas subyacentes en Windows XP, la API WiFi nativa de tiene algunas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="60dfe-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="60dfe-109">Esta es una lista de limitaciones:</span><span class="sxs-lookup"><span data-stu-id="60dfe-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="60dfe-110">Como máximo, un SSID puede asociarse a un perfil.</span><span class="sxs-lookup"><span data-stu-id="60dfe-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="60dfe-111">Las redes de infraestructura siempre aparecen antes que las redes ad hoc en la lista de perfiles.</span><span class="sxs-lookup"><span data-stu-id="60dfe-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="60dfe-112">Los nombres de perfil se derivan del SSID y el usuario no puede establecerlo en una cadena arbitraria.</span><span class="sxs-lookup"><span data-stu-id="60dfe-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="60dfe-113">No se admiten los tipos de PHY.</span><span class="sxs-lookup"><span data-stu-id="60dfe-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="60dfe-114">No se admite el almacenamiento en caché de clave maestra en pares (PMK).</span><span class="sxs-lookup"><span data-stu-id="60dfe-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="60dfe-115">No se admiten las funciones de extensibilidad del proveedor de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="60dfe-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="60dfe-116">No se admiten los permisos de perfil.</span><span class="sxs-lookup"><span data-stu-id="60dfe-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="60dfe-117">Solo \_ se completa la conexión ACM de notificación de WLAN \_ \_ \_ y las \_ notificaciones de WLAN desconectadas de la notificación de WLAN \_ \_ están disponibles.</span><span class="sxs-lookup"><span data-stu-id="60dfe-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="60dfe-118">No se admiten las opciones de configuración de 802.1 X y EAPOL globales.</span><span class="sxs-lookup"><span data-stu-id="60dfe-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="60dfe-119">Las siguientes funciones son compatibles con Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:</span><span class="sxs-lookup"><span data-stu-id="60dfe-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="60dfe-120">**devolución de llamada de \_ notificación de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="60dfe-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="60dfe-121">**WlanAllocateMemory**</span><span class="sxs-lookup"><span data-stu-id="60dfe-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="60dfe-122">**WlanCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="60dfe-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="60dfe-123">**WlanConnect**</span><span class="sxs-lookup"><span data-stu-id="60dfe-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="60dfe-124">**WlanDeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="60dfe-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="60dfe-125">**WlanDisconnect**</span><span class="sxs-lookup"><span data-stu-id="60dfe-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="60dfe-126">**WlanEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="60dfe-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="60dfe-127">**WlanFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="60dfe-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="60dfe-128">**WlanGetAvailableNetworkList**</span><span class="sxs-lookup"><span data-stu-id="60dfe-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="60dfe-129">**WlanGetProfile**</span><span class="sxs-lookup"><span data-stu-id="60dfe-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="60dfe-130">**WlanGetProfileList**</span><span class="sxs-lookup"><span data-stu-id="60dfe-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="60dfe-131">**WlanOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="60dfe-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="60dfe-132">**WlanQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="60dfe-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="60dfe-133">**WlanReasonCodeToString**</span><span class="sxs-lookup"><span data-stu-id="60dfe-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="60dfe-134">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="60dfe-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="60dfe-135">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="60dfe-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="60dfe-136">**WlanSetInterface**</span><span class="sxs-lookup"><span data-stu-id="60dfe-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="60dfe-137">**WlanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="60dfe-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="60dfe-138">**WlanSetProfileEapXmlUserData**</span><span class="sxs-lookup"><span data-stu-id="60dfe-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="60dfe-139">**WlanSetProfileList**</span><span class="sxs-lookup"><span data-stu-id="60dfe-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="60dfe-140">**WlanSetProfilePosition**</span><span class="sxs-lookup"><span data-stu-id="60dfe-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="60dfe-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60dfe-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="60dfe-142">Acerca de WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="60dfe-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 
