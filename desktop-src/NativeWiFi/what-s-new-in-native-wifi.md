---
description: Novedades de Wi-Fi nativo
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novedades de Wi-Fi nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687181"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="329e1-103">Novedades de Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="329e1-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="329e1-104">Windows 10, versión 2004</span><span class="sxs-lookup"><span data-stu-id="329e1-104">Windows 10, version 2004</span></span>

<span data-ttu-id="329e1-105">Vea [aprovisionar un perfil de Wi-Fi a través de un sitio web](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="329e1-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="329e1-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="329e1-106">Windows 10</span></span>

<span data-ttu-id="329e1-107">Se ha agregado compatibilidad con la zona activa 2,0 [al \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="329e1-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="329e1-108">HotSpot 2,0 habilita la conexión automática a los servicios de Wi-Fi públicos mediante las credenciales existentes y la pertenencia a las redes del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="329e1-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="329e1-109">Los proveedores de servicios especifican cómo se realizan las conexiones con los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas.</span><span class="sxs-lookup"><span data-stu-id="329e1-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="329e1-110">Consulte la documentación del elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="329e1-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="329e1-111">Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="329e1-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="329e1-112">Se han agregado las siguientes características a las API de WiFi nativas en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="329e1-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="329e1-113">Wi-Fi característica directa basada en el desarrollo de la Wi-Fi especificación técnica punto a punto v 1.1 de la Alianza de Wi-Fi (consulte las [especificaciones publicadas de Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="329e1-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="329e1-114">El objetivo de la Wi-Fi especificación técnica punto a punto es proporcionar una solución para Wi-Fi la conectividad de dispositivo a dispositivo sin necesidad de que un punto de acceso inalámbrico (AP inalámbrico) Configure la conexión o el uso del mecanismo de Wi-Fi ad hoc (IBSS) existente.</span><span class="sxs-lookup"><span data-stu-id="329e1-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="329e1-115">Las funciones siguientes admiten la característica Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="329e1-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="329e1-116">**\_devolución de \_ \_ llamada completa de sesión abierta de WFD \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="329e1-117">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="329e1-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="329e1-118">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="329e1-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="329e1-119">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="329e1-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="329e1-120">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="329e1-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="329e1-121">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="329e1-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="329e1-122">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="329e1-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="329e1-123">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="329e1-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="329e1-124">Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="329e1-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="329e1-125">Se han agregado las siguientes características a las API de WiFi nativas en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="329e1-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="329e1-126">La red hospedada inalámbrica permite a un único adaptador inalámbrico físico conectarse como cliente a un punto de acceso de hardware (AP), al mismo tiempo que actúa como un punto de conexión de software que permite que otros dispositivos compatibles con la red inalámbrica se conecten a él.</span><span class="sxs-lookup"><span data-stu-id="329e1-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="329e1-127">Las funciones siguientes admiten la característica red hospedada inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="329e1-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="329e1-128">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="329e1-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="329e1-129">**WlanHostedNetworkForceStop**</span><span class="sxs-lookup"><span data-stu-id="329e1-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="329e1-130">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="329e1-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="329e1-131">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="329e1-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="329e1-132">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="329e1-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="329e1-133">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="329e1-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="329e1-134">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="329e1-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="329e1-135">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="329e1-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="329e1-136">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="329e1-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="329e1-137">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="329e1-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="329e1-138">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="329e1-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="329e1-139">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="329e1-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="329e1-140">Las siguientes estructuras nuevas que funcionan con redes hospedadas inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="329e1-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="329e1-141">**\_configuración de \_ conexión de red hospedada de \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="329e1-142">**\_cambio de \_ \_ \_ Estado del mismo nivel de datos \_ hospedados \_ de WLAN**</span><span class="sxs-lookup"><span data-stu-id="329e1-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="329e1-143">**\_ \_ \_ Estado del mismo nivel de red HOSPEDAda de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="329e1-144">**\_Estado de \_ radio de red hospedada de \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="329e1-145">**\_configuración de \_ seguridad de red hospedada de \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="329e1-146">**\_cambio de \_ Estado de red hospedada de \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="329e1-147">**\_Estado de \_ red hospedada de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="329e1-148">Las siguientes enumeraciones nuevas que funcionan con redes hospedadas inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="329e1-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="329e1-149">**\_código de \_ notificación de red hospedada por \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="329e1-150">**\_código de \_ operación de red hospedada de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="329e1-151">**\_Estado de \_ \_ autenticación del mismo nivel de red HOSPEDAda de WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="329e1-152">**\_motivo de \_ red hospedada de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="329e1-153">**\_Estado de \_ red hospedada de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="329e1-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="329e1-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="329e1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="329e1-155">Acerca de la red hospedada inalámbrica</span><span class="sxs-lookup"><span data-stu-id="329e1-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="329e1-156">Uso de redes hospedadas inalámbricas y conexión compartida a Internet</span><span class="sxs-lookup"><span data-stu-id="329e1-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



