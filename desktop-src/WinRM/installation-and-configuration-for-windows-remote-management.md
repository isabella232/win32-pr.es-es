---
title: 'Instalación y configuración de Administración remota de Windows '
description: Para Windows scripts de administración remota (WinRM) y para que la herramienta de línea de comandos de **Winrm** realice operaciones de datos, Windows Remote Management (WinRM) debe instalarse y configurarse.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: c031ad9b9d9c888385527c227b102c64bb4dfb65eaea340e52eac3fb9595e591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997625"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Instalación y configuración de Windows administración remota

Para Windows scripts de administración remota (WinRM) y para que la herramienta de línea de comandos de **Winrm** realice operaciones de datos, Windows Remote Management (WinRM) debe instalarse y configurarse.

Estos elementos también dependen de la configuración de WinRM.

- La [Windows línea de comandos](./windows-remote-management-glossary.md#w) de Remote Shell **(Winrs).**
- [Reenvío de eventos](./windows-remote-management-glossary.md#e).
- Windows PowerShell comunicación remota 2.0.

## <a name="where-winrm-is-installed"></a>Dónde está instalado WinRM

WinRM se instala automáticamente con todas las versiones admitidas actualmente del Windows operativo.

## <a name="configuration-of-winrm-and-ipmi"></a>Configuración de WinRM e IPMI

Estos componentes de proveedor [WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) de WinRM y [Intelligent Platform Management Interface (IPMI)](./windows-remote-management-glossary.md#i) se instalan con el sistema operativo.

- El servicio WinRM se inicia automáticamente en Windows Server 2008 y en los distritos (en Windows Vista, debe iniciar el servicio manualmente).
- De forma predeterminada, no se configura ningún agente de [escucha](./windows-remote-management-glossary.md#l) de WinRM. Incluso si el servicio WinRM se está ejecutando, WS-Management [mensajes](./windows-remote-management-glossary.md#m) de protocolo que solicitan datos no se pueden recibir ni enviar.
- El Firewall de conexiones a Internet (ICF) bloquea el acceso a los puertos.

Use el **comando Winrm** para buscar agentes de escucha y las direcciones escribiendo el siguiente comando en un símbolo del sistema.

```console
winrm e winrm/config/listener
```

Para comprobar el estado de las opciones de configuración, escriba el siguiente comando.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Configuración predeterminada rápida

Puede habilitar el protocolo WS-Management en el equipo local y configurar la configuración predeterminada para la administración remota con el comando `winrm quickconfig` .

El `winrm quickconfig` comando (o la versión abreviada) `winrm qc` realiza estas operaciones.

- Inicia el servicio WinRM y establece el tipo de inicio del servicio en inicio automático.
- Configura un agente de escucha para los puertos que envían y reciben WS-Management [de](./windows-remote-management-glossary.md#m) protocolo mediante HTTP o HTTPS en cualquier dirección IP.
- Define excepciones ICF para el servicio WinRM y abre los puertos para HTTP y HTTPS.

> [!NOTE]
> El `winrm quickconfig` comando crea una excepción de firewall solo para el perfil de usuario actual. Si se cambia el perfil de firewall por cualquier motivo, debe ejecutar para habilitar la excepción de firewall para el nuevo perfil; de lo contrario, es posible que la excepción `winrm quickconfig` no esté habilitada.

Para recuperar información sobre cómo personalizar una configuración, escriba `winrm help config` en un símbolo del sistema.

### <a name="to-configure-winrm-with-default-settings"></a>Para configurar WinRM con la configuración predeterminada

1. Escriba `winrm quickconfig` en un símbolo del sistema.

   Si no se ejecuta en la cuenta de administrador  del equipo local, debe seleccionar Ejecutar como administrador en el menú Inicio o usar el comando **Runas** en un símbolo del sistema. 

2. Cuando la herramienta muestra **Realizar estos cambios \[ y/n \] ?**, escriba **y**.

   Si la configuración es correcta, se muestra la siguiente salida.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Mantenga la configuración predeterminada para los componentes de cliente y servidor de WinRM, o personalízalos. Por ejemplo, es posible que tenga que agregar determinados equipos remotos a la lista TrustedHosts de configuración de cliente.

   Debe configurar una lista de hosts de confianza cuando no se pueda establecer la autenticación mutua. Kerberos permite la autenticación mutua, pero no se puede usar solo en dominios de &mdash; grupos de trabajo. Un procedimiento recomendado al configurar hosts de confianza para un grupo de trabajo es hacer que la lista esté lo más restringida posible.

4. Cree un agente de escucha HTTPS escribiendo el comando `winrm quickconfig -transport:https` . Tenga en cuenta que debe abrir el puerto 5986 para que el transporte HTTPS funcione.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Configuración predeterminada del agente WS-Management agente de escucha y el protocolo de escucha

Para obtener la configuración del agente de escucha, escriba `winrm enumerate winrm/config/listener` en un símbolo del sistema. Los agentes de escucha se definen mediante un transporte (HTTP o HTTPS) y una dirección IPv4 o IPv6.

`winrm quickconfig` crea la siguiente configuración predeterminada para un agente de escucha. Puede crear más de un agente de escucha. Para obtener más información, escriba `winrm help config` en un símbolo del sistema.

### <a name="address"></a>Dirección

Especifica la dirección para la que se creó este agente de escucha.

### <a name="transport"></a>Transporte

Especifica el transporte que se va a utilizar para enviar y recibir las solicitudes y las respuestas del protocolo WS-Management. El valor debe ser *HTTP* o *HTTPS.* El valor predeterminado es *HTTP.*

### <a name="port"></a>Port

Especifica el puerto TCP para el que se creó este agente de escucha.

**WinRM 2.0:** El puerto HTTP predeterminado es 5985.

### <a name="hostname"></a>Nombre de host

Especifica el nombre de host del equipo en el que se ejecuta el servicio WinRM. El valor debe ser un nombre de dominio completo, una cadena literal IPv4 o IPv6, o un carácter comodín.

### <a name="enabled"></a>habilitado

Especifica si el agente de escucha está habilitado o deshabilitado. El valor predeterminado es *True*.

### <a name="urlprefix"></a>URLPrefix

Especifica un prefijo de dirección URL en el que se aceptan solicitudes HTTP o HTTPS. Se trata de una cadena que contiene solo los caracteres a-z, A-Z, 9-0, subrayado ( \_ ) y barra diagonal (/). La cadena no debe comenzar con ni terminar con una barra diagonal (/). Por ejemplo, si el nombre del equipo es SampleMachine, el cliente winRM especificaría https://SampleMachine/< *URLPrefix*> en la dirección de destino. El prefijo de dirección URL predeterminado es "wsman".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Especifica la huella digital del certificado del servicio. Este valor representa una cadena de valores hexadecimales de dos dígitos que se encuentran en el campo Huella digital del certificado. Esta cadena contiene el hash SHA-1 del certificado. Los certificados se usan para la autenticación basada en certificados de cliente. Los certificados solo se pueden asignar a cuentas de usuario locales y no funcionan con cuentas de dominio.

### <a name="listeningon"></a>ListeningOn

Especifica las direcciones IPv4 e IPv6 que usa el agente de escucha. Por ejemplo: "111.0.0.1, 111.222.333.444, ::1, 1000:2000:2c:3:c19:9ec8:a715:5e24, 3ffe:8311:ffff:f70f:0:5efe:111.222.333.444, fe80::5efe:111.222.333.444%8, fe80::c19:9ec8:a715:5e24%6".

## <a name="protocol-default-settings"></a>Configuración predeterminada del protocolo

Muchas de las opciones de configuración, como MaxEnvelopeSizekb o SoapTraceEnabled, determinan cómo interactúan los componentes de cliente y servidor de WinRM con WS-Management protocolo. En la lista siguiente se describen las opciones de configuración disponibles.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Especifica el número máximo de datos de Protocolo de acceso a objetos simple (SOAP) en kilobytes. El valor predeterminado es 150 kilobytes.

> [!NOTE]  
> No se admite el comportamiento si MaxEnvelopeSizekb está establecido en un valor mayor que 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Especifica el tiempo de espera máximo, en milisegundos, que se puede usar para cualquier solicitud que no sea solicitudes de extracción. El valor predeterminado es 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Especifica el número máximo de elementos que pueden utilizarse en una respuesta Pull. El valor predeterminado es 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Especifica el número máximo de solicitudes simultáneas permitidas por el servicio. El valor predeterminado es 25.

**WinRM 2.0:** Esta configuración está en desuso y se establece en de solo lectura.

## <a name="winrm-client-default-configuration-settings"></a>Opciones de configuración predeterminadas del cliente WinRM

La versión de cliente de WinRM tiene los siguientes valores de configuración predeterminados.

### <a name="networkdelayms"></a>NetworkDelayms

Especifica el tiempo adicional en milisegundos que espera el equipo cliente para adaptarse al tiempo de retraso de la red. El valor predeterminado es 5000 milisegundos.

### <a name="urlprefix"></a>URLPrefix

Especifica un prefijo de dirección URL en el que se aceptan solicitudes HTTP o HTTPS. El prefijo de dirección URL predeterminado es "wsman".

### <a name="allowunencrypted"></a>AllowUnencrypted

Permite que el equipo cliente solicite tráfico sin cifrar. De forma predeterminada, el equipo cliente requiere tráfico de red cifrado y esta configuración es *False.*

### <a name="basic"></a>Básico

Permite que el equipo cliente utilice la autenticación Básica. La autenticación Básica es un esquema en el que el nombre de usuario y la contraseña se envían al servidor o proxy como texto no cifrado. Este método de autenticación es el menos seguro de todos. El valor predeterminado es *True*.

### <a name="digest"></a>Digest

Permite al cliente utilizar la autenticación Implícita. La autenticación Implícita es un esquema de desafío/respuesta que utiliza una cadena de datos especificada por el servidor para el desafío. Solo el equipo cliente puede iniciar una solicitud de autenticación Implícita. El equipo cliente envía una solicitud al servidor para autenticarse y recibe una cadena de token del servidor. A continuación, el equipo cliente envía la solicitud de recurso, incluido el nombre de usuario y un hash criptográfico de la contraseña combinados con la cadena de token. Se admite la autenticación Implícita para HTTP y HTTPS. Las aplicaciones y scripts de cliente de WinRM Shell pueden especificar la autenticación implícita, pero el servicio WinRM no acepta la autenticación implícita. El valor predeterminado es *True*.

> [!NOTE]
> la autenticación Implícita en HTTP no se considera segura.

### <a name="certificate"></a>Certificado

Permite al cliente usar la autenticación basada en certificados de cliente. La autenticación basada en certificados es un esquema en el que el servidor autentica un cliente identificado por un certificado X509. El valor predeterminado es *True*.

### <a name="kerberos"></a>Kerberos

Permite al cliente utilizar la autenticación Kerberos. La autenticación Kerberos es un esquema en el que el cliente y el servidor se autentican mutuamente mediante certificados Kerberos. El valor predeterminado es *True*.

### <a name="negotiate"></a>Negotiate

Permite al cliente utilizar la autenticación Negotiate. La autenticación Negotiate es un esquema en el que el cliente envía una solicitud al servidor para que la autentique. El servidor determina si se utiliza el protocolo Kerberos o NTLM. Se selecciona el protocolo Kerberos para autenticar una cuenta de dominio, y se selecciona NTLM para las cuentas de equipo local. El nombre de usuario debe especificarse en formato de \\ nombre de usuario de dominio para un usuario de \_ dominio. El nombre de usuario debe especificarse en formato "nombre de usuario de nombre de servidor" para \_ un usuario local en un equipo \\ \_ servidor. El valor predeterminado es *True*.

### <a name="credssp"></a>CredSSP

Permite al cliente usar la autenticación del proveedor de compatibilidad de seguridad de credenciales (CredSSP). CredSSP permite que una aplicación delegue las credenciales del usuario desde el equipo cliente al servidor de destino. El valor predeterminado es *False*.

### <a name="defaultports"></a>DefaultPorts

Especifica los puertos que el cliente usará para HTTP o HTTPS.

**WinRM 2.0:** El puerto HTTP predeterminado es 5985 y el puerto HTTPS predeterminado es 5986.

### <a name="trustedhosts"></a>TrustedHosts

Especifica la lista de equipos remotos de confianza. Otros equipos de un grupo de trabajo o equipos de un dominio diferente deben agregarse a esta lista.

> [!Note]
> Los equipos de la lista TrustedHosts no están autenticados. El cliente puede enviar información de credenciales a estos equipos.

Si se especifica una dirección IPv6 para trustedHost, la dirección debe ir entre corchetes, como se muestra en el siguiente comando de la utilidad winrm: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Para obtener más información sobre cómo agregar equipos a la lista TrustedHosts, escriba `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Opciones de configuración predeterminadas del servicio WinRM

La versión de servicio de WinRM tiene las siguientes opciones de configuración predeterminadas.

### <a name="rootsddl"></a>RootSDDL

Especifica el descriptor de seguridad que controla el acceso remoto al agente de escucha. El valor predeterminado es "O:NSG:BAD:P(A;; GA;;; BA)(A;; GR;;; ER)S:P(AU;FA; GA;;; WD)(AU;SA; GWGX;;; WD)".

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

Número máximo de operaciones simultáneas. El valor predeterminado es 100.

**WinRM 2.0:** La configuración MaxConcurrentOperations está en desuso y se establece en de solo lectura. Esta configuración se ha reemplazado por MaxConcurrentOperationsPerUser.

### <a name="maxconcurrentoperationsperuser"></a>MaxConcurrentOperationsPerUser

Especifica el número máximo de operaciones simultáneas que cualquier usuario puede abrir de forma remota en el mismo sistema. El valor predeterminado es 1500.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Especifica el tiempo de espera de inactividad en milisegundos entre los mensajes de extracción. El valor predeterminado es 60 000.

### <a name="maxconnections"></a>MaxConnections

Especifica el número máximo de solicitudes activas que el servicio puede procesar simultáneamente. El valor predeterminado es 300.

**WinRM 2.0:** El valor predeterminado es 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Especifica el tiempo máximo, en segundos, que tarda el servicio WinRM en recuperar un paquete. El valor predeterminado es 120 segundos.

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

Permite que el servicio WinRM use la autenticación del proveedor de soporte técnico de seguridad de credenciales (CredSSP). El valor predeterminado es *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Establece la directiva para los requisitos de token de enlace de canal en las solicitudes de autenticación. El valor predeterminado es *Relaxed*.

### <a name="defaultports"></a>DefaultPorts

Especifica los puertos que el servicio WinRM usará para HTTP o HTTPS.

**WinRM 2.0:** El puerto HTTP predeterminado es 5985 y el puerto HTTPS predeterminado es 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter e IPv6Filter

Especifica las direcciones IPv4 o IPv6 que pueden usar los agentes de escucha. Los valores predeterminados son IPv4Filter = \* e IPv6Filter = \* .

**IPv4:** Una cadena literal IPv4 consta de cuatro números decimales de puntos, cada uno en el intervalo de 0 a 255. Por ejemplo: 192.168.0.0.

**IPv6:** Una cadena literal IPv6 se incluye entre corchetes y contiene números hexadecimales separados por dos puntos. Por ejemplo: \[ ::1 \] o \[ 3ffe:ffff::6ECB:0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Especifica si el agente de escucha HTTP de compatibilidad está habilitado. Si esta configuración es *True*, el agente de escucha escuchará en el puerto 80 además del puerto 5985. El valor predeterminado es *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Especifica si el agente de escucha HTTPS de compatibilidad está habilitado. Si esta configuración es *True*, el agente de escucha escuchará en el puerto 443 además del puerto 5986. El valor predeterminado es *False*.

## <a name="winrs-default-configuration-settings"></a>Configuración predeterminada de Winrs Configuración

`winrm quickconfig`también configura los **valores predeterminados de Winrs.**

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Permite el acceso a shells remotos. Si establece este parámetro en *False*, el servidor rechazará las nuevas conexiones de shell remoto. El valor predeterminado es *True*.

### <a name="idletimeout"></a>IdleTimeout

Especifica el tiempo máximo, en milisegundos, que el shell remoto permanecerá abierto cuando no haya ninguna actividad de usuario en el shell remoto. El shell remoto se elimina automáticamente después de que transcurra el tiempo especificado.

**WinRM 2.0:** El valor predeterminado es 180000. El valor mínimo es 60 000. Establecer este valor por debajo de 60 000 no tendrá ningún efecto en el tiempo de espera.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Especifica el número máximo de usuarios que pueden realizar simultáneamente operaciones remotas en el mismo equipo a través de un shell remoto. Las nuevas conexiones de shell remoto se rechazarán si superan el límite especificado. El valor predeterminado es 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Especifica el tiempo máximo, en milisegundos, que puede ejecutar el comando remoto o el script. El valor predeterminado es 28800000.

**WinRM 2.0:** La opción MaxShellRunTime se establece en solo lectura. Cambiar el valor de MaxShellRunTime no tendrá ningún efecto en los shells remotos.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Especifica el número máximo de procesos que cualquier operación de shell puede iniciar. Un valor de 0 permite un número ilimitado de procesos. El valor predeterminado es 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Especifica la cantidad máxima de memoria asignada por shell, incluidos los procesos secundarios del shell. El valor predeterminado es 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Especifica el número máximo de shells simultáneos que puede abrir de forma remota cada usuario en el mismo equipo. Si esta configuración de directiva está habilitada, el usuario no podrá abrir nuevos shells remotos si el recuento supera el límite especificado. Si se deshabilita la configuración de la directiva o no se configura, el límite quedará establecido en 5 shells remotos por usuario de forma predeterminada.

## <a name="configuring-winrm-with-group-policy"></a>Configuración de WinRM con directiva de grupo

Use el editor directiva de grupo para configurar Windows Remote Shell y WinRM para equipos de su empresa.

### <a name="to-configure-with-group-policy"></a>Para configurar con directiva de grupo

1. Abra una ventana de símbolo del sistema como administrador.
2. En el símbolo del sistema, escriba `gpedit.msc`. Se **abre Editor de objetos de directiva de grupo** ventana de configuración.
3. Busque el **Windows remote** **management** and Windows Remote Shell directiva de grupo Objects (GPO) en Computer Configuration Plantillas administrativas Windows Components (Componentes de Plantillas administrativas **Windows \\ \\ equipo).**
4. En la **pestaña Extendido,** seleccione una configuración para ver una descripción. Haga doble clic en una configuración para editarla.

## <a name="windows-firewall-and-winrm-20-ports"></a>Windows Firewall y puertos WinRM 2.0

A partir de WinRM 2.0, los puertos de escucha predeterminados configurados por son el puerto 5985 para el transporte HTTP y el `Winrm quickconfig` puerto 5986 para HTTPS. Los agentes de escucha de WinRM se pueden configurar en cualquier puerto arbitrario.

Si un equipo se actualiza a WinRM 2.0, se migran los agentes de escucha configurados previamente y siguen recibiendo tráfico.

## <a name="winrm-installation-and-configuration-notes"></a>Notas de instalación y configuración de WinRM

WinRM no depende de ningún otro servicio excepto WinHttp. Si el servicio de administración de IIS está instalado en el mismo equipo, es posible que vea mensajes que indican que WinRM no se puede cargar antes de Internet Information Services (IIS). Sin embargo, WinRM no depende realmente de IIS, ya que el orden de carga garantiza que el servicio IIS se inicie &mdash; antes que el servicio HTTP. WinRM requiere que `WinHTTP.dll` se registre.

Si el cliente de firewall ISA2004 está instalado en el equipo, puede provocar que un cliente de Servicios web para la administración (WS-Management) deje de responder. Para evitar este problema, instale ISA2004 Firewall SP1.

Si dos servicios de escucha con direcciones IP diferentes están configurados con el mismo número de puerto y nombre de equipo, WinRM escucha o recibe mensajes en una sola dirección. Esto se debe a que los prefijos de dirección URL usados por WS-Management protocolo son los mismos.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Notas de instalación del proveedor y del controlador IPMI

Es posible que el controlador no detecte la existencia de controladores IPMI que no son de Microsoft. Si el controlador no se inicia, es posible que deba deshabilitarlo.

Si los recursos del controlador de administración de placa base [(BMC)](./windows-remote-management-glossary.md#b) aparecen en el BIOS del sistema, ACPI (Plug and Play) detecta el hardware de BMC e instala automáticamente el controlador IPMI. Plug and Play compatibilidad con los BMC podría no estar presente en todos los BMC. Si el BMC se detecta mediante Plug and Play, aparece un dispositivo desconocido en Administrador de dispositivos antes de instalar el componente de administración de hardware. Cuando se instala el controlador, aparece un nuevo componente, el dispositivo compatible con IPMI genérico de Microsoft ACPI, en Administrador de dispositivos.

Si el sistema no detecta automáticamente el BMC e instala el controlador, pero se detectó un BMC durante el proceso de instalación, debe crear el dispositivo BMC. Para ello, escriba el siguiente comando en un símbolo del sistema: `Rundll32 ipmisetp.dll, AddTheDevice` . Después de ejecutar este comando, se crea el dispositivo IPMI y aparece en Administrador de dispositivos. Si desinstala el componente Administración de hardware, se quita el dispositivo.

Para obtener más información, vea [Introducción a la administración de hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

El proveedor IPMI coloca las clases de hardware en el **espacio de nombres de hardware \\ raíz** [de](/windows/desktop/WmiSdk/gloss-n) WMI. Para obtener más información sobre las clases de hardware, vea [Proveedor de IPMI.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Para obtener más información sobre los espacios *de nombres WMI*, vea Arquitectura [wmi](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Notas de configuración del complemento WMI

A partir Windows 8 y Windows Server 2012, los complementos WMI tienen sus [propias](./windows-remote-management-glossary.md#w) configuraciones de seguridad. Para que un usuario normal o de encendido (que no sea administrador) pueda usar el [](./windows-remote-management-glossary.md#l) *complemento WMI,* debe habilitar el acceso para ese usuario una vez configurado el agente de escucha. En primer lugar, debe configurar el usuario para el acceso remoto [a WMI](./windows-remote-management-glossary.md#w) mediante uno de estos pasos.

- Ejecute `lusrmgr.msc` para agregar el usuario al grupo **WinRMRemoteWMIUsers \_ \_** en la ventana Usuarios y **grupos** locales, o bien
- use la herramienta de línea de comandos **winrm** para configurar el descriptor de seguridad para el espacio de nombres del [complemento WMI,](./windows-remote-management-glossary.md#w)como se muestra a continuación: [](./windows-remote-management-glossary.md#n) `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Cuando aparezca la interfaz de usuario, agregue el usuario.

Después de configurar el usuario para el acceso remoto a [WMI,](./windows-remote-management-glossary.md#w)debe configurar *WMI* para permitir que el usuario acceda al complemento. Para ello, ejecute para modificar la seguridad de WMI para el espacio de nombres al que se va a `wmimgmt.msc` tener acceso en la ventana Control **WMI.**  [](./windows-remote-management-glossary.md#n)

La mayoría de las clases WMI para la administración están en el **espacio de \\ nombres cimv2** raíz.