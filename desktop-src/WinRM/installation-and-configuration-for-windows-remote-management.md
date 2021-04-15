---
title: 'Instalación y configuración de Administración remota de Windows '
description: Para que se ejecuten los scripts de Administración remota de Windows (WinRM) y para que la herramienta de línea de comandos de **WinRM** realice operaciones de datos, administración remota de Windows (WinRM) debe estar instalado y configurado.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: 4ebe4094984f237a3c8949392e3e9a6b47b8afe6
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "104536405"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Instalación y configuración de Administración remota de Windows

Para que se ejecuten los scripts de Administración remota de Windows (WinRM) y para que la herramienta de línea de comandos de **WinRM** realice operaciones de datos, administración remota de Windows (WinRM) debe estar instalado y configurado.

Estos elementos también dependen de la configuración de WinRM.

- Herramienta de línea de comandos del [Shell remoto de Windows](./windows-remote-management-glossary.md#w) (**Winrs**).
- [Reenvío de eventos](./windows-remote-management-glossary.md#e).
- Comunicación remota de Windows PowerShell 2,0.

## <a name="where-winrm-is-installed"></a>Dónde está instalado WinRM

WinRM se instala automáticamente con todas las versiones admitidas actualmente del sistema operativo Windows.

## <a name="configuration-of-winrm-and-ipmi"></a>Configuración de WinRM e IPMI

Estos componentes de WinRM y de [proveedor de WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) de [interfaz de administración de plataforma inteligente (IPMI)](./windows-remote-management-glossary.md#i) se instalan con el sistema operativo.

- El servicio WinRM se inicia automáticamente en Windows Server 2008 y en las versiones posteriores (en Windows Vista, debe iniciar el servicio manualmente).
- De forma predeterminada, no se configura ningún [agente de escucha](./windows-remote-management-glossary.md#l) de WinRM. Incluso si el servicio WinRM se está ejecutando, no se pueden recibir ni enviar [mensajes](./windows-remote-management-glossary.md#m) de protocolo WS-Management que soliciten datos.
- Firewall de conexión a Internet (ICF) bloquea el acceso a los puertos.

Use el comando **WinRM** para buscar agentes de escucha y las direcciones escribiendo el siguiente comando en un símbolo del sistema.

```console
winrm e winrm/config/listener
```

Para comprobar el estado de las opciones de configuración, escriba el siguiente comando.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Configuración rápida predeterminada

Puede habilitar el protocolo de WS-Management en el equipo local y configurar la configuración predeterminada para la administración remota con el comando `winrm quickconfig` .

El `winrm quickconfig` comando (o la versión abreviada `winrm qc` ) realiza estas operaciones.

- Inicia el servicio WinRM y establece el tipo de inicio del servicio en Inicio automático.
- Configura un agente de escucha para los puertos que envían y reciben [mensajes](./windows-remote-management-glossary.md#m) de protocolo WS-Management mediante http o https en cualquier dirección IP.
- Define las excepciones de ICF para el servicio WinRM y abre los puertos para HTTP y HTTPS.

> [!NOTE]
> El `winrm quickconfig` comando crea una excepción de Firewall solo para el perfil de usuario actual. Si se cambia el perfil de Firewall por cualquier motivo, debe ejecutar `winrm quickconfig` para habilitar la excepción de Firewall para el nuevo perfil; de lo contrario, es posible que la excepción no esté habilitada.

Para recuperar información acerca de la personalización de una configuración, escriba `winrm help config` en un símbolo del sistema.

### <a name="to-configure-winrm-with-default-settings"></a>Para configurar WinRM con la configuración predeterminada

1. Escriba `winrm quickconfig` en un símbolo del sistema.

   Si no se está ejecutando con la cuenta de administrador del equipo local, debe seleccionar **Ejecutar como administrador** en el menú **Inicio** , o bien usar el comando **runas** en un símbolo del sistema.

2. Cuando la herramienta muestre **realizar estos cambios \[ y/n \] ?**, escriba **y**.

   Si la configuración es correcta, se muestra el siguiente resultado.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Mantenga la configuración predeterminada para los componentes de cliente y servidor de WinRM o personalícela. Por ejemplo, puede que necesite agregar algunos equipos remotos a la lista de configuración de cliente TrustedHosts.

   Debe configurar una lista de hosts de confianza cuando no se pueda establecer la autenticación mutua. Kerberos permite la autenticación mutua, pero no se puede usar en dominios solo de grupos de trabajo &mdash; . Un procedimiento recomendado para configurar hosts de confianza para un grupo de trabajo es hacer que la lista esté lo más restringida posible.

4. Cree un agente de escucha HTTPS escribiendo el comando `winrm quickconfig -transport:https` . Tenga en cuenta que debe abrir el puerto 5986 para que el transporte HTTPS funcione.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Configuración predeterminada del Protocolo de escucha y WS-Management

Para obtener la configuración del agente de escucha, escriba `winrm enumerate winrm/config/listener` en un símbolo del sistema. Los agentes de escucha se definen mediante un transporte (HTTP o HTTPS) y una dirección IPv4 o IPv6.

`winrm quickconfig` crea la siguiente configuración predeterminada para un agente de escucha. Puede crear más de un agente de escucha. Para obtener más información, escriba `winrm help config` en un símbolo del sistema.

### <a name="address"></a>Dirección

Especifica la dirección para la que se creó este agente de escucha.

### <a name="transport"></a>Transporte

Especifica el transporte que se va a utilizar para enviar y recibir las solicitudes y las respuestas del protocolo WS-Management. El valor debe ser *http* o *https*. El valor predeterminado es *http*.

### <a name="port"></a>Port

Especifica el puerto TCP para el que se creó este agente de escucha.

**WinRM 2,0:** El puerto HTTP predeterminado es 5985.

### <a name="hostname"></a>Nombre de host

Especifica el nombre de host del equipo en el que se está ejecutando el servicio WinRM. El valor debe ser un nombre de dominio completo, una cadena literal IPv4 o IPv6 o un carácter comodín.

### <a name="enabled"></a>habilitado

Especifica si el agente de escucha está habilitado o deshabilitado. El valor predeterminado es *True*.

### <a name="urlprefix"></a>URLPrefix

Especifica un prefijo de dirección URL en el que se aceptan solicitudes HTTP o HTTPS. Se trata de una cadena que solo contiene los caracteres a-z, A-Z, 9-0, subrayado ( \_ ) y barra diagonal (/). La cadena no debe empezar ni acabar con una barra diagonal (/). Por ejemplo, si el nombre del equipo es SampleMachine, el cliente WinRM especificaría https://SampleMachine/< *URLPrefix*> en la dirección de destino. El prefijo de dirección URL predeterminado es "wsman".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Especifica la huella digital del certificado del servicio. Este valor representa una cadena de valores hexadecimales de dos dígitos que se encuentran en el campo de huella digital del certificado. Esta cadena contiene el hash SHA-1 del certificado. Los certificados se usan para la autenticación basada en certificados de cliente. Los certificados solo se pueden asignar a cuentas de usuario locales y no funcionan con cuentas de dominio.

### <a name="listeningon"></a>ListeningOn

Especifica las direcciones IPv4 e IPv6 que usa el agente de escucha. Por ejemplo: "111.0.0.1, 111.222.333.444,:: 1, 1000:2000:2C: 3: C19:9ec8: a715:5e24, 3ffe: 8311: ffff: f70f: 0:5EFE: 111.222.333.444, fe80:: 5EFE: 111.222.333.444% 8, fe80:: C19:9ec8: a715:5e24% 6".

## <a name="protocol-default-settings"></a>Configuración predeterminada del Protocolo

Muchas de las opciones de configuración, como MaxEnvelopeSizekb o SoapTraceEnabled, determinan el modo en que los componentes de servidor y cliente de WinRM interactúan con el protocolo de WS-Management. En la lista siguiente se describen las opciones de configuración disponibles.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Especifica los datos de Protocolo simple de acceso a objetos (SOAP) en kilobytes. El valor predeterminado es 150 kilobytes.

> [!NOTE]  
> No se admite el comportamiento si MaxEnvelopeSizekb está establecido en un valor mayor que 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Especifica el tiempo de espera máximo, en milisegundos, que se puede usar para cualquier solicitud que no sea de solicitudes de incorporación de cambios. El valor predeterminado es 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Especifica el número máximo de elementos que pueden utilizarse en una respuesta Pull. El valor predeterminado es 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Especifica el número máximo de solicitudes simultáneas permitidas por el servicio. El valor predeterminado es 25.

**WinRM 2,0:** Esta opción está en desuso y está establecida en solo lectura.

## <a name="winrm-client-default-configuration-settings"></a>Opciones de configuración predeterminadas del cliente WinRM

La versión de cliente de WinRM tiene los siguientes valores de configuración predeterminados.

### <a name="networkdelayms"></a>NetworkDelayms

Especifica el tiempo adicional en milisegundos que espera el equipo cliente para adaptarse al tiempo de retraso de la red. El valor predeterminado es 5000 milisegundos.

### <a name="urlprefix"></a>URLPrefix

Especifica un prefijo de dirección URL en el que se aceptan solicitudes HTTP o HTTPS. El prefijo de dirección URL predeterminado es "wsman".

### <a name="allowunencrypted"></a>AllowUnencrypted

Permite que el equipo cliente solicite tráfico sin cifrar. De forma predeterminada, el equipo cliente requiere tráfico de red cifrado y este valor es *false*.

### <a name="basic"></a>Básico

Permite que el equipo cliente utilice la autenticación Básica. La autenticación Básica es un esquema en el que el nombre de usuario y la contraseña se envían al servidor o proxy como texto no cifrado. Este método de autenticación es el menos seguro de todos. El valor predeterminado es *True*.

### <a name="digest"></a>Digest

Permite al cliente utilizar la autenticación Implícita. La autenticación Implícita es un esquema de desafío/respuesta que utiliza una cadena de datos especificada por el servidor para el desafío. Solo el equipo cliente puede iniciar una solicitud de autenticación Implícita. El equipo cliente envía una solicitud al servidor para autenticarse y recibe una cadena de token del servidor. A continuación, el equipo cliente envía la solicitud de recursos, incluido el nombre de usuario y un hash criptográfico de la contraseña combinada con la cadena de token. Se admite la autenticación Implícita para HTTP y HTTPS. Las aplicaciones y scripts de cliente del shell de WinRM pueden especificar la autenticación implícita, pero el servicio WinRM no acepta la autenticación implícita. El valor predeterminado es *True*.

> [!NOTE]
> la autenticación Implícita en HTTP no se considera segura.

### <a name="certificate"></a>Certificado

Permite al cliente utilizar la autenticación basada en certificados de cliente. La autenticación basada en certificados es un esquema en el que el servidor autentica un cliente identificado por un certificado X509. El valor predeterminado es *True*.

### <a name="kerberos"></a>Kerberos

Permite al cliente utilizar la autenticación Kerberos. La autenticación Kerberos es un esquema en el que el cliente y el servidor se autentican mutuamente mediante certificados Kerberos. El valor predeterminado es *True*.

### <a name="negotiate"></a>Negotiate

Permite al cliente utilizar la autenticación Negotiate. La autenticación Negotiate es un esquema en el que el cliente envía una solicitud al servidor para que la autentique. El servidor determina si se utiliza el protocolo Kerberos o NTLM. Se selecciona el protocolo Kerberos para autenticar una cuenta de dominio, y se selecciona NTLM para las cuentas de equipo local. El nombre de usuario debe especificarse en \\ el \_ formato de nombre de usuario de dominio para un usuario de dominio. El nombre de usuario debe especificarse en el \_ formato "nombre de usuario del nombre del servidor \\ \_ " para un usuario local en un equipo servidor. El valor predeterminado es *True*.

### <a name="credssp"></a>CredSSP

Permite al cliente utilizar la autenticación del proveedor de compatibilidad para seguridad de credenciales (CredSSP). CredSSP permite a una aplicación delegar las credenciales del usuario desde el equipo cliente al servidor de destino. El valor predeterminado es *False*.

### <a name="defaultports"></a>DefaultPorts

Especifica los puertos que el cliente usará para HTTP o HTTPS.

**WinRM 2,0:** El puerto HTTP predeterminado es 5985 y el Puerto HTTPS predeterminado es 5986.

### <a name="trustedhosts"></a>TrustedHosts

Especifica la lista de equipos remotos de confianza. En esta lista se deben agregar otros equipos de un grupo de trabajo o equipos de un dominio diferente.

> [!Note]
> Los equipos de la lista TrustedHosts no se autentican. El cliente puede enviar información de credenciales a estos equipos.

Si se especifica una dirección IPv6 para un TrustedHost, la dirección debe ir entre corchetes, tal y como se muestra en el siguiente comando de la utilidad WinRM: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Para obtener más información sobre cómo agregar equipos a la lista TrustedHosts, escriba `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Opciones de configuración predeterminadas del servicio WinRM

La versión del servicio de WinRM tiene los siguientes valores de configuración predeterminados.

### <a name="rootsddl"></a>RootSDDL

Especifica el descriptor de seguridad que controla el acceso remoto al agente de escucha. El valor predeterminado es "O:NSG: BAD: P (A;; GA;;; BA) (A;; GR;;; ER) S:P (AU; FA; GA;;; WD) (AU; SA; GWGX;;; WD) ".

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

Número máximo de operaciones simultáneas. El valor predeterminado es 100.

**WinRM 2,0:** La configuración MaxConcurrentOperations está en desuso y está establecida en solo lectura. Esta configuración se ha reemplazado por propiedades maxconcurrentoperationsperuser.

### <a name="maxconcurrentoperationsperuser"></a>Propiedades maxconcurrentoperationsperuser

Especifica el número máximo de operaciones simultáneas que cualquier usuario puede abrir de forma remota en el mismo sistema. El valor predeterminado es 1500.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Especifica el tiempo de espera de inactividad en milisegundos entre los mensajes de extracción. El valor predeterminado es 60000.

### <a name="maxconnections"></a>MaxConnections

Especifica el número máximo de solicitudes activas que el servicio puede procesar simultáneamente. El valor predeterminado es 300.

**WinRM 2,0:** El valor predeterminado es 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Especifica el período de tiempo máximo, en segundos, que el servicio WinRM tarda en recuperar un paquete. El valor predeterminado es 120 segundos.

### <a name="allowunencrypted"></a>AllowUnencrypted

Permite que el equipo cliente solicite tráfico sin cifrar. El valor predeterminado es *False*.

### <a name="basic"></a>Básico

Permite que el servicio WinRM use la autenticación básica. El valor predeterminado es *False*.

### <a name="certificate"></a>Certificado

Permite que el servicio WinRM use la autenticación basada en certificados de cliente. El valor predeterminado es *False*.

### <a name="kerberos"></a>Kerberos

Permite que el servicio WinRM use la autenticación Kerberos. El valor predeterminado es *True*.

### <a name="negotiate"></a>Negotiate

Permite que el servicio WinRM use la autenticación Negotiate. El valor predeterminado es *True*.

### <a name="credssp"></a>CredSSP

Permite que el servicio WinRM use la autenticación del proveedor de compatibilidad para seguridad de credenciales (CredSSP). El valor predeterminado es *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Establece la directiva para los requisitos de token de enlace de canal en las solicitudes de autenticación. El valor predeterminado es *relajado*.

### <a name="defaultports"></a>DefaultPorts

Especifica los puertos que el servicio WinRM usará para HTTP o HTTPS.

**WinRM 2,0:** El puerto HTTP predeterminado es 5985 y el Puerto HTTPS predeterminado es 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter y IPv6Filter

Especifica las direcciones IPv4 o IPv6 que pueden usar los agentes de escucha. Los valores predeterminados son IPv4Filter = \* y IPv6Filter = \* .

**IPv4:** Una cadena literal IPv4 consta de cuatro números decimales con puntos, cada uno en el intervalo comprendido entre 0 y 255. Por ejemplo: 192.168.0.0.

**IPv6:** Una cadena literal IPv6 se incluye entre corchetes y contiene números hexadecimales separados por dos puntos. Por ejemplo: \[ :: 1 \] o \[ 3ffe: ffff:: 6ECB: 0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Especifica si está habilitada la escucha HTTP de compatibilidad. Si este valor es *true*, el agente de escucha escuchará en el puerto 80 además del puerto 5985. El valor predeterminado es *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Especifica si el agente de escucha HTTPS de compatibilidad está habilitado. Si este valor es *true*, el agente de escucha escuchará en el puerto 443 además del puerto 5986. El valor predeterminado es *False*.

## <a name="winrs-default-configuration-settings"></a>Opciones de configuración predeterminadas de Winrs

`winrm quickconfig` también configura valores predeterminados de **Winrs** .

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Permite el acceso a shells remotos. Si establece este parámetro en *false*, el servidor rechazará las nuevas conexiones de shell remoto. El valor predeterminado es *True*.

### <a name="idletimeout"></a>IdleTimeout

Especifica el tiempo máximo, en milisegundos, que el shell remoto permanecerá abierto cuando no haya ninguna actividad de usuario en el shell remoto. El shell remoto se elimina automáticamente después de que transcurra el tiempo especificado.

**WinRM 2,0:** El valor predeterminado es 180000. El valor mínimo es 60000. El establecimiento de este valor inferior a 60000 no tendrá ningún efecto en el tiempo de espera.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Especifica el número máximo de usuarios que pueden realizar simultáneamente operaciones remotas en el mismo equipo a través de un shell remoto. Se rechazarán las nuevas conexiones de shell remoto si superan el límite especificado. El valor predeterminado es 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Especifica el tiempo máximo, en milisegundos, que puede ejecutarse el comando remoto o el script. El valor predeterminado es 28,8 millones.

**WinRM 2,0:** El valor de MaxShellRunTime se establece en solo lectura. Cambiar el valor de MaxShellRunTime no tendrá ningún efecto en los shells remotos.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Especifica el número máximo de procesos que cualquier operación de shell puede iniciar. Un valor de 0 permite un número ilimitado de procesos. El valor predeterminado es 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Especifica la cantidad máxima de memoria asignada por Shell, incluidos los procesos secundarios del shell. El valor predeterminado es 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Especifica el número máximo de shells simultáneos que puede abrir de forma remota cada usuario en el mismo equipo. Si esta configuración de directiva está habilitada, el usuario no podrá abrir nuevos shells remotos si el recuento supera el límite especificado. Si se deshabilita la configuración de la directiva o no se configura, el límite quedará establecido en 5 shells remotos por usuario de forma predeterminada.

## <a name="configuring-winrm-with-group-policy"></a>Configuración de WinRM con directiva de grupo

Use el editor de directiva de grupo para configurar el shell remoto de Windows y WinRM para los equipos de su empresa.

### <a name="to-configure-with-group-policy"></a>Para configurar con directiva de grupo

1. Abra una ventana de símbolo del sistema como administrador.
2. En el símbolo del sistema, escriba `gpedit.msc` . Se abre la ventana **Editor de objetos de directiva de grupo** .
3. Busque el **administración remota de Windows** y los objetos de directiva de grupo de **Shell remoto de Windows** (GPO) en **configuración del equipo \\ plantillas administrativas componentes de \\ Windows**.
4. En la pestaña **extendido** , seleccione una opción para ver una descripción. Haga doble clic en un valor para editarlo.

## <a name="windows-firewall-and-winrm-20-ports"></a>Puertos de Firewall de Windows y WinRM 2,0

A partir de WinRM 2,0, los puertos de escucha predeterminados configurados por `Winrm quickconfig` son el puerto 5985 para el transporte http y el puerto 5986 para HTTPS. Los agentes de escucha de WinRM se pueden configurar en cualquier puerto arbitrario.

Si un equipo se actualiza a WinRM 2,0, los agentes de escucha configurados previamente se migran y siguen recibiendo tráfico.

## <a name="winrm-installation-and-configuration-notes"></a>Notas sobre la instalación y configuración de WinRM

WinRM no depende de ningún otro servicio, excepto WinHttp. Si el servicio de administración de IIS está instalado en el mismo equipo, es posible que vea mensajes que indican que WinRM no se puede cargar antes de Internet Information Services (IIS). Sin embargo, WinRM no depende realmente de los &mdash; mensajes que se producen porque el orden de carga garantiza que el servicio IIS se inicie antes que el servicio http. WinRM requiere que `WinHTTP.dll` se registre.

Si el cliente de Firewall de ISA2004 está instalado en el equipo, puede hacer que un cliente de servicios web para administración (WS-Management) deje de responder. Para evitar este problema, instale ISA2004 Firewall SP1.

Si dos servicios de escucha con diferentes direcciones IP están configurados con el mismo número de puerto y el mismo nombre de equipo, WinRM escucha o recibe mensajes solo en una dirección. Esto se debe a que los prefijos de dirección URL utilizados por el protocolo WS-Management son los mismos.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Notas de instalación del proveedor y el controlador IPMI

Es posible que el controlador no detecte la existencia de controladores IPMI que no sean de Microsoft. Si el controlador no se inicia, es posible que tenga que deshabilitarlo.

Si los recursos del [controlador de administración de placa base (BMC)](./windows-remote-management-glossary.md#b) aparecen en el BIOS del sistema, ACPI (plug and Play) detecta el hardware de BMC e instala automáticamente el controlador IPMI. Es posible que la compatibilidad con Plug and Play no esté presente en todos los BMC. Si Plug and Play detecta el BMC, aparece un dispositivo desconocido en Administrador de dispositivos antes de instalar el componente de administración de hardware. Cuando se instala el controlador, en Administrador de dispositivos se muestra un nuevo componente, el dispositivo compatible con IPMI genérico de Microsoft ACPI.

Si el sistema no detecta automáticamente el BMC e instala el controlador, pero se detectó un BMC durante el proceso de instalación, debe crear el dispositivo de BMC. Para ello, escriba el siguiente comando en un símbolo del sistema: `Rundll32 ipmisetp.dll, AddTheDevice` . Después de ejecutar este comando, se crea el dispositivo IPMI y aparece en Administrador de dispositivos. Si desinstala el componente de administración de hardware, se quitará el dispositivo.

Para obtener más información, consulte Introducción a la [Administración de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

El proveedor IPMI coloca las clases de hardware en el [espacio de nombres](/windows/desktop/WmiSdk/gloss-n) de **\\ hardware raíz** de WMI. Para obtener más información acerca de las clases de hardware, consulte el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Para obtener más información acerca de los *espacios de nombres* WMI, vea [arquitectura de WMI](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Notas de configuración del complemento WMI

A partir de Windows 8 y Windows Server 2012, los [Complementos WMI](./windows-remote-management-glossary.md#w) tienen sus propias configuraciones de seguridad. Para que un usuario normal o de energía (no administrador) pueda usar el *complemento WMI*, debe habilitar el acceso para ese usuario una vez configurado el [agente de escucha](./windows-remote-management-glossary.md#l) . En primer lugar, debe configurar el usuario para el acceso remoto a [WMI](./windows-remote-management-glossary.md#w) a través de uno de estos pasos.

- Ejecute `lusrmgr.msc` para agregar el usuario al grupo **WinRMRemoteWMIUsers \_ \_** en la ventana **usuarios y grupos locales** , o bien
- Use la herramienta de línea de comandos **WinRM** para configurar el descriptor de seguridad para el [*espacio de nombres*](./windows-remote-management-glossary.md#n) del [complemento WMI](./windows-remote-management-glossary.md#w), como se indica a continuación: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Cuando aparezca la interfaz de usuario, agregue el usuario.

Después de configurar el usuario para el acceso remoto a [WMI](./windows-remote-management-glossary.md#w), debe configurar *WMI* para permitir que el usuario tenga acceso al complemento. Para ello, ejecute `wmimgmt.msc` para modificar la seguridad de *WMI* del espacio de [nombres](./windows-remote-management-glossary.md#n) al que se va a tener acceso en la ventana **control WMI** .

La mayoría de las clases WMI para la administración se encuentran en el espacio de nombres **root \\ cimv2** .