---
description: Acerca de la red hospedada inalámbrica
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Acerca de la red hospedada inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88af34a1e0df2029c230b7b7800130d3b550dbf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882769"
---
# <a name="about-the-wireless-hosted-network"></a>Acerca de la red hospedada inalámbrica

La red hospedada inalámbrica es una nueva característica DE WLAN compatible con Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrico instalado. Esta característica implementa dos funciones principales:

-   La virtualización de un adaptador inalámbrico físico en más de un adaptador inalámbrico virtual a veces se conoce como Wi-Fi virtual.
-   Un punto de acceso inalámbrico (AP) basado en software a veces se conoce como SoftAP que usa un adaptador inalámbrico virtual designado.

Estas dos funciones coexisten en un Windows conjunto. La habilitación o deshabilitación de la red hospedada inalámbrica habilita o deshabilita las Wi-Fi virtuales y SoftAP. No es posible habilitar o deshabilitar estas dos funciones por separado en Windows.

Con esta característica, un equipo Windows puede usar un único adaptador inalámbrico físico para conectarse como cliente a un punto de acceso de hardware (AP), mientras que al mismo tiempo actúa como un AP de software que permite que otros dispositivos con capacidad inalámbrica se conecten a él. Esta característica requiere que se instale un adaptador inalámbrico compatible con red hospedada en el equipo local. El controlador del adaptador inalámbrico debe implementar el modelo de controlador de dispositivo LAN inalámbrico definido por Microsoft para su uso Windows 7. Para recibir el Windows 7, un controlador inalámbrico debe implementar la característica red hospedada inalámbrica.

Hay como máximo una red hospedada inalámbrica habilitada en cualquier momento en el equipo local y solo la red hospedada inalámbrica usará un adaptador inalámbrico. Si hay más de un adaptador inalámbrico compatible con red hospedada, Windows elegirá un adaptador para usarlo con la red hospedada inalámbrica. Cuando se usan las API de red hospedada, el adaptador inalámbrico compatible con red hospedada se virtualiza a como máximo en 3 adaptadores lógicos:

-   Un adaptador de estación (STA) para su uso por parte de aplicaciones inalámbricas ad hoc o de cliente. El adaptador sta hereda toda la configuración del adaptador inalámbrico físico original y presenta los mismos comportamientos que el adaptador físico. Conceptualmente, se puede ver el adaptador sta como idéntico al adaptador físico después de la virtualización. El adaptador STA siempre está en el sistema siempre que el adaptador físico inalámbrico correspondiente esté presente.
-   Un adaptador de AP para que lo use la red hospedada inalámbrica para hospedar SoftAP. El adaptador de AP está presente en el sistema Windows solo después de invocar la red hospedada inalámbrica por primera vez (cuando se llama por primera vez a la función [**WlanHostedNetworkStartUsing,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Una vez creado, el adaptador de AP permanecerá en el sistema hasta que se deshabilite la red hospedada inalámbrica. Si la red hospedada inalámbrica está habilitada en algún momento posterior, el adaptador de AP se mostrará de nuevo en el sistema.
-   Un adaptador de estación virtual (VSTA) para que lo usen los proveedores de hardware para ampliar la funcionalidad de red hospedada inalámbrica en Windows. El adaptador de VSTA es opcional y solo puede crearse en el sistema mediante el servicio IHV correspondiente. A diferencia del adaptador de AP, el adaptador de VSTA solo existe en el sistema Windows desde el momento en que el servicio IHV inicializa el adaptador hasta el momento en que el servicio IHV libera el adaptador.

Virtual Wi-Fi asigna los adaptadores lógicos a los puertos NDIS. El enlace de los adaptadores STA, AP y VSTA a puertos NDIS específicos se decide Windows. El adaptador sta siempre está enlazado al puerto 0. El adaptador de AP se enlaza al siguiente puerto NDIS disponible cuando se inicia la virtualización y el enlace permanece igual hasta que finaliza la virtualización cuando la red hospedada inalámbrica está deshabilitada. El adaptador de VSTA se enlaza al siguiente puerto NDIS disponible cuando lo inicializa el servicio IHV correspondiente y el enlace permanece igual hasta que el servicio IHV lo libera.

Es posible que el adaptador de VSTA se cree para que lo usen los IHV sin crear el adaptador de SoftAP.

Las siguientes combinaciones son válidas para un adaptador físico con virtualización:

-   Adaptador sta.
-   Adaptadores STA y AP.
-   Adaptadores STA y VSTA.
-   Adaptadores STA, AP y VSTA.

Excepto en el caso del adaptador STA, todas las demás combinaciones solo son válidas cuando la red hospedada inalámbrica está habilitada. En cuanto al caso del adaptador STA único, es el adaptador físico si la red hospedada inalámbrica está deshabilitada. Si la red hospedada inalámbrica está habilitada, es el adaptador STA cuando la red hospedada inalámbrica nunca se ha invocado en el sistema.

El protocolo de puente de nivel 2 está prohibido entre el adaptador de AP y cualquier otro adaptador del sistema. La misma restricción se aplica al adaptador de VSTA cuando está presente en el sistema.

La característica red hospedada inalámbrica de Windows implementa un SoftAP. Sin embargo, este SoftAP no está diseñado para reemplazar los dispositivos AP inalámbricos basados en hardware. En concreto, si la red hospedada inalámbrica se está ejecutando cuando el equipo entra en suspensión (en espera), hiberna o antes de que se reinicie el equipo, se detendrán las redes hospedadas inalámbricas. La red hospedada inalámbrica no se reiniciará automáticamente después de que el equipo se reanude de suspensión, hibernación o reinicio. Además, SoftAP no proporciona la resolución DNS. En el caso de que un servidor DNS externo no esté disponible mediante el uso compartido de conexiones a Internet (consulte la explicación de ICS a continuación), la resolución de nombres de dominio completo (FQDN) entre dos equipos o dispositivos conectados a SoftAP, incluido el equipo que hospeda softAP, solo funcionaría si ambas entidades marcan el tipo de red de la red SoftAP como PRIVATE (HOME o WORK en el elemento emergente de la categoría de red). Dado que el equipo que hospeda SoftAP siempre marca el tipo de red SoftAP como PRIVATE, solo los equipos o dispositivos conectados a SoftAP deben marcar el tipo de red SoftAP como PRIVATE para que la resolución de FQDN funcione.

Las redes softAP y ad hoc se excluyen mutuamente en el mismo adaptador físico. Si SoftAP se ejecuta en el adaptador de AP y un usuario o una aplicación inician redes ad hoc en el adaptador sta, SoftAP se apagará. Iif ad hoc networking is running on the STA adapter, an attempt to start SoftAP on the AP adapter will fail.

Para proporcionar protección para las comunicaciones inalámbricas entre el equipo que hospeda SoftAP y los dispositivos que se conectan a SoftAP, la red hospedada inalámbrica requiere que todos los dispositivos conectados usen el conjunto de cifrado WPA2-PSK/AES. La clave compartida es un valor de 63 caracteres generado por Windows cuando se invoca la red hospedada inalámbrica por primera vez (cuando se llama por primera vez a la función [**WlanHostedNetworkStartUsing,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)o [**WlanHostedNetworkInitSettings).**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) Un usuario o aplicación no puede cambiar el valor de esta clave compartida, pero una aplicación puede solicitar al sistema operativo que regenere una nueva clave mediante una llamada a la función [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) o un usuario puede solicitar que el sistema operativo vuelva a generar una nueva clave mediante comandos **netsh wlan.** Esta clave compartida se denomina clave principal o del sistema para la red hospedada inalámbrica y es persistente en el inicio y la detención de la red hospedada inalámbrica. Esta clave principal se denomina "clave de seguridad del sistema" en **los comandos de netsh wlan.**

Para facilitar el uso, la red hospedada inalámbrica también admite el concepto de clave de seguridad secundaria o de usuario más fácil de usar, pero que podría ser menos segura. Esta clave secundaria se denomina "clave de seguridad de usuario" en **los comandos de netsh wlan.** La clave secundaria no la genera Windows. El usuario debe proporcionar el valor de esta clave. Un usuario o aplicación puede establecer o cambiar el valor de clave llamando a la función [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) o mediante los comandos **netsh wlan.** La clave secundaria se puede establecer como persistente o temporal. En el caso de una clave temporal, si la red hospedada inalámbrica ya se está ejecutando, la clave secundaria será válida hasta que se detenga la red hospedada inalámbrica. Para una clave temporal, si la red hospedada inalámbrica no se está ejecutando, solo será válida entre el siguiente inicio y detenerse de la red hospedada inalámbrica.

Hay exactamente una clave principal y, como máximo, una clave secundaria para el hetwork hospedado inalámbrico en cualquier equipo. Cualquier dispositivo aprovisionado mediante Wi-Fi configuración protegida (WPS) recibirá la clave principal. Otros dispositivos configurados manualmente pueden tener cualquiera de las claves. Cada vez que se cambia una clave, cualquier dispositivo con el valor de clave anterior no podrá conectarse a la red hospedada inalámbrica sin volver a aprovisionarse con la nueva clave. Sin embargo, los dispositivos con la otra clave sin cambios seguirán siendo capaces de conectarse a la red hospedada inalámbrica.

Una aplicación puede registrarse para recibir notificaciones de red hospedada inalámbrica, por lo que se enviará una notificación WLAN a la devolución de llamada de la aplicación cuando las propiedades cambien en la red hospedada inalámbrica. Una aplicación se registra para las notificaciones de red hospedada inalámbrica mediante una llamada a [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) con el parámetro *dwNotifSource* establecido para incluir el bit \_ \_ HNWK DE ORIGEN DE NOTIFICACIÓN DE \_ WLAN.

Windows proporciona dos maneras para que los administradores de TI administren la característica red hospedada inalámbrica. En el caso de los equipos que son miembros de un dominio, los administradores pueden usar la directiva de grupo para no permitir la red hospedada inalámbrica. Con **los comandos de netsh wlan,** un administrador puede habilitar o deshabilitar la red hospedada inalámbrica localmente en el equipo.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Escenarios admitidos para la red hospedada inalámbrica

La red hospedada inalámbrica permite dos escenarios principales para Windows equipos:

• La capacidad de proporcionar una red de área personal inalámbrica (PAN inalámbrica) para su uso con otros dispositivos inalámbricos.

• Uso compartido de conexiones de red para su uso por parte de otros equipos y dispositivos.

El PAN inalámbrico es el escenario principal habilitado por la red hospedada inalámbrica por sí mismo. Una vez que se inicia la red hospedada inalámbrica en un equipo, cualquier dispositivo compatible con la tecnología inalámbrica que admita WPA2-PSK/AES podrá conectarse al softAP como si se conectase a una API de hardware normal. Los dispositivos conectados a la red hospedada inalámbrica forman un PAN inalámbrico, donde pueden intercambiar información con el equipo Windows que hospeda softAP, así como entre ellos.

El uso compartido de conexiones de red para su uso por parte de otros equipos y dispositivos requiere el uso compartido de conexión a Internet (ICS). En este escenario, la interfaz pública de ICS es la conexión compartida, mientras que la interfaz privada es el adaptador virtual que hospeda SoftAP. La conexión compartida puede ser una conexión Ethernet, LAN inalámbrica o wan inalámbrica. En el caso de una conexión LAN inalámbrica, la interfaz pública de ICS puede ser de otro adaptador LAN inalámbrico o del adaptador virtual de estación en el mismo adaptador inalámbrico físico que hospeda softAP. El uso más común para el uso compartido de red es compartir una conexión a Internet, donde la red de la interfaz pública de ICS tiene acceso a Internet.

La red hospedada inalámbrica interactúa con Wi-Fi Protected Setup (WPS), otra característica nueva importante de Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrico instalado. La red hospedada inalámbrica y WPS admiten un escenario que aprovisiona un dispositivo compatible con WPS para una API de hardware no compatible con WPS. En este caso, el SoftAP hospedado en Windows se invoca en segundo plano para insertar el perfil de AP de hardware en el dispositivo compatible con WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Acceso de usuarios y aplicaciones a una red hospedada inalámbrica

Los usuarios finales interactúan con la característica red hospedada inalámbrica Windows mediante aplicaciones de terceros o comandos **netsh.** Actualmente no hay ninguna interfaz de usuario nativa para configurar o administrar la red hospedada inalámbrica en Windows 7 o en Windows Server 2008 R2 con el servicio LAN inalámbrico instalado.

Las aplicaciones de terceros y los **comandos netsh** se basan en el uso de las funciones de red hospedada inalámbrica pública. Este conjunto de funciones proporciona un conjunto completo de funcionalidades para administrar la red hospedada inalámbrica en Windows 7 y en Windows Server 2008 R2 con el servicio laN inalámbrica instalado.

A continuación se muestra una lista de las funciones de red hospedada inalámbrica y las acciones comunes desde un punto de vista del usuario final para el que se usaría la función:



| Funciones usadas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Inicie la red hospedada inalámbrica.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Detenga la red hospedada inalámbrica.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configure las opciones de red hospedada inalámbrica (cambie el SSID, cambie la clave secundaria o solicite que se vuelva a generar la clave principal).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) [**WlanHostedNetworkQuerySecondaryKey,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey) [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Consulte la información y la configuración de red hospedada inalámbrica (estado, SSID, clave secundaria, clave principal o una lista de los dispositivos conectados actualmente).<br/> |



 

Los **comandos netsh** están diseñados para su uso por usuarios o administradores avanzados.

*Netsh.exe* tiene muchos subcomandos para la LAN inalámbrica. En el símbolo del sistema hay disponible una lista completa de opciones para **netsh** y la LAN inalámbrica; para ello, escriba lo siguiente:

**netsh wlan /?**

La documentación sobre todos los comandos de Netsh para la LAN inalámbrica también está disponible en línea en Technet. Para más información, consulte Comandos netsh para red inalámbrica [de área local (WLAN).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

Los siguientes son algunos comandos **netsh** que se usan normalmente con para la LAN inalámbrica y la red hospedada inalámbrica, aunque se admiten otras combinaciones de comandos:



| Get-Help                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Inicie la red hospedada inalámbrica.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Detenga la red hospedada inalámbrica.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode= \] allow \| disallow**<br/>                                                                                                                                                                                                                                                                      | Habilite o deshabilite la red hospedada inalámbrica.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid= \] &lt; ssid &gt; \[ key= \] &lt; passphrase &gt; \[ keyUsage= \] persistent \| temporary** <br/> | Configure los valores de red hospedada inalámbrica.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan refresh hostednetwork \[ data= \] key**<br/>                                                                                                                                                                                                                                                                                       | Actualice la clave de red hospedada inalámbrica.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ setting= \] security\]**<br/>                                                                                                                                                                                                                                                                     | Mostrar información de red hospedada inalámbrica.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Muestra la configuración global de LAN inalámbrica.<br/>           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de redes hospedadas inalámbricas y uso compartido de conexiones a Internet](using-hosted-network-and-internet-connection-sharing.md)
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

 

 
