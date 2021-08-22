---
description: Novedades de Wi-Fi nativo
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novedades de Wi-Fi nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a9430fa2c1645d574f8b4ab851a8cf5ce1407139cfe63a6aabeb3ebfd57abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064865"
---
# <a name="whats-new-in-native-wifi"></a>Novedades de Wi-Fi nativo

## <a name="windows-10-version-2004"></a>Windows 10, versión 2004

Consulte [Aprovisionamiento de un Wi-Fi a través de un sitio web](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

Se ha agregado compatibilidad con Hotspot 2.0 al esquema [de \_ perfil WLAN.](wlan-profileschema-schema.md) Hotspot 2.0 permite la conexión automática a servicios de Wi-Fi públicos mediante credenciales existentes y pertenencia a redes de proveedor de servicios. Los proveedores de servicios especifican cómo se realizan las conexiones mediante los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas. Consulte la documentación [**del elemento Hotspot2**](wlan-profileschema-hotspot2-element.md) para obtener más información.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Se han agregado las siguientes características a las API de Wi-Fi nativas en Windows 8 y Windows Server 2012.

Una característica Wi-Fi Direct basada en el desarrollo de la especificación técnica punto a punto de Wi-Fi v1.1 por parte de Wi-Fi Alliance (consulte Especificaciones publicadas de [Wi-Fi Alliance).](https://www.wi-fi.org/) El objetivo de la especificación técnica punto a punto de Wi-Fi es proporcionar una solución para la conectividad de dispositivo Wi-Fi dispositivo sin necesidad de un punto de acceso inalámbrico (AP inalámbrico) para configurar la conexión o el uso del mecanismo Wi-Fi adhoc (IBSS) existente.

Las siguientes funciones admiten la característica Wi-Fi Direct.

-   [**DEVOLUCIÓN DE LLAMADA \_ COMPLETA DE SESIÓN ABIERTA \_ \_ \_ DE WFD**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

Se han agregado las siguientes características a las API de Wi-Fi nativas en Windows 7 y Windows Server 2008 R2.

La red hospedada inalámbrica permite que un único adaptador inalámbrico físico se conecte como cliente a un punto de acceso de hardware (AP), al mismo tiempo que actúa como un AP de software que permite que otros dispositivos compatibles con la tecnología inalámbrica se conecten a él.

Las siguientes funciones admiten la característica red hospedada inalámbrica.

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

Las siguientes estructuras nuevas que funcionan con red hospedada inalámbrica.

-   [**CONFIGURACIÓN DE \_ CONEXIÓN DE \_ RED HOSPEDADA \_ EN \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**CAMBIO \_ DE ESTADO DEL MISMO NIVEL DE DATOS DE RED \_ \_ \_ \_ \_ HOSPEDADA EN WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**ESTADO DEL \_ MISMO NIVEL DE RED \_ \_ HOSPEDADA EN \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**ESTADO \_ DE RADIO DE RED \_ \_ HOSPEDADA EN \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**CONFIGURACIÓN DE \_ SEGURIDAD DE \_ RED HOSPEDADA \_ EN \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**CAMBIO \_ DE ESTADO DE RED \_ \_ HOSPEDADA EN \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**ESTADO DE \_ RED HOSPEDADA \_ EN WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Las siguientes enumeraciones nuevas que funcionan con red hospedada inalámbrica.

-   [**CÓDIGO DE \_ NOTIFICACIÓN \_ DE RED \_ HOSPEDADA EN \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**CÓDIGO \_ DE OPERACIÓN DE RED \_ \_ HOSPEDADA EN WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**ESTADO DE \_ AUTENTICACIÓN \_ DEL MISMO NIVEL DE RED \_ \_ \_ HOSPEDADA EN WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**MOTIVO \_ DE LA RED \_ HOSPEDADA EN WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**ESTADO \_ DE RED \_ HOSPEDADA DE WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la red hospedada inalámbrica](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso de redes hospedadas inalámbricas y uso compartido de conexiones a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



