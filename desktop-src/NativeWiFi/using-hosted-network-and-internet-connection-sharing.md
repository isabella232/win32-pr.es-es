---
title: Uso de redes hospedadas inalámbricas, uso compartido de conexiones a Internet
description: Uso de redes hospedadas inalámbricas y uso compartido de conexiones a Internet
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972774e921199e32eb70841c74c7478e2178cda9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260543"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>Uso de redes hospedadas inalámbricas, uso compartido de conexiones a Internet

La red hospedada inalámbrica es una nueva característica de WLAN compatible con Windows 7 y Windows 8. También se admite en Windows Server 2012 y Windows Server 2008 R2 con el servicio laN inalámbrica instalado. Esta característica implementa dos funciones principales:

-   La virtualización de un adaptador inalámbrico físico en más de un adaptador inalámbrico virtual a veces se conoce como Wi-Fi virtual.
-   Un punto de acceso inalámbrico (AP) basado en software a veces se conoce como SoftAP que usa un adaptador inalámbrico virtual designado.

El uso compartido de conexiones a Internet (ICS) es una característica de Windows a través del servicio SharedAccess. En términos estrictos, SharedAccess permite el uso compartido de red a través de un equipo en el que el acceso de red compartido no proporciona necesariamente acceso a Internet. En esta sección se usa indistintamente el término ICS y SharedAccess, ya que el uso compartido de conexiones a Internet es un escenario importante para la red hospedada inalámbrica y la comunidad de usuarios conoce mejor el término ICS.

La red hospedada inalámbrica está estrechamente vinculada a ICS para habilitar la red de área personal inalámbrica (PAN) y los escenarios de uso compartido de Internet. En esta sección se proporcionan recomendaciones generales a los desarrolladores de aplicaciones sobre cómo integrar la red hospedada inalámbrica y el ICS mediante la red pública inalámbrica hospedada y las API de ICS.

## <a name="internet-connection-sharing"></a>Conexión compartida a Internet

El servicio ICS funciona en uno de los dos modos posibles:

-   Modo independiente

    Solo la función de servidor DHCPv4 funciona cuando se invoca el servicio ICS. Se trata de un modo de operación especial para ICS y solo está disponible a través de la red hospedada inalámbrica. Un usuario o aplicación no puede iniciar ni detener ics independiente directamente a través de las API de ICS públicas o los **comandos netsh.** Iniciar la red hospedada inalámbrica normalmente implica iniciar ICS en modo independiente para usar la función de servidor DHCPv4 para proporcionar direcciones IPv4 privadas para dispositivos conectados. La comunicación de red para los dispositivos conectados se limita al envío y recepción de paquetes de red entre un dispositivo conectado y el equipo local que hospeda la red hospedada inalámbrica y entre los propios dispositivos conectados. Esto habilita de forma eficaz el escenario de red de área personal inalámbrica para la red hospedada inalámbrica.

-   Modo completo

    Todas las características de ICS funcionan cuando se invoca el servicio, como la traducción de direcciones de red y las funciones del servidor DHCP para IPv4 e IPv6. Este es el modo normal de funcionamiento de ICS. Un usuario o aplicación puede iniciar y detener el modo ICS completo a través de API públicas o comandos de NetShell. Por ejemplo, este servicio se puede detener mediante net stop sharedaccess desde un símbolo del sistema con privilegios elevados. La combinación de red hospedada inalámbrica con ICS completo, la comunicación de red para los dispositivos conectados no se limita al PAN inalámbrico. Cualquier dispositivo conectado tiene acceso a la red (como Internet) a través de la conexión de red compartida desde el equipo que ejecuta la red hospedada inalámbrica. Esto habilita de forma eficaz el escenario de uso compartido de red para la red hospedada inalámbrica.

En esta sección, usamos el término ICS completo para significar el caso en el que se invocan todas las funciones de ICS en el servicio ICS para proporcionar acceso a todas las características de ICS completa con la red hospedada inalámbrica.

Los dos modos de operación de ICS son mutuamente excluyentes y el ICS completo tiene mayor prioridad. El servicio ICS puede pasar del modo independiente al modo completo, pero no del modo completo al modo independiente. El modo independiente de ICS se introdujo en Windows 7 y en Windows Server 2008 R2 con el servicio LAN inalámbrico instalado junto con la característica red hospedada inalámbrica. No está disponible en versiones anteriores de Windows.

Cualquier operación de ICS completa implica dos adaptadores de red diferentes en el sistema:

-   Interfaz pública. Se trata de la interfaz de red con acceso a Internet. Es esta interfaz que el equipo local que ejecuta ICS usa para compartir Internet con clientes y dispositivos que se conectan a ella a través de SoftAP.
-   Interfaz privada. Esta es la interfaz de red que usan otros dispositivos para conectarse al equipo local que ejecuta ICS. Un servidor DHCPv4 se ejecuta en esta interfaz privada para proporcionar direcciones IP locales privadas a los demás equipos remotos.

Cuando la interfaz pública no tiene acceso a Internet, el servidor DHCP de la interfaz privada sigue proporcionando direcciones IP locales a los dispositivos conectados. ICS independiente solo implica la interfaz privada en la que se ejecuta SoftAP; no implica ninguna interfaz pública.

En cualquier momento, hay como máximo una instancia de ICS completa que se ejecuta en el equipo local. Si el ICS completo ya se está ejecutando en el equipo local, al iniciar otro ICS completo se muestran los siguientes comportamientos funcionales:

-   Si las interfaces públicas y privadas del nuevo ICS completo son las mismas que las del ICS completo existente, iniciar el segundo ICS completo equivale a una operación sin operación.
-   Si la nueva interfaz pública es diferente de la interfaz pública anterior, pero la nueva interfaz privada es la misma que la interfaz privada anterior, iniciar un segundo ICS completo tiene poco impacto en los dispositivos conectados en la misma interfaz privada. La capacidad de acceder a Internet puede cambiar con la nueva interfaz pública.
-   Si la nueva interfaz privada es diferente de la interfaz privada anterior, las funciones de ICS dejarán de funcionar en la interfaz privada anterior y comenzarán a aplicarse a la nueva interfaz privada. Cualquier dispositivo remoto que se conecte al equipo local mediante la interfaz privada anterior perderá la conectividad IP con el equipo local.

Cuando el ICS completo ya se está ejecutando, invocar un segundo ICS completo es perjudicial para los dispositivos conectados de forma remota mediante la interfaz privada antigua, siempre y cuando la segunda integración de ICS use una nueva interfaz privada diferente.

Para administrar y usar el servicio ICS para admitir la integración de ICS con red hospedada inalámbrica, una aplicación de software debe obtener primero una [**interfaz INetSharingManager.**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) La **interfaz INetSharingManager** proporciona acceso directa o indirectamente a todas las demás interfaces COM de la API de ICS. El [**método \_ get SharingInstalled de**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled) la interfaz **INetSharingManager** informa de si el equipo local admite el uso compartido de conexiones. El [**método get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) de la interfaz **INetSharingManager** recupera una interfaz de enumeración para todas las conexiones de la carpeta connections. El [**método get \_ INetSharingConfigurationForINetConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection) recupera una [**interfaz INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) para la conexión especificada. Los métodos de **la interfaz INetSharingConfiguration** se pueden usar para consultar y cambiar la configuración de ICS.

La red hospedada inalámbrica debe iniciarse antes de llamar al método [**get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) en la interfaz [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) para enumerar todas las conexiones de la carpeta connections.

Para obtener información sobre ICS y las interfaces y métodos públicos que se pueden usar para consultar y cambiar la configuración de ICS, consulte la documentación sobre el uso compartido de conexiones a Internet y el firewall de conexión [a Internet.](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall)

## <a name="hosted-network-and-ics-integration"></a>Integración de ICS y red hospedada

Cuando el ICS completo no se está ejecutando, el inicio de una red hospedada inalámbrica también inicia internamente el servicio ICS en modo independiente con solo la función de servidor DHCPv4 para asignar direcciones IP para los dispositivos conectados en la interfaz de red hospedada inalámbrica. El intervalo de direcciones de subred para el servidor DHCPv4 independiente es 192.168.173.0/24. Esto es diferente del intervalo de subred de 192.168.137.0/24 que se usa con ICS completo.

El inicio de una red hospedada inalámbrica con ICS completo emplea la siguiente lógica:

-   Si el ICS completo aún no se está ejecutando, el inicio de una red hospedada inalámbrica también inicia el servicio ICS con el servidor DHCPv4 independiente.
-   Si el ICS completo ya se está ejecutando y la interfaz privada es la interfaz de red hospedada inalámbrica, simplemente inicie la red hospedada inalámbrica.
-   Si el ICS completo ya se está ejecutando pero la interfaz privada no es la interfaz de red hospedada inalámbrica, la red hospedada inalámbrica se inicia sin la función de servidor DHCPv4 en la interfaz de red hospedada inalámbrica.

El impacto de la lógica anterior resalta los siguientes hechos:

-   ICS no realiza la transición del modo completo al modo independiente.
-   El modo independiente solo se puede invocar mediante la red hospedada inalámbrica cuando ICS no se ejecuta en modo completo.
-   Si ICS se ejecuta en modo independiente, se adelantará al modo completo si un usuario o una aplicación inicia ICS en modo completo.
-   La transición del modo independiente al modo completo en ICS será perjudicial para los dispositivos conectados en el PAN inalámbrico si la interfaz privada del ICS completo no es la misma que la de SoftAP.

Se tarda tiempo en iniciar o detener el servicio ICS en el equipo local en modo completo o independiente. Una aplicación debe comprobar el estado del servicio ICS mediante la función **NotifyServiceStatusChange** para asegurarse de que el servicio ICS no está en el estado pendiente de inicio o detención antes de iniciar o detener la red hospedada inalámbrica para su uso con la integración de ICS.

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>Inicio y detención de la red hospedada inalámbrica

Windows proporciona una plataforma en la que más de una aplicación simultánea puede administrar una red hospedada inalámbrica al mismo tiempo. Específicamente, cada aplicación puede iniciar y detener la red hospedada inalámbrica por sí misma, sin tener conocimientos previos sobre otras aplicaciones.

Hay dos conjuntos de funciones para iniciar y detener una red hospedada.

Varias aplicaciones pueden requerir el uso de la red hospedada inalámbrica. Las [**funciones WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) y [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) inician y detienen un host Entrada de red una manera compatible con otras aplicaciones simultáneas. Las **funciones WlanHostedNetworkStartUsing** y **WlanHostedNetworkStopUsing** permiten a una aplicación tener una referencia a la red hospedada inalámbrica. Este mecanismo mantiene la red hospedada inalámbrica en ejecución siempre que al menos otra aplicación tenga una referencia actual a la red hospedada inalámbrica. Cualquier usuario puede llamar a estas funciones. Las llamadas correctas **a WlanHostedNetworkStartUsing** deben coincidir con las llamadas a la **función WlanHostedNetworkStopUsing.** Cualquier cambio de estado de red hospedada causado por la función **WlanHostedNetworkStartUsing** se deshacería automáticamente si la aplicación que realiza la llamada cierra su identificador de llamada (llamando a [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) con el mismo parámetro *hClientHandle* pasado a **WlanHostedNetworkStartUsing)** o si finaliza el proceso.

Las [**funciones WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) y [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) obligan a iniciar y detener una red hospedada inalámbrica. Solo se puede llamar a estas funciones si el usuario tiene el privilegio elevado adecuado. Las llamadas correctas a **WlanHostedNetworkForceStart** pueden coincidir con una llamada a la función **WlanHostedNetworkForceStop,** según el diseño de la aplicación. Estas funciones transiciónn el estado de red hospedada inalámbrica sin asociar la solicitud con el identificador de llamada de la aplicación. Cualquier cambio de estado de red hospedada causado por la función **WlanHostedNetworkForceStart** no se deshacería automáticamente si la aplicación que realiza la llamada cierra su identificador de llamada (llamando a [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) con el mismo parámetro *hClientHandle* pasado a [**WlanHostedNetworkStartUsing)**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)o si finaliza el proceso. Si la aplicación que llamó a la función **WlanHostedNetworkForceStart** se cierra sin llamar a una de las funciones para detener la red hospedada inalámbrica, la red hospedada se deja en ejecución. Una aplicación podría llamar a la función **WlanHostedNetworkForceStart** después de asegurarse de que un usuario del sistema con privilegios elevados acepta los mayores requisitos de energía implicados en la ejecución de la red hospedada inalámbrica durante largos períodos de tiempo.

Las recomendaciones generales sobre las funciones a las que se debe llamar para iniciar y detener una red hospedada inalámbrica son las siguientes:

-   Use las [**funciones WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) y [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) dentro de una aplicación para iniciar y detener una red hospedada inalámbrica.
-   No use la función [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para iniciar una red hospedada inalámbrica a menos que sea absolutamente necesaria para la aplicación. La **función WlanHostedNetworkForceStart** también requiere privilegios elevados.
-   Use solo la [**función WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) como método de recuperación. La **función WlanHostedNetworkForceStop** hace que una red hospedada inalámbrica se detenga inmediatamente. Es posible que otras aplicaciones que escuchan notificaciones de red hospedada inalámbrica deban realizar acciones de recuperación. Para obtener más información, consulte la explicación siguiente sobre la secuencia de recuperación de red hospedada inalámbrica.

## <a name="start-sequence-for-wireless-hosted-network"></a>Secuencia de inicio de red hospedada inalámbrica

En el caso de una aplicación que inicia una red hospedada inalámbrica con ICS completo, la recomendación es iniciar la red hospedada inalámbrica y, a continuación, iniciar el ICS completo. Si ya se está ejecutando una red hospedada inalámbrica, una aplicación debe usar la función [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para detener la red hospedada inalámbrica solo si se requiere ICS completo, pero no se ha habilitado antes de que se iniciara la red hospedada. Esto permitirá que otras aplicaciones se recuperen de posibles interrupciones causadas por el inicio del ICS completo. Para obtener más información, consulte la explicación siguiente sobre la secuencia de recuperación de red hospedada inalámbrica. La operación combinada debe ser correcta y producir un error en su conjunto.

> [!Note]  
> La red hospedada inalámbrica debe iniciarse antes de intentar enumerar el adaptador correspondiente mediante la [**interfaz IEnumNetSharingEveryConnection.**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection)

 

Los siguientes pasos ordenados son la secuencia de inicio recomendada en una aplicación que usa red hospedada inalámbrica con ICS completo:

-   Llame a [**la función WlanHostedNetworkInitSettings para**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) asegurarse de que la red hospedada inalámbrica está configurada y lista para usarse.
-   Llame a [**las funciones WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) y [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) para determinar si la red hospedada inalámbrica está permitida y disponible. Si la red hospedada inalámbrica no está permitida y no está disponible, devuelva un error.
-   Pruebe para ver si se permite el servicio ICS usado para el ICS completo. Si no se puede iniciar el servicio ICS, devuelva un error.
-   Llame a [**la función WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para forzar una detenerse de la red hospedada inalámbrica.
-   Llame a [**la función WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) para iniciar la red hospedada inalámbrica.
-   Si la red hospedada inalámbrica no se inicia, devuelve un error.
-   Si el ICS completo ya se está ejecutando y la interfaz pública o privada actual es diferente de la nueva interfaz que se va a usar, almacenar en caché las interfaces públicas y privadas actuales. Una aplicación también puede optar por devolver un error o preguntar al usuario si la integración de ICS ya se está ejecutando.
-   Inicie el ICS completo con la nueva configuración para las interfaces públicas y privadas.
-   Si el ICS completo no se puede iniciar con esta configuración, intente iniciar el servicio ICS completo con las interfaces públicas y privadas almacenadas en caché si el ICS completo se estaba ejecutando antes. Llame a [**la función WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para detener la red hospedada inalámbrica y devolver un error.
-   Devuelve correctamente que la red hospedada inalámbrica y el ICS completo se completan correctamente.

## <a name="stop-sequence-for-wireless-hosted-network"></a>Secuencia de detenerse para la red hospedada inalámbrica

Cuando se usa una red hospedada inalámbrica con ICS completo, una aplicación que ha finalizado su trabajo puede querer detener la red hospedada inalámbrica y el servicio ICS usado para el ICS completo. En este caso, se recomienda llamar a la función [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para detener la red hospedada en lugar de llamar a la [**función WlanHostedNetworkStopUsing.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) La **función WlanHostedNetworkForceStop** detiene la red hospedada inalámbrica y también sirve para permitir que otras aplicaciones se recuperen. Para obtener más información, consulte la explicación siguiente sobre la secuencia de recuperación de red hospedada inalámbrica.

Los siguientes pasos ordenados son la secuencia de detención recomendada en una aplicación que usa red hospedada inalámbrica e ICS completo:

-   Detenga el ICS completo.
-   Llame a [**la función WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para detener la red hospedada inalámbrica.

Una aplicación que usa una red hospedada inalámbrica sin ICS completa que termina con su trabajo solo necesita llamar a la función [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) o [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) para detener la red hospedada inalámbrica. Si se llamó a la función [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) para iniciar la red hospedada inalámbrica, la aplicación debe llamar a la función **WlanHostedNetworkStopUsing** para detener la red hospedada inalámbrica. Si la red hospedada inalámbrica ya se inició antes de la aplicación o la aplicación llamó a la función [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para forzar el inicio de la red hospedada inalámbrica, la aplicación puede llamar a la función **WlanHostedNetworkForceStop** para detener la red hospedada inalámbrica o no hacer nada (dejar la red hospedada inalámbrica iniciada) en función del escenario.

## <a name="recovery-sequence-for-wireless-hosted-network"></a>Secuencia de recuperación para red hospedada inalámbrica

Una aplicación que usa la red hospedada inalámbrica puede verse afectada por las acciones de otras aplicaciones. El servicio ICS y las interfaces para administrar ICS no proporcionan ningún método para que una aplicación se registre para recibir notificaciones de cambio de ICS. Si otra aplicación llama a los [**métodos EnableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing) o [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing) en la interfaz [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) para habilitar o deshabilitar el uso compartido en una conexión, se envía un mensaje a la interfaz de usuario (la pantalla) del equipo local, no a otras aplicaciones. Por lo tanto, una aplicación debe basarse en las notificaciones de red hospedada inalámbricas para realizar acciones de recuperación cuando se producen cambios en ics o red hospedada inalámbrica.

Una aplicación que use la red hospedada inalámbrica debe registrarse para recibir notificaciones de red hospedada inalámbrica mediante una llamada a [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification). Si solo se necesitan notificaciones de red hospedada inalámbrica, la aplicación debe pasar **\_ \_ \_ HNWK DE** ORIGEN DE NOTIFICACIÓN WLAN en el parámetro *dwNotifSource* pasado a **WlanRegisterNotification**. Si también se necesitan otras noticaciones inalámbricas, **wlan \_ notification source \_ \_ HNWK** debe combinarse con las constantes de origen de notificación para otros tipos de notificaciones inalámbricas deseadas y pasar este valor en el *parámetro dwNotifSource.*

La secuencia de recuperación es la misma para las aplicaciones con o sin ICS completo, suponiendo que las aplicaciones no quieran volver a iniciar el servicio ICS. Al recibir una notificación de red hospedada inalámbrica de que la red hospedada se ha detenido, haga lo siguiente:

-   Si la aplicación llamó [**a WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) para iniciar la red hospedada inalámbrica, reinicie la red hospedada mediante una llamada **a WlanHostedNetworkForceStart.** De lo contrario, [**llame a WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) para reiniciar la red hospedada inalámbrica.

## <a name="recovery-sequence-for-connected-devices"></a>Secuencia de recuperación para dispositivos conectados

Los dispositivos remotos o los equipos conectados a la red hospedada inalámbrica pueden verse afectados por las acciones de otras aplicaciones que afectan a ICS y a la red hospedada inalámbrica. Afortunadamente, la mayoría de los dispositivos tienen una lógica de reintento integrada en la aplicación de dispositivo para tratar con una pérdida temporal de señal o itinerancia.

A continuación se muestra una posible secuencia de recuperación para dispositivos o equipos conectados a la red hospedada inalámbrica que pierden contacto:

-   El controlador de dispositivo inalámbrico indica una desconexión de medios a las capas superiores de la pila de red del dispositivo.
-   La aplicación de dispositivo inicia comprobaciones periódicas para la disponibilidad de la red hospedada inalámbrica.
-   Una vez que la aplicación de dispositivo detecta de nuevo la red hospedada inalámbrica, el dispositivo inicia una conexión inalámbrica.
-   Tras una conexión correcta con la red hospedada inalámbrica, la aplicación de dispositivo actualiza su configuración de IP en consecuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la red hospedada inalámbrica](about-the-wireless-hosted-network.md)
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

 

 
