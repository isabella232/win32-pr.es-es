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
# <a name="whats-new-in-native-wifi"></a>Novedades de Wi-Fi nativo

## <a name="windows-10-version-2004"></a>Windows 10, versión 2004

Vea [aprovisionar un perfil de Wi-Fi a través de un sitio web](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

Se ha agregado compatibilidad con la zona activa 2,0 [al \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md). HotSpot 2,0 habilita la conexión automática a los servicios de Wi-Fi públicos mediante las credenciales existentes y la pertenencia a las redes del proveedor de servicios. Los proveedores de servicios especifican cómo se realizan las conexiones con los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas. Consulte la documentación del elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) para obtener más información.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Se han agregado las siguientes características a las API de WiFi nativas en Windows 8 y Windows Server 2012.

Wi-Fi característica directa basada en el desarrollo de la Wi-Fi especificación técnica punto a punto v 1.1 de la Alianza de Wi-Fi (consulte las [especificaciones publicadas de Wi-Fi Alliance](https://www.wi-fi.org/)). El objetivo de la Wi-Fi especificación técnica punto a punto es proporcionar una solución para Wi-Fi la conectividad de dispositivo a dispositivo sin necesidad de que un punto de acceso inalámbrico (AP inalámbrico) Configure la conexión o el uso del mecanismo de Wi-Fi ad hoc (IBSS) existente.

Las funciones siguientes admiten la característica Wi-Fi Direct.

-   [**\_devolución de \_ \_ llamada completa de sesión abierta de WFD \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

Se han agregado las siguientes características a las API de WiFi nativas en Windows 7 y Windows Server 2008 R2.

La red hospedada inalámbrica permite a un único adaptador inalámbrico físico conectarse como cliente a un punto de acceso de hardware (AP), al mismo tiempo que actúa como un punto de conexión de software que permite que otros dispositivos compatibles con la red inalámbrica se conecten a él.

Las funciones siguientes admiten la característica red hospedada inalámbrica.

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Las siguientes estructuras nuevas que funcionan con redes hospedadas inalámbricas.

-   [**\_configuración de \_ conexión de red hospedada de \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**\_cambio de \_ \_ \_ Estado del mismo nivel de datos \_ hospedados \_ de WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**\_ \_ \_ Estado del mismo nivel de red HOSPEDAda de WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**\_Estado de \_ radio de red hospedada de \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**\_configuración de \_ seguridad de red hospedada de \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_cambio de \_ Estado de red hospedada de \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_Estado de \_ red hospedada de WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Las siguientes enumeraciones nuevas que funcionan con redes hospedadas inalámbricas.

-   [**\_código de \_ notificación de red hospedada por \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**\_código de \_ operación de red hospedada de WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_Estado de \_ \_ autenticación del mismo nivel de red HOSPEDAda de WLAN \_ \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_motivo de \_ red hospedada de WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**\_Estado de \_ red hospedada de WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la red hospedada inalámbrica](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso de redes hospedadas inalámbricas y conexión compartida a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



