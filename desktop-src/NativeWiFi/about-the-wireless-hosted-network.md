---
description: Acerca de la red hospedada inalámbrica
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Acerca de la red hospedada inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15be48bb5ef10754b11a0b3d4bb7d8e31ace9752
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277359"
---
# <a name="about-the-wireless-hosted-network"></a>Acerca de la red hospedada inalámbrica

La red hospedada inalámbrica es una nueva característica de WLAN compatible con Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado. Esta característica implementa dos funciones principales:

-   La virtualización de un adaptador inalámbrico físico en más de un adaptador inalámbrico virtual a veces se denomina Wi-Fi virtual.
-   Un punto de acceso inalámbrico (AP) basado en software, que a veces se denomina SoftAP, que usa un adaptador inalámbrico virtual designado.

Estas dos funciones coexisten en un sistema Windows juntas. Habilitar o deshabilitar la red hospedada inalámbrica habilita o deshabilita el Wi-Fi virtual y SoftAP. No es posible habilitar o deshabilitar estas dos funciones por separado en Windows.

Con esta característica, un equipo Windows puede usar un solo adaptador inalámbrico físico para conectarse como cliente a un punto de acceso de hardware (AP), al mismo tiempo que actúa como un punto de conexión de software que permite que otros dispositivos compatibles con redes inalámbricas se conecten a él. Esta característica requiere la instalación de un adaptador inalámbrico compatible con redes hospedadas en el equipo local. El controlador del adaptador inalámbrico debe implementar el modelo de controlador de dispositivo de LAN inalámbrica definido por Microsoft para su uso en Windows 7. Para recibir el logotipo de Windows 7, un controlador inalámbrico debe implementar la característica de red hospedada inalámbrica.

Hay como máximo una red hospedada inalámbrica habilitada en cualquier momento en el equipo local y la red hospedada inalámbrica solo usará un adaptador inalámbrico. Si hay más de un adaptador inalámbrico compatible con redes hospedadas, Windows elegirá un adaptador para su uso con la red hospedada inalámbrica. Cuando se usan las API de red hospedada, el adaptador inalámbrico compatible con redes hospedadas se virtualiza como máximo 3 adaptadores lógicos:

-   Adaptador de estación (STA) para su uso por parte de aplicaciones de cliente o ad hoc inalámbricas. El adaptador de STA hereda toda la configuración del adaptador inalámbrico físico original y exhibe los mismos comportamientos que el adaptador físico. Conceptualmente, puede ver el adaptador de STA como idéntico al adaptador físico después de la virtualización. El adaptador de STA siempre está en el sistema, siempre que esté presente el adaptador físico inalámbrico correspondiente.
-   Un adaptador de AP para que la red hospedada inalámbrica la use para hospedar SoftAP. El adaptador de AP está presente en el sistema Windows solo después de que la red hospedada inalámbrica se invoca por primera vez (cuando se llama por primera vez a la función [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Una vez creada, el adaptador de AP permanecerá en el sistema hasta que la red hospedada inalámbrica esté deshabilitada. Si la red hospedada inalámbrica está habilitada en algún momento posterior, el adaptador de AP volverá a aparecer en el sistema.
-   Adaptador de estación virtual (VSTA) para que lo usen los proveedores de hardware para extender la funcionalidad de red hospedada inalámbrica en Windows. El adaptador de VSTA es opcional y solo se puede crear en el sistema mediante el servicio IHV correspondiente. A diferencia del adaptador de AP, el adaptador de VSTA solo existe en el sistema Windows desde el momento en que el servicio IHV inicializa el adaptador hasta el momento en que el servicio IHV libera el adaptador.

Wi-Fi virtual asigna los adaptadores lógicos a los puertos NDIS. Windows decide el enlace de los adaptadores STA, AP y VSTA a puertos NDIS específicos. El adaptador de STA siempre está enlazado al puerto 0. El adaptador de AP se enlaza al siguiente puerto NDIS disponible cuando se inicia la virtualización y el enlace sigue siendo el mismo hasta que la virtualización finaliza cuando se deshabilita la red hospedada inalámbrica. El adaptador de VSTA se enlaza al siguiente puerto NDIS disponible cuando lo inicializa el servicio IHV correspondiente y el enlace permanece igual hasta que el servicio IHV lo libera.

Es posible que el adaptador de VSTA se cree para que lo usen los IHV sin crear el adaptador de SoftAP.

Las siguientes combinaciones son válidas para un adaptador físico con virtualización:

-   Adaptador de STA.
-   Adaptadores STA y PA.
-   Adaptadores de STA y VSTA.
-   Adaptadores de STA, AP y VSTA.

Excepto en el caso del adaptador STA, todas las demás combinaciones solo son válidas cuando la red hospedada inalámbrica está habilitada. Como en el caso del adaptador de un solo STA, es el adaptador físico si la red hospedada inalámbrica está deshabilitada. Si la red hospedada inalámbrica está habilitada, es el adaptador de STA cuando la red hospedada inalámbrica no se ha invocado nunca en el sistema.

El protocolo de puente de capa 2 está prohibido entre el adaptador de AP y cualquier otro adaptador del sistema. La misma restricción se aplica al adaptador de VSTA cuando está presente en el sistema.

La característica red hospedada inalámbrica de Windows implementa un SoftAP. Sin embargo, esta SoftAP no está diseñada para reemplazar dispositivos AP inalámbricos basados en hardware. En concreto, si la red hospedada inalámbrica se está ejecutando cuando el equipo entra en modo de suspensión (en espera), hibernación o antes de que se reinicie el equipo, se detendrá la red hospedada inalámbrica. La red hospedada inalámbrica no se reiniciará automáticamente después de que el equipo se reanude de la suspensión, la hibernación o el reinicio. Además, SoftAP no proporciona la resolución DNS. En el caso de que no haya un servidor DNS externo disponible mediante conexión compartida a Internet (consulte la explicación de ICS a continuación), la resolución de nombre de dominio completo (FQDN) entre dos equipos o dispositivos conectados con el SoftAP, incluido el equipo que hospeda SoftAP, solo funcionaría si ambas entidades marcan el tipo de red de la red SoftAP como privada (hogar o trabajo en la categoría de red emergente). Dado que el equipo que hospeda el SoftAP siempre marca el tipo de red SoftAP como privado, solo los equipos o dispositivos conectados a SoftAP deben marcar el tipo de red SoftAP como privado para que funcione la resolución de FQDN.

Las redes SoftAP y ad hoc se excluyen mutuamente en el mismo adaptador físico. Si SoftAP se está ejecutando en el adaptador de AP y un usuario o aplicación inicia redes ad hoc en el adaptador de STA, se apagará SoftAP. IIF las redes ad hoc se están ejecutando en el adaptador de STA; se producirá un error al intentar iniciar SoftAP en el adaptador de AP.

Para proporcionar protección a las comunicaciones inalámbricas entre el equipo que hospeda SoftAP y los dispositivos que se conectan a SoftAP, la red hospedada inalámbrica requiere que todos los dispositivos conectados usen el conjunto de cifrado WPA2-PSK/AES. La clave compartida es un valor de carácter 63 generado por Windows cuando la red hospedada inalámbrica se invoca por primera vez (cuando se llama por primera vez a la función [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Un usuario o una aplicación no puede cambiar el valor de esta clave compartida, pero una aplicación puede solicitar al sistema operativo que vuelva a generar una nueva clave mediante una llamada a la función [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) o que un usuario puede solicitar al sistema operativo que vuelva a generar una nueva clave mediante los comandos **netsh de WLAN** . Esta clave compartida se denomina clave principal o de sistema para la red hospedada inalámbrica y es persistente en el inicio y la detención de la red hospedada inalámbrica. Esta clave principal se denomina "clave de seguridad del sistema" en comandos **netsh de WLAN** .

Para facilitar el uso, la red hospedada inalámbrica también admite el concepto de una clave de seguridad secundaria o de usuario que es más fácil de usar, pero podría ser menos segura. Esta clave secundaria se denomina "clave de seguridad de usuario" en comandos **netsh de WLAN** . Windows no genera la clave secundaria. El usuario debe proporcionar el valor de esta clave. Un usuario o una aplicación puede establecer o cambiar el valor de clave mediante una llamada a la función [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) o mediante los comandos **netsh wlan** . La clave secundaria se puede establecer para ser persistente o temporal. En el caso de una clave temporal, si la red hospedada inalámbrica ya se está ejecutando, la clave secundaria será válida hasta que se detenga la red hospedada inalámbrica. En el caso de una clave temporal, si la red hospedada inalámbrica no se está ejecutando, solo será válida entre el siguiente inicio y detención de la red hospedada inalámbrica.

Hay exactamente una clave principal y, como máximo, una clave secundaria para la Hetwork hospedada inalámbrica en cualquier equipo. Cualquier dispositivo aprovisionado a través de Wi-Fi instalación protegida (WPS) recibirá la clave principal. Otros dispositivos configurados manualmente pueden utilizar cualquiera de las dos claves. Cada vez que se cambia una clave, cualquier dispositivo con el valor de clave anterior no podrá conectarse a la red hospedada inalámbrica sin que se vuelva a aprovisionar con la nueva clave. Sin embargo, los dispositivos con la otra clave sin cambios seguirán pudiendo conectarse a la red hospedada inalámbrica.

Una aplicación puede registrarse para recibir notificaciones de red hospedada inalámbrica, por lo que se enviará una notificación de WLAN a la devolución de llamada de la aplicación cuando cambien las propiedades en la red hospedada inalámbrica. Una aplicación se registra para las notificaciones de red hospedada inalámbrica mediante una llamada a [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) con el parámetro *dwNotifSource* establecido para incluir el origen de la notificación de WLAN \_ \_ \_ HNWK bit.

Windows proporciona a los administradores de TI dos maneras de administrar la característica de red hospedada inalámbrica. En el caso de los equipos que son miembros de un dominio, los administradores pueden usar la Directiva de grupo para no permitir la red hospedada inalámbrica. Mediante los comandos **netsh de WLAN** , un administrador puede habilitar o deshabilitar la red hospedada inalámbrica localmente en el equipo.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Escenarios admitidos para redes hospedadas inalámbricas

La red hospedada inalámbrica habilita dos escenarios principales para equipos Windows:

• La capacidad de proporcionar una red de área personal inalámbrica (PAN inalámbrica) para su uso con otros dispositivos inalámbricos.

• Uso compartido de conexión de red para su uso por parte de otros equipos y dispositivos.

La PAN inalámbrica es el escenario principal que la red hospedada inalámbrica habilita por sí misma. Una vez que la red hospedada inalámbrica se inicia en un equipo, cualquier dispositivo compatible con redes inalámbricas que admita WPA2-PSK/AES podrá conectarse al softAP como si se estuviera conectando a un punto de conexión de hardware normal. Los dispositivos conectados a la red hospedada inalámbrica forman una PAN inalámbrica, donde pueden intercambiar información con el equipo de Windows que hospeda el SoftAP y entre ellos.

El uso compartido de conexión de red para su uso por parte de otros equipos y dispositivos requiere el uso de conexión compartida a Internet (ICS). En este escenario, la interfaz pública de ICS es la conexión compartida mientras que la interfaz privada es el adaptador virtual que hospeda el SoftAP. La conexión compartida puede ser una conexión Ethernet, LAN inalámbrica o WAN inalámbrica. En el caso de una conexión LAN inalámbrica, la interfaz pública de ICS puede ser de otro adaptador de LAN inalámbrica o del adaptador virtual de estación en el mismo adaptador inalámbrico físico que hospeda la SoftAP. El uso más común para el uso compartido de redes es compartir una conexión a Internet, donde la red de la interfaz pública de ICS tiene acceso a Internet.

La red hospedada inalámbrica interactúa con Wi-Fi instalación protegida (WPS), otra característica importante nueva de Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado. La red hospedada inalámbrica y WPS admiten un escenario que aprovisiona un dispositivo compatible con WPS para un punto de conexión de hardware compatible con la WPS. En este caso, el SoftAP hospedado en Windows se invoca en segundo plano para insertar el perfil de AP de hardware en el dispositivo compatible con WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Acceso de usuarios y aplicaciones a la red hospedada inalámbrica

Los usuarios finales interactúan con la característica red hospedada inalámbrica de Windows mediante aplicaciones de terceros o comandos **netsh** . Actualmente no hay ninguna interfaz de usuario nativa para configurar o administrar la red hospedada inalámbrica en Windows 7 o en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.

Las aplicaciones de terceros y los comandos **netsh** se basan en el uso de las funciones de red hospedadas por redes inalámbricas públicas. Este conjunto de funciones proporciona un conjunto completo de funcionalidades para administrar la red hospedada inalámbrica en Windows 7 y en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.

A continuación se muestra una lista de las funciones de red hospedada inalámbrica y las acciones comunes de un punto de vista de usuario final en las que la función se utilizaría para:



| Funciones usadas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Inicie la red hospedada inalámbrica.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Detenga la red hospedada inalámbrica.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configure las opciones de red hospedada inalámbrica (cambie el SSID, cambie la clave secundaria o solicite que se vuelva a generar la clave principal).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Consulte la información y la configuración de red hospedada inalámbrica (estado, SSID, clave secundaria, clave principal o una lista de los dispositivos conectados actualmente).<br/> |



 

Los comandos **netsh** están pensados para su uso por parte de usuarios avanzados o administradores.

*Netsh.exe* tiene muchos subcomandos para LAN inalámbrica. Puede encontrar una lista completa de las opciones de **netsh** y LAN inalámbrica en el símbolo del sistema. para ello, escriba lo siguiente:

**netsh wlan/?**

La documentación de todos los comandos Netsh para LAN inalámbrica también está disponible en línea en TechNet. Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

A continuación se muestran algunos comandos **netsh** que se suelen usar con para la red LAN inalámbrica y la red hospedada inalámbrica, aunque se admiten otras combinaciones de comandos:



| Get-Help                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan Start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Inicie la red hospedada inalámbrica.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan STOP hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Detenga la red hospedada inalámbrica.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ Mode = \] permitir no \| permitir**<br/>                                                                                                                                                                                                                                                                      | Habilitar o deshabilitar la red hospedada inalámbrica.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ SSID = \] <ssid> \[ clave = \] <passphrase> \[ keyUsage = \] \| temporal persistente** <br/> | Configure las opciones de red hospedada inalámbrica.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan Refresh hostednetwork \[ Data = \] clave**<br/>                                                                                                                                                                                                                                                                                       | Actualice la clave de red hospedada inalámbrica.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ SETTING = \] Security\]**<br/>                                                                                                                                                                                                                                                                     | Mostrar información de red hospedada inalámbrica.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**configuración de netsh wlan show**<br/>                                                                                                                                                                                                                                                                                                                                                       | Muestra la configuración global de LAN inalámbrica.<br/>           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de redes hospedadas inalámbricas y conexión compartida a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[Ejemplo de red hospedada inalámbrica](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
