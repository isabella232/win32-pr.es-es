---
title: Administración remota de Windows Glosario
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105678667"
---
# <a name="windows-remote-management-glossary"></a>Administración remota de Windows Glosario


<dl> <dt>

wsman: items * * * *
</dt> <dd>

WS-Management elemento de protocolo devuelto en una enumeración que obtiene las instancias y la instancia de [*EPRs*](/windows). **wsman: items** es un contenedor que contiene una instancia y su EPR. Este tipo de enumeración se inicia cuando se establece la marca **WSManFlagReturnObjectAndEPR** en la solicitud.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**controlador de administración de placa base (BMC)**
</dt> <dd>

Microcontrolador conectado localmente a un servidor. Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión. Tiene acceso a los datos de BMC a través del proveedor WMI de [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Autenticación básica**
</dt> <dd>

El nombre de usuario y la contraseña enviados en el intercambio de autenticación. La autenticación básica puede configurarse para usar el transporte HTTP o HTTPS en un dominio o grupo de trabajo. Este método de autenticación es el menos seguro de todos.

</dd> <dt>

**BMC**
</dt> <dd>

Consulte [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**ESTUDIO**
</dt> <dd>

Consulte [*modelo de información común (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

La aplicación cliente que usa el protocolo WS-Management para tener acceso al servicio de administración en el equipo local o remoto.

</dd> <dt>

**Modelo de información común (CIM)**
</dt> <dd>

El modelo de la [*aplicación de administración distribuida (DMTF)*](windows-remote-management-glossary.md) que describe cómo representar los objetos de equipo y de red del mundo real. CIM utiliza un paradigma orientado a objetos, donde los objetos administrados se modelan mediante los conceptos de clases e instancias.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticación implícita**
</dt> <dd>

Un intercambio en el que el servidor recibe una solicitud de un cliente y envía datos sobre el cliente a un servidor de autenticación, normalmente un controlador de dominio. Si el cliente está autenticado, el servidor recibe una clave de sesión implícita que se usa para autenticar las solicitudes posteriores desde el cliente.

</dd> <dt>

**Distributed Management Task Force (DMTF)**
</dt> <dd>

La organización del sector que desarrolla estándares de administración y tecnología de integración para entornos empresariales y de Internet.

</dd> <dt>

**DTMF**
</dt> <dd>

Consulte [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**finales**
</dt> <dd>

Un recurso que se puede direccionar mediante una [*referencia de extremo (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**referencia de extremo (EPR)**
</dt> <dd>

Combinación de elementos de dirección WS-Addressing y WS-Management que describen de forma conjunta una dirección de un recurso en el encabezado SOAP del mensaje. Se trata de un término de servicio Web.

</dd> <dt>

**enumeración**
</dt> <dd>

Conjunto o colección de instancias de [*recurso*](windows-remote-management-glossary.md) o acción de solicitar este conjunto. En WS-Management protocolo, se usa [*WS-Enumeration*](windows-remote-management-glossary.md) para obtener la colección. En la implementación de scripting del servicio WinRM de enumeración, se usan [**Session. Enumerate**](session-enumerate.md) y el objeto de [**enumerador**](enumerator.md) . El método y la interfaz de C++ correspondientes son [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) y [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Consulte [*referencia de extremo (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Servicio de recopilación de eventos**
</dt> <dd>

Componente del sistema operativo que recibe eventos del BMC y otros componentes o aplicaciones del sistema operativo.

</dd> <dt>

**reenvío de eventos**
</dt> <dd>

Una notificación de eventos que se producen en equipos remotos se puede enviar a aplicaciones de suscripción. El reenvío de eventos no es una característica de WinRM, sino del [registro de eventos de Windows](/windows/desktop/WES/windows-event-log). El reenvío de eventos está disponible por primera vez en Windows Vista. Las aplicaciones de administración, como Microsoft Operations Manager (MOM) usan el reenvío de eventos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Mecanismo de consulta para especificar un conjunto limitado de instancias en la solicitud de un [*recurso*](windows-remote-management-glossary.md). Puede especificar un parámetro de *filtro* en las llamadas a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialecto de filtro**
</dt> <dd>

Cadena XML que identifica el dialecto XML usado para especificar un [*filtro*](windows-remote-management-glossary.md) en una llamada a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). El servicio WinRM admite [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialecto de filtro al recibir solicitudes.

</dd> <dt>

**Fragment**
</dt> <dd>

Cadena XML que identifica parte de una instancia de un recurso en lugar de todo el recurso. La compatibilidad de fragmentos se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**dialecto de fragmento**
</dt> <dd>

Cadena XML que identifica el dialecto XML usado para especificar un [*fragmento*](windows-remote-management-glossary.md). La compatibilidad de fragmentos se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) . El servicio WinRM admite [*XPath*](windows-remote-management-glossary.md) para el dialecto de fragmentos al recibir solicitudes.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**en banda**
</dt> <dd>

La aplicación cliente obtiene los datos de BMC a través del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM en el sistema operativo.

</dd> <dt>

**Interfaz de administración de plataforma inteligente (IPMI)**
</dt> <dd>

Un estándar del sector de TI para la arquitectura del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md). Las características de administración de hardware de Windows proporcionan un [*controlador IPMI*](windows-remote-management-glossary.md) y un [*proveedor IPMI*](windows-remote-management-glossary.md) de WMI que permite que los scripts de administración, las herramientas de línea de comandos y las aplicaciones obtengan datos de BMC. El proveedor IPMI tiene [clases](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.

</dd> <dt>

**IPMI**
</dt> <dd>

Vea [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Controlador IPMI**
</dt> <dd>

El controlador de kernel que permite el acceso a los dispositivos del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) desde los componentes del sistema operativo.

</dd> <dt>

**Proveedor IPMI**
</dt> <dd>

Proveedor WMI estándar que define las clases que modelan la [*IPMI*](windows-remote-management-glossary.md) y sus datos. El [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un archivo dll com que obtiene datos de BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Consulte [*estilo de controladora de teclado (KCS)*](windows-remote-management-glossary.md).

</dd> <dt>

**Autenticación Kerberos**
</dt> <dd>

Método de autenticación mutua entre el cliente y el servidor que usa claves cifradas. En el caso de los equipos que se ejecutan en un sistema operativo basado en Windows, la cuenta de cliente debe ser una cuenta de dominio en el mismo dominio que el servidor. Cuando un cliente usa las credenciales predeterminadas, Kerberos es el método de autenticación si la cadena de conexión no es una de las siguientes: localhost, 127.0.0.1 o \[ :: 1 \] .

</dd> <dt>

**Estilo de controlador de teclado (KCS)**
</dt> <dd>

Protocolo utilizado por el [*controlador IPMI*](windows-remote-management-glossary.md) para comunicarse con el [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Servicio de administración que implementa WS-Management protocolo para enviar y recibir mensajes. WinRM es un servicio de escucha. Un agente de escucha se define mediante un transporte (HTTP o HTTPS) y una dirección IPv4 o IPv6. Puede crear más de una instancia del agente de escucha de WinRM en un solo equipo proporcionándole una dirección TCP/IP diferente o un número de puerto.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Paquete de información transmitida entre equipos o redes independientes construidas con el protocolo [*SOAP*](windows-remote-management-glossary.md) . El paquete tiene un encabezado, que describe el destino del mensaje y el transporte, y un cuerpo que incluye el contenido que se va a utilizar cuando llegue el mensaje. Un mensaje es una combinación de elementos de especificaciones como [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)y [*WS-Management*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Un espacio de nombres [*WMI*](windows-remote-management-glossary.md) , que es una agrupación lógica de clases e instancias WMI para controlar el ámbito y el acceso. La fuente más frecuente de datos de administración para sistemas que ejecutan Windows es el \\ espacio de nombres root cimv2, que contiene clases como el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process). Los espacios de nombres aparecen en el URI de recurso para las clases WMI, por ejemplo https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .

</dd> <dt>

**Negociar la autenticación**
</dt> <dd>

Un tipo de autenticación negociada y de inicio de sesión único que es la implementación de Windows del [*mecanismo de negociación de GSSAPI simple y protegido (SPNEGO)*](windows-remote-management-glossary.md). La negociación SPNEGO determina si la autenticación se controla mediante Kerberos o NTLM. Kerberos es el mecanismo preferido. Negociar la autenticación en sistemas basados en Windows también se denomina autenticación integrada de Windows.

</dd> <dt>

**sensor numérico**
</dt> <dd>

Un tipo numérico de sensor en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md), por ejemplo, temperatura o tensión.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Opción**
</dt> <dd>

Los datos adicionales requeridos por el proveedor de recursos para procesar una solicitud. Por ejemplo, algunos proveedores de WMI requieren datos adicionales proporcionados como objetos [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) . La compatibilidad con la opción se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**fuera de banda**
</dt> <dd>

La aplicación cliente obtiene los datos directamente del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) de otro equipo, en lugar de hacerlo a través del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM en el sistema operativo.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**obtener**
</dt> <dd>

Se envía un mensaje de extracción [*de WS-Enumeration*](windows-remote-management-glossary.md) para continuar una enumeración iniciada por una llamada inicial a WS-Enumeration: Enumerate. El [**enumerador**](enumerator-readitem.md) realiza la operación de extracción en el servicio WinRM. Readitem o [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**resource**
</dt> <dd>

Un [*extremo*](windows-remote-management-glossary.md) que representa un tipo distinto de operación de administración o valor. Un servicio expone uno o más recursos y algunos recursos pueden tener más de una instancia. Un recurso de administración es similar a una clase WMI o una tabla de base de datos, y una instancia de es similar a una instancia de la clase o una fila de la tabla. Por ejemplo, la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa un recurso. `Win32_LogicalDisk="C:\"` es una instancia específica del recurso.

</dd> <dt>

**URI de recurso**
</dt> <dd>

[*Identificador uniforme de recursos (URI)*](windows-remote-management-glossary.md) que se usa para identificar un tipo específico de recurso, como discos o procesos, en un sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**SEL**
</dt> <dd>

Consulte [*registro de eventos del sistema (SEL)*](windows-remote-management-glossary.md).

</dd> <dt>

**Adaptador SEL**
</dt> <dd>

Adaptador que envía los datos del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) al [*recopilador de eventos*](windows-remote-management-glossary.md).

</dd> <dt>

**situado**
</dt> <dd>

Un par de nombre y valor que representa una instancia determinada de un [*recurso*](windows-remote-management-glossary.md). Es esencialmente un filtro o una "clave" que identifica la instancia deseada del recurso. La compatibilidad con el selector se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .

</dd> <dt>

**sensor**
</dt> <dd>

Un dispositivo de medición en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).

</dd> <dt>

**service**
</dt> <dd>

Aplicación que proporciona servicios de administración a los clientes a través del Protocolo de WS-Management y otros [*servicios web*](windows-remote-management-glossary.md). Normalmente, un servicio es el mismo que el [*agente de escucha*](windows-remote-management-glossary.md) de una red. El servicio tiene una dirección de transporte física.

</dd> <dt>

**sesión**
</dt> <dd>

Una conexión entre un [*cliente*](windows-remote-management-glossary.md) administración remota de Windows y el [*agente de escucha*](windows-remote-management-glossary.md)WinRM local o remoto, o servicio. Esta conexión es similar a la conexión entre un script de cliente WMI y WMI en un servidor remoto. Las operaciones de sesión, como enumerar un recurso (enumerar), obtener una instancia de un recurso (GET) o ejecutar un método de recursos (Invoke) son métodos del objeto de **sesión** . [**WSMan. createSession**](wsman-createsession.md)crea un objeto de **sesión** .

</dd> <dt>

**Mecanismo de negociación simple y protegida de GSS-API (SPNEGO)**
</dt> <dd>

Mecanismo de autenticación utilizado por el cliente o el servidor que recibe solicitudes de datos a través de WinRM en un contexto de Active Directory. SPNEGO se basa en un protocolo de solicitud de comentarios (RFC) producido por Internet Engineering Task Force (IETF). SPNEGO también se conoce como [*autenticación integrada de Windows*](windows-remote-management-glossary.md), el término que se usa en los temas de ayuda de administración remota de Windows.

</dd> <dt>

**Protocolo simple de acceso a objetos (SOAP)**
</dt> <dd>

Protocolo basado en XML utilizado por los servicios Web.

</dd> <dt>

**SOAP**
</dt> <dd>

Vea [*Protocolo simple de acceso a objetos (SOAP)*](windows-remote-management-glossary.md).

</dd> <dt>

**SPNEGO**
</dt> <dd>

Consulte [*mecanismo de negociación simple y protegida de GSS-API (SPNEGO)*](windows-remote-management-glossary.md).

</dd> <dt>

**Registro de eventos del sistema (SEL)**
</dt> <dd>

La base de datos de eventos en el hardware del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) . El [*adaptador SEL*](windows-remote-management-glossary.md) transmite estos eventos al sistema operativo.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**identificador uniforme de recursos (URI)**
</dt> <dd>

Cadena que identifica un recurso de la empresa, como un equipo, un proceso, una unidad de disco o un sensor de temperatura en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md). El URI es el mecanismo de direccionamiento del servicio Web definido en el identificador uniforme de recursos (URI) de Internet Engineering Task Force (IETF): Sintaxis genérica \[ RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Consulte [*identificador uniforme de recursos (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**servicio Web**
</dt> <dd>

Aplicación de software que se usa para la interacción entre equipos a través de Internet o una red. Los servicios web se describen mediante el [*lenguaje de descripción de servicios web (WSDL)*](windows-remote-management-glossary.md). La descripción específica del servicio web indica a otros servicios cómo interactuar con el servicio Web mediante mensajes SOAP. Los mensajes se transmiten entre equipos mediante un transporte, normalmente HTTP o HTTPS. [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)y [*WS-Management*](windows-remote-management-glossary.md) son ejemplos de protocolos usados por las aplicaciones de servicios web para comunicarse entre sí.

</dd> <dt>

**Lenguaje de descripción de servicios web (WSDL)**
</dt> <dd>

Lenguaje basado en XML que se usa para definir cómo interactuar con un servicio Web. Normalmente, el WSDL describe qué mensajes SOAP requiere el servicio web para devolver datos o realizar operaciones. El WSDL permite que una implementación de un sistema operativo se comunique con el servicio Web implementado en otro sistema operativo, siempre que se cumplan los requisitos del WSDL.

</dd> <dt>

**Autenticación integrada de Windows**
</dt> <dd>

Consulte [*negociar la autenticación*](windows-remote-management-glossary.md).

</dd> <dt>

**Instrumental de administración de Windows (WMI)**
</dt> <dd>

La implementación de Microsoft del estándar Web-Based Enterprise Management (WBEM) publicada por el [*equipo de administración distribuida (DMTF)*](windows-remote-management-glossary.md). WMI permite administrar equipos locales y remotos y modela los objetos de equipo y red mediante una extensión del estándar [*modelo de información común (CIM)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Administración remota de Windows (WinRM)**
</dt> <dd>

Implementación de Microsoft de un servicio Web de administración basado en el protocolo [*WS-Management*](windows-remote-management-glossary.md) estándar público.

</dd> <dt>

**Shell remoto de Windows (WinRS)**
</dt> <dd>

Herramienta de Shell que se basa en [*administración remota de Windows*](windows-remote-management-glossary.md) para ejecutar comandos remotos, especialmente en el caso de los servidores sin periféricos. La herramienta de línea de comandos es Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Consulte [*instrumental de administración de Windows (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Complemento WMI**
</dt> <dd>

El complemento WinRM que hace que los datos de WMI estén disponibles para los clientes de WinRM.

</dd> <dt>

**WS-Addressing (WSA)**
</dt> <dd>

Un protocolo estándar público, que está basado en SOAP, que crea un sistema de direcciones usado en los encabezados de los mensajes enviados a través de Internet. El estándar define cómo se pueden ubicar los recursos a través de redes y firewalls. WS-Addressing es uno de los protocolos de servicio Web que componen el protocolo WS-Management.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Protocolo estándar público, que se basa en SOAP, para enumerar una secuencia de elementos XML que pueden representar colecciones de datos, registros u otras estructuras de información lineal. WS-Enumeration es uno de los protocolos de servicio Web que componen el protocolo WS-Management.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Protocolo estándar público, que está basado en SOAP, que permite a un servicio Web (el suscriptor) suscribirse y aceptar mensajes de notificación de eventos de otro servicio Web (el origen del evento). WS-Eventing es uno de los protocolos de servicio Web que componen el protocolo WS-Management.

</dd> <dt>

**WS-Management**
</dt> <dd>

Un protocolo estándar público, que está basado en SOAP, para compartir datos de administración entre todos los sistemas operativos, equipos y dispositivos. Todos los [*mensajes*](windows-remote-management-glossary.md) enviados por los componentes de servidor o cliente de WinRM usan este protocolo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Un protocolo estándar público, que está basado en SOAP, para tener acceso a representaciones XML de recursos basados en servicios web a través de un sencillo conjunto de verbos como Get, Put, Invoke o DELETE. WS-Transfer define operaciones para enviar y recibir la representación de un recurso determinado y operaciones para crear o eliminar un recurso y su representación correspondiente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Una notación de ruta de acceso para direccionar partes de un documento XML, similar a una dirección URL. Una expresión XPath es una secuencia de frases que se va a obtener de la ubicación actual del documento XML a otro nodo o conjunto de nodos. Las frases se separan con caracteres de barra diagonal ("/"). El servicio WinRM admite [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) para el [*dialecto de fragmentos*](windows-remote-management-glossary.md).

</dd> </dl>

 

 