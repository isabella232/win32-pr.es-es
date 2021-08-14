---
title: Windows Glosario de administración remota
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532562a45090040cebbefae2bfff601727efb8bca794a9d9833e61a53ad63a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743272"
---
# <a name="windows-remote-management-glossary"></a>Windows Glosario de administración remota


<dl> <dt>

wsman:Items***
</dt> <dd>

Un WS-Management de protocolo devuelto en una enumeración que obtiene las instancias y las [*EPR de instancia.*](/windows) **wsman:Items** es un contenedor que contiene una instancia de y su EPR. Este tipo de enumeración se inicia cuando la **marca WSManFlagReturnObjectAndEPR** se establece en la solicitud.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**controlador de administración de placa base (BMC)**
</dt> <dd>

Un microcontrolador conectado localmente a un servidor. Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión. Tiene acceso a los datos de BMC a través del proveedor WMI de interfaz de administración de plataforma inteligente [*(IPMI).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticación básica**
</dt> <dd>

Nombre de usuario y contraseña enviados en el intercambio de autenticación. La autenticación básica se puede configurar para usar el transporte HTTP o HTTPS en un dominio o grupo de trabajo. Este método de autenticación es el menos seguro de todos.

</dd> <dt>

**BMC**
</dt> <dd>

Consulte [*controlador de administración de placa base (BMC).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**CIM**
</dt> <dd>

Vea [*Modelo de información común (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

La aplicación cliente que usa el WS-Management para acceder al servicio de administración en el equipo local o remoto.

</dd> <dt>

**Modelo de información común (CIM)**
</dt> <dd>

El modelo del Grupo de tareas de administración distribuida [*(DMTF)*](windows-remote-management-glossary.md) que describe cómo representar objetos de red y equipos del mundo real. CIM utiliza un paradigma orientado a objetos, donde los objetos administrados se modelan mediante los conceptos de clases e instancias.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticación implícita**
</dt> <dd>

Intercambio en el que el servidor recibe una solicitud de un cliente y envía datos sobre el cliente a un servidor de autenticación, normalmente un controlador de dominio. Si el cliente está autenticado, el servidor recibe una clave de sesión implícita que se usa para autenticar las solicitudes posteriores del cliente.

</dd> <dt>

**Distributed Management Task Force (DMTF)**
</dt> <dd>

La organización del sector que desarrolla estándares de administración y tecnología de integración para entornos empresariales e Internet.

</dd> <dt>

**Dmtf**
</dt> <dd>

Vea [*Distributed Management Task Force (DMTF).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Un recurso que se puede solucionar mediante una referencia [*de punto de conexión (EPR).*](windows-remote-management-glossary.md)

</dd> <dt>

**referencia de punto de conexión (EPR)**
</dt> <dd>

Combinación de elementos WS-Addressing y WS-Management que juntos describen una dirección para un recurso en el encabezado SOAP del mensaje. Se trata de un término de servicio web.

</dd> <dt>

**enumeración**
</dt> <dd>

Un conjunto, o colección, de [*instancias de*](windows-remote-management-glossary.md) recursos o la acción de solicitar dicho conjunto. En WS-Management protocolo, [*WS-Enumeration*](windows-remote-management-glossary.md) se usa para obtener la colección. En la implementación de scripting del servicio WinRM de enumeración, [**se usan Session.Enumerate**](session-enumerate.md) y [**el objeto Enumerator.**](enumerator.md) El método y la interfaz de C++ correspondientes [**son IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

</dd> <dt>

**EPR**
</dt> <dd>

Consulte [*la referencia de punto de conexión (EPR).*](windows-remote-management-glossary.md)

</dd> <dt>

**Servicio de recopilación de eventos**
</dt> <dd>

Componente de sistema operativo que recibe eventos del BMC y otros componentes o aplicaciones del sistema operativo.

</dd> <dt>

**reenvío de eventos**
</dt> <dd>

Se puede enviar una notificación de eventos que se producen en equipos remotos a las aplicaciones de suscripción. El reenvío de eventos no es una característica de WinRM, sino del [Windows de eventos .](/windows/desktop/WES/windows-event-log) El reenvío de eventos está disponible por primera vez en Windows Vista. Las aplicaciones de administración, como Microsoft Operations Manager (MOM) usan el reenvío de eventos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Mecanismo de consulta para especificar un conjunto limitado de instancias en la solicitud de un [*recurso*](windows-remote-management-glossary.md). Puede especificar un *parámetro de filtro* en las llamadas a [**Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialecto de filtro**
</dt> <dd>

Cadena XML que identifica el dialecto [](windows-remote-management-glossary.md) XML utilizado para especificar un filtro en una llamada a [**Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). El servicio WinRM admite [WQL como](/windows/desktop/WmiSdk/wql-sql-for-wmi) dialecto de filtro al recibir solicitudes.

</dd> <dt>

**Fragmento**
</dt> <dd>

Cadena XML que identifica parte de una instancia de un recurso en lugar de todo el recurso. La compatibilidad con fragmentos se encuentra [**en el objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**dialecto de fragmento**
</dt> <dd>

Cadena XML que identifica el dialecto XML utilizado para especificar un [*fragmento*](windows-remote-management-glossary.md). La compatibilidad con fragmentos se encuentra [**en el objeto ResourceLocator.**](resourcelocator.md) El servicio WinRM admite [*XPath para*](windows-remote-management-glossary.md) el dialecto de fragmento al recibir solicitudes.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**en banda**
</dt> <dd>

La aplicación cliente obtiene datos de BMC a través del agente de [*escucha*](windows-remote-management-glossary.md) de WinRM en el sistema operativo.

</dd> <dt>

**Intelligent Platform Management Interface (IPMI)**
</dt> <dd>

Un estándar del sector de TI para la arquitectura del controlador de administración de [*placa base (BMC).*](windows-remote-management-glossary.md) Las Windows de administración de hardware de software suministran un controlador [*IPMI*](windows-remote-management-glossary.md) y un proveedor [*DE IPMI*](windows-remote-management-glossary.md) WMI que permiten que los scripts de administración, las herramientas de línea de comandos y las aplicaciones obtengan datos de BMC. El proveedor IPMI tiene clases [WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

</dd> <dt>

**IPMI**
</dt> <dd>

Consulte [*Intelligent Platform Management Interface (IMPI).*](windows-remote-management-glossary.md)

</dd> <dt>

**Controlador IPMI**
</dt> <dd>

Controlador de kernel que permite el acceso a los dispositivos del controlador de administración de placa base [*(BMC)*](windows-remote-management-glossary.md) desde los componentes del sistema operativo.

</dd> <dt>

**Proveedor de IPMI**
</dt> <dd>

Proveedor WMI estándar que define las clases que modela el [*IPMI*](windows-remote-management-glossary.md) y sus datos. El [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un archivo DLL COM que obtiene datos del BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Kcs**
</dt> <dd>

Vea [*Estilo del controlador de teclado (KCS).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticación Kerberos**
</dt> <dd>

Método de autenticación mutua entre el cliente y el servidor que usa claves cifradas. Para los equipos que se ejecutan Windows sistema operativo basado en el servidor, la cuenta de cliente debe ser una cuenta de dominio en el mismo dominio que el servidor. Cuando un cliente usa credenciales predeterminadas, Kerberos es el método de autenticación si la cadena de conexión no es una de las siguientes: localhost, 127.0.0.1 o \[ ::1 \] .

</dd> <dt>

**Estilo del controlador de teclado (KCS)**
</dt> <dd>

Protocolo utilizado por el controlador [*IPMI para*](windows-remote-management-glossary.md) comunicarse con el controlador de administración de [*placa base (BMC).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Un servicio de administración que implementa WS-Management protocolo para enviar y recibir mensajes. WinRM es un servicio de escucha. Un agente de escucha se define mediante un transporte (HTTP o HTTPS) y una dirección IPv4 o IPv6. Puede crear más de una instancia de agente de escucha de WinRM en un solo equipo si les asigna una dirección TCP/IP o un número de puerto diferentes.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Paquete de información transmitido entre equipos o redes independientes construidas con el [*protocolo SOAP.*](windows-remote-management-glossary.md) El paquete tiene un encabezado , que describe el destino y el transporte del mensaje, y un cuerpo que contiene el contenido que se usará cuando llegue el mensaje. Un mensaje es una combinación de elementos de especificaciones como [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)y [*WS-Management.*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Un espacio de nombres [*WMI,*](windows-remote-management-glossary.md) que es una agrupación lógica de clases e instancias wmi para controlar el ámbito y el acceso. El origen más frecuente de datos de administración para sistemas que ejecutan Windows es el espacio de nombres cimv2 raíz, que contiene clases \\ como [**Proceso de Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process) Los espacios de nombres aparecen en el URI del recurso para las clases WMI, por https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service ejemplo.

</dd> <dt>

**Negociación de la autenticación**
</dt> <dd>

Un tipo negociado de autenticación de inicio de sesión único que es Windows implementación del mecanismo de negociación [*de GSSAPI simple y protegido (SPNEGO).*](windows-remote-management-glossary.md) La negociación SPNEGO determina si Kerberos o NTLM controlan la autenticación. Kerberos es el mecanismo preferido. La negociación de la autenticación Windows en sistemas basados en Windows autenticación integrada.

</dd> <dt>

**sensor numérico**
</dt> <dd>

Tipo numérico de sensor en un controlador de administración de [*placa base (BMC),*](windows-remote-management-glossary.md)por ejemplo, temperatura o voltaje.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Opción**
</dt> <dd>

Datos adicionales necesarios para que el proveedor de recursos procese una solicitud. Por ejemplo, algunos proveedores WMI requieren datos adicionales proporcionados como [**objetos IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet.**](/windows/desktop/WmiSdk/swbemnamedvalueset) La compatibilidad con las opciones se encuentra en [**el objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**fuera de banda**
</dt> <dd>

La aplicación cliente obtiene datos directamente desde el controlador de administración de placa [*base (BMC)*](windows-remote-management-glossary.md) de otro equipo, en lugar de a través del agente de escucha de [*WinRM*](windows-remote-management-glossary.md) en el sistema operativo.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**pull**
</dt> <dd>

Se [*envía un mensaje de extracción WS-Enumeration*](windows-remote-management-glossary.md) para continuar con una enumeración iniciada por una llamada inicial a WS-Enumeration:Enumerate. [**Enumerator.ReadItem**](enumerator-readitem.md) o [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)realizan la operación de extracción en el servicio WinRM.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**resource**
</dt> <dd>

Extremo [*que*](windows-remote-management-glossary.md) representa un tipo distinto de operación o valor de administración. Un servicio expone uno o varios recursos y algunos recursos pueden tener más de una instancia. Un recurso de administración es similar a una clase WMI o una tabla de base de datos, y una instancia es similar a una instancia de la clase o una fila de la tabla. Por ejemplo, la [**clase \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa un recurso. `Win32_LogicalDisk="C:\"` es una instancia específica del recurso.

</dd> <dt>

**URI de recurso**
</dt> <dd>

Identificador [*uniforme de recursos (URI)*](windows-remote-management-glossary.md) que se usa para identificar un tipo específico de recurso, como discos o procesos, en un sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Sel**
</dt> <dd>

Consulte [*Registro de eventos del sistema (SEL).*](windows-remote-management-glossary.md)

</dd> <dt>

**Adaptador de SEL**
</dt> <dd>

Adaptador que envía datos del controlador de administración de placa base [*(BMC)*](windows-remote-management-glossary.md) al [*recopilador de eventos.*](windows-remote-management-glossary.md)

</dd> <dt>

**Selector**
</dt> <dd>

Par de nombre y valor que representa una instancia determinada de un [*recurso*](windows-remote-management-glossary.md). Se trata básicamente de un filtro o "clave" que identifica la instancia deseada del recurso. La compatibilidad con el selector se encuentra en [**el objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**sensor**
</dt> <dd>

Un dispositivo de medida en un controlador de administración de placa [*base (BMC).*](windows-remote-management-glossary.md)

</dd> <dt>

**service**
</dt> <dd>

Una aplicación que proporciona servicios de administración a los clientes a través del protocolo WS-Management y otros [*servicios web*](windows-remote-management-glossary.md). Un servicio suele ser el mismo que el [*agente de escucha*](windows-remote-management-glossary.md) de una red. El servicio tiene una dirección de transporte física.

</dd> <dt>

**Sesión**
</dt> <dd>

Una conexión entre un cliente Windows [*administración*](windows-remote-management-glossary.md) remota y el agente de escucha de [*WinRM*](windows-remote-management-glossary.md)local o remoto, o servicio. Esta conexión es similar a la conexión entre un script de cliente WMI y WMI en un servidor remoto. Las operaciones de sesión, como enumerar un recurso (Enumerar), obtener una instancia de un recurso (Get) o ejecutar un método de recurso (Invoke) son métodos del **objeto Session.** [**WSMan.CreateSession**](wsman-createsession.md)crea un objeto Session. 

</dd> <dt>

**Mecanismo de negociación de GSS-API simple y protegido (SPNEGO)**
</dt> <dd>

Un mecanismo de autenticación utilizado por el cliente o servidor que recibe solicitudes de datos a través de WinRM en Active Directory contexto. SPNEGO se basa en un protocolo de solicitud de comentarios (RFC) generado por el Grupo de tareas de ingeniería de Internet (IETF). SPNEGO también se conoce como [*Windows autenticación integrada,*](windows-remote-management-glossary.md)el término que se usa en los temas de ayuda Windows administración remota.

</dd> <dt>

**Protocolo simple de acceso a objetos (SOAP)**
</dt> <dd>

Protocolo basado en XML que usan los servicios web.

</dd> <dt>

**SOAP**
</dt> <dd>

Vea [*Protocolo de acceso a objetos simple (SOAP).*](windows-remote-management-glossary.md)

</dd> <dt>

**Spnego**
</dt> <dd>

Consulte [*Mecanismo de negociación de GSS-API (SPNEGO) simple y protegido.*](windows-remote-management-glossary.md)

</dd> <dt>

**Registro de eventos del sistema (SEL)**
</dt> <dd>

Base de datos de eventos en el hardware del controlador de administración de placa base [*(BMC).*](windows-remote-management-glossary.md) El [*adaptador SEL*](windows-remote-management-glossary.md) transmite estos eventos al sistema operativo.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**identificador uniforme de recursos (URI)**
</dt> <dd>

Cadena que identifica un recurso de la empresa, como un equipo, un proceso, una unidad de disco o un sensor de temperatura en un controlador de administración de placa base [*(BMC).*](windows-remote-management-glossary.md) El URI es el mecanismo de direccionamiento del servicio web definido en identificador uniforme de recursos (URI) del Grupo de tareas de ingeniería de Internet (IETF): sintaxis \[ genérica RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Consulte [*identificador uniforme de recursos (URI).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**servicio web**
</dt> <dd>

Una aplicación de software que se usa para la interacción entre equipos a través de Internet o una red. El Lenguaje de descripción de [*servicios web (WSDL)*](windows-remote-management-glossary.md)describe los servicios web. La descripción específica del servicio web indica a otros servicios cómo interactuar con el servicio web mediante mensajes SOAP. Los mensajes se transmiten entre equipos mediante un transporte, normalmente HTTP o HTTPS. [*WS-Addressing,*](windows-remote-management-glossary.md) [*WS-Eventing*](windows-remote-management-glossary.md)y [*WS-Management*](windows-remote-management-glossary.md) son ejemplos de protocolos que usan las aplicaciones de servicio web para comunicarse entre sí.

</dd> <dt>

**Lenguaje de descripción del servicio web (WSDL)**
</dt> <dd>

Lenguaje basado en XML que se usa para definir cómo interactuar con un servicio web. Normalmente, wsdl describe qué mensajes SOAP requiere el servicio web para devolver datos o realizar operaciones. WSDL permite que una implementación de un sistema operativo se comunique con el servicio web implementado en otro sistema operativo, siempre y cuando se cumplen los requisitos del WSDL.

</dd> <dt>

**Autenticación integrada de Windows**
</dt> <dd>

Consulte [*Negociación de la autenticación.*](windows-remote-management-glossary.md)

</dd> <dt>

**Instrumental de administración de Windows (WMI)**
</dt> <dd>

Implementación de Microsoft del estándar Web-Based Enterprise Management (WBEM) publicado por el Grupo de tareas de administración distribuida [*(DMTF).*](windows-remote-management-glossary.md) WMI permite administrar equipos y modelos locales y remotos de equipos y objetos de red mediante una extensión del estándar [*Modelo de información común (CIM).*](windows-remote-management-glossary.md)

</dd> <dt>

**Administración remota de Windows (WinRM)**
</dt> <dd>

Implementación de Microsoft de un servicio web de administración basado en el protocolo [*WS-Management*](windows-remote-management-glossary.md) estándar público.

</dd> <dt>

**Windows Shell remoto (WinRS)**
</dt> <dd>

Una herramienta de shell que se basa en [*Windows remoto para*](windows-remote-management-glossary.md) ejecutar comandos remotos, especialmente para servidores sin sentido. La herramienta de línea de comandos es Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Vea [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Complemento WMI**
</dt> <dd>

Complemento WinRM que hace que los datos WMI estén disponibles para los clientes de WinRM.

</dd> <dt>

**WS-Addressing (wsa)**
</dt> <dd>

Un protocolo estándar público, basado en SOAP, que crea un sistema de direccionamiento que se usa en los encabezados de los mensajes enviados a través de Internet. El estándar define cómo se pueden encontrar los recursos entre redes y firewalls. WS-Addressing es uno de los protocolos de servicio web que componen el WS-Management web.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Un protocolo estándar público, basado en SOAP, para enumerar una secuencia de elementos XML que pueden representar colecciones de datos, registros u otras estructuras de información lineal. WS-Enumeration es uno de los protocolos de servicio web que componen el WS-Management web.

</dd> <dt>

**WS-Eventing (wse)**
</dt> <dd>

Un protocolo estándar público, basado en SOAP, que permite a un servicio web (el suscriptor) suscribirse y aceptar mensajes de notificación de eventos de otro servicio web (el origen del evento). WS-Eventing es uno de los protocolos de servicio web que componen el WS-Management web.

</dd> <dt>

**WS-Management**
</dt> <dd>

Un protocolo estándar público, basado en SOAP, para compartir datos de administración entre todos los sistemas operativos, equipos y dispositivos. Todos [*los mensajes*](windows-remote-management-glossary.md) enviados por los componentes de cliente o servidor de WinRM usan este protocolo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Un protocolo estándar público, basado en SOAP, para tener acceso a representaciones XML de recursos basados en servicios web a través de un conjunto sencillo de verbos como Get, Put, Invoke o Delete. WS-Transfer define las operaciones para enviar y recibir la representación de un recurso determinado y las operaciones para crear o eliminar un recurso y su representación correspondiente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Una notación de ruta de acceso para direccionar partes de un documento XML, similar a una dirección URL. Una expresión XPath es una secuencia de frases que se obtienen de la ubicación actual del documento XML a otro nodo o conjunto de nodos. Las frases están separadas por caracteres de barra diagonal ("/"). El servicio WinRM admite [XPath para](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) el [*dialecto de fragmento.*](windows-remote-management-glossary.md)

</dd> </dl>

 

 