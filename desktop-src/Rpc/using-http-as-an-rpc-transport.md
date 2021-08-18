---
title: Uso de HTTP como transporte RPC
description: RPC sobre HTTP permite a los programas cliente usar Internet para ejecutar procedimientos proporcionados por programas de servidor en redes lejanas.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8775aab1771dcc6da9cade97d36c7141d6d66d8bc8172a20c8263ef64b8ed7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010793"
---
# <a name="using-http-as-an-rpc-transport"></a>Uso de HTTP como transporte RPC

RPC sobre HTTP permite a los programas cliente usar Internet para ejecutar procedimientos proporcionados por programas de servidor en redes lejanas. RPC a través de HTTP tunela sus llamadas a través de un puerto HTTP establecido. Por lo tanto, sus llamadas pueden cruzar los firewalls de red en las redes cliente y servidor.

RPC a través de HTTP enruta sus llamadas al proxy RPC ubicado en la red del servidor RPC. El proxy RPC establece y mantiene una conexión con el servidor RPC. Actúa como proxy, enviando llamadas a procedimiento remoto al servidor RPC y enviando las respuestas del servidor a través de Internet a la aplicación cliente. Este proceso se ilustra en el diagrama siguiente.

![interacción entre un servidor rpc y un servidor de información de Internet para http rpc](images/httprpc1.png)

El diagrama muestra un firewall en la red de la aplicación cliente. Esto no es necesario para que RPC sobre HTTP funcione. Sin embargo, si la red cliente tiene un firewall, también necesitará un programa de servidor proxy como Servidor proxy de Microsoft.

Cuando el programa cliente emite una llamada a procedimiento remoto mediante HTTP como transporte, la biblioteca en tiempo de ejecución rpc del cliente se pone en contacto con el proxy RPC. Dependiendo de si se solicitó al cliente RPC que use el puerto HTTP o HTTPS (HTTP con SSL) 80 o el puerto 443, respectivamente. El proxy RPC se pone en contacto con el programa de servidor RPC y establece una conexión TCP/IP. El cliente y el proxy RPC mantienen su conexión HTTP o HTTPS a través de Internet. La conexión HTTP o HTTPS del cliente al proxy RPC puede pasar a través de un firewall (sujeto a los permisos de acceso adecuados) si hay alguno. A continuación, el servidor puede ejecutar la llamada a procedimiento remoto y usar la conexión a través del proxy RPC para responder al cliente. El proxy RPC es una extensión ISAPI que se ejecuta en el contexto de IIS.

Si el cliente o el servidor se desconectan por cualquier motivo, el proxy RPC lo detectará y finalizará la sesión RPC. Mientras la sesión continúe, el proxy RPC mantendrá sus conexiones con el cliente y el servidor. Reenviará las llamadas a procedimiento remoto desde el cliente al servidor y enviará respuestas del servidor al cliente.

El programa cliente RPC puede tunenelización de sus llamadas RPC a través de Internet mediante la creación de un enlace de cadena con el formato:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Donde:

-   *object \_ uuid* especifica un UUID de objeto RPC. Para obtener más información, vea [Generar UUID](generating-interface-uuids.md) de interfaz y [UUID de cadena.](string-uuid.md)
-   **ncacn \_ http selecciona** la especificación de secuencia de protocolo para RPC a través de HTTP. Para obtener más información, vea [Constantes de secuencia de protocolo y](protocol-sequence-constants.md) Enlace de [cadenas.](string-binding.md)
-   *rpc \_ server* es la dirección de red del equipo que ejecuta el proceso de servidor RPC. La dirección del servidor debe especificarse en un formulario visible y comprensible para el equipo proxy RPC, no para el cliente. Puesto que el cliente no se conecta directamente al servidor, no necesita poder resolver el nombre del servidor ni establecer una conexión con él. El proxy RPC establecerá la conexión en nombre del cliente y, por lo tanto, el servidor *rpc \_* debe ser un nombre reconocible por el proxy RPC.
-   *el* punto de conexión especifica el puerto TCP/IP al que escucha el proceso del servidor RPC para las llamadas a procedimiento remoto. Para obtener más información, vea [Buscar puntos de conexión.](finding-endpoints.md)
-   **HttpProxy** especifica opcionalmente un servidor proxy HTTP en la red del cliente RPC, como Servidor proxy de Microsoft. Si se selecciona un servidor proxy, no se especifica ningún número de puerto, el código auxiliar rpc usa el puerto 80 de forma predeterminada si no se solicita SSL y el puerto 443 si se especifica SSL.
-   **RpcProxy** especifica la dirección y el número de puerto del equipo IIS que actúa como proxy para el servidor RPC. Solo debe especificarlo si el proceso del servidor RPC reside en un equipo diferente al proxy RPC. Si no especifica un número de puerto, el código auxiliar del cliente RPC usa de forma predeterminada el puerto 80 si no se especifica SSL y usa el puerto 443 si se especifica SSL (HTTPS).
-   **HttpConnectionOption** permite, opcionalmente, dirigir el comportamiento de RPC al realizar conexiones HTTP. El **valor UseHttpProxy** indica a RPC que enruta su tráfico a través del proxy HTTP en todo momento, incluso cuando el cliente tiene sus opciones de Internet establecidas en Internet Explorer en "Omitir servidor proxy para direcciones locales".

    Esta opción se admite en Windows 7, Windows Server 2008 R2, Windows 8.1 y Windows Server 2012 R2 con KB2916915 instalado. Esta opción no se admite en Windows 8 y Windows Server 2012. Las aplicaciones pueden determinar si el tiempo de ejecución de RPC admite esta opción comprobando el valor del Registro **ConnectionOptionsFlag** ubicado en la siguiente clave del Registro:

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Rpc**

    Si se establece el bit 0 (LSB) de este valor del Registro, se admite esta opción específica. De lo contrario, el entorno de ejecución de RPC no admite esta opción en el sistema.

Para obtener más información sobre cómo crear enlaces de cadena, vea [Enlace y identificadores.](binding-and-handles.md)

El programa de servidor RPC puede aceptar llamadas RPC tuneladas escuchando en la secuencia del \_ protocolo HTTP ncacn.

Microsoft tiene dos implementaciones principales de RPC sobre HTTP: versión 1 y versión 2.

La versión 1 (denominada RPC sobre HTTP v1) se admite a través Windows XP. La versión 1 del proxy RPC se admite Windows 2000.

La versión 2 (llamada RPC sobre HTTP v2) es la versión actual.

Las dos versiones tienen capacidades diferentes e interoperabilidad limitada. Aquí se proporciona un resumen de las diferencias. Para ver las consideraciones de interoperabilidad, consulte Requisitos del sistema [e interoperabilidad de RPC a través de HTTP.](system-requirements-and-interoperability-for-rpc-over-http.md)

-   RPC a través de HTTP v1 requiere que la tunelización SSL esté habilitada en todos los servidores proxy o firewalls HTTP entre el cliente RPC a través de HTTP y el proxy RPC. RPC a través de HTTP v1 intenta compilar una instancia de SSL Tunnel a través del puerto 80, aunque los datos que envía no están cifrados con SSL. Los servidores proxy y los firewalls normalmente rechazan estas solicitudes a menos que se configuren explícitamente para permitirlas. RPC a través de HTTP v2 no tiene este requisito.
-   RPC a través de HTTP v1 no puede establecer una sesión SSL para el proxy RPC. La RPC a través de HTTP v2 puede enviar todo el tráfico RPC a través de HTTP dentro de una sesión SSL; De forma predeterminada, v2 requiere que los datos se envíen dentro de una sesión SSL.
-   RPC a través de HTTP v1 no se puede autenticar en el proxy RPC. RPC a través de HTTP v2 se puede autenticar; De forma predeterminada, v2 requiere autenticación en el proxy RPC.
-   El proxy RPC v1 no funciona correctamente cuando la máquina IIS en la que está instalado forma parte de una granja de servidores web. El proxy RPC v2 funciona correctamente cuando la máquina IIS en la que está instalado forma parte de una granja de servidores web.

> [!Note]  
> Si Microsoft Internet Explorer está instalado en el equipo del programa cliente y el cliente no especifica un **HttpProxy** en su enlace de cadena, el código auxiliar del cliente RPC buscará en el registro del equipo cliente una entrada **HttpProxy.** Si encuentra una, usará el proxy especificado en la entrada del Registro.

 

Supongamos, por ejemplo, que el programa cliente debe conectarse a través de Internet a un servidor RPC en un equipo denominado Server7.microsoft.com. Además, suponga que el proxy RPC se ejecuta en Major7.microsoft.com. El programa de servidor RPC escucha el puerto 2225. El cliente usaría el enlace de cadena:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Si el proxy RPC puede resolver el nombre del servidor como Server7, sin necesidad de un nombre de dominio completo, también puede especificar:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Si la red cliente usa un firewall y un servidor proxy de Internet denominado myproxy y Internet Explorer en el cliente no está configurado para usar ese proxy, tendría que modificar el enlace de cadena del cliente a:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Esto dirige al cliente a conectarse al programa de servidor RPC en Server7.microsoft.com. Para ello, el cliente usará primero el puerto 80 (o el puerto 443 si se usa SSL) para conectarse a myproxy. Esto dará al programa cliente acceso a Internet. Con Internet, el programa cliente se conecta a continuación al proxy RPC en Major7.microsoft.com. El proxy RPC establecerá una conexión con el programa de servidor RPC que se ejecuta en Server7.microsoft.com.

Si la red cliente usa un firewall y no se puede acceder directamente al proxy RPC, para que una conexión se establezca más rápido, el enlace de cadena de cliente se puede modificar para:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption** permite dirigir el comportamiento de RPC al realizar conexiones HTTP. El **valor UseHttpProxy** indica a RPC que enruta su tráfico a través del proxy HTTP en todo momento, incluso cuando el cliente tiene sus opciones de Internet establecidas en Internet Explorer en "Omitir servidor proxy para direcciones locales". Esto hace que el cliente se conecte de forma forzar al proxy RPC a través del proxy HTTP. Esto acelera el tiempo para establecer una conexión, ya que omite cualquier retraso en la búsqueda del servidor RPC directamente antes de usar el proxy HTTP.

Si se usa la opción **HttpConnectionOption** y Internet Explorer en el cliente no está configurado para usar ese proxy HTTP, las conexiones pueden producir un error con **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS**.

La gran mayoría de los equipos de hoy en día están configurados para Exploración web. Por lo tanto, la mayoría de los clientes no necesitan especificar **HttpProxy**, ya que se recuperará de la configuración de conectividad a Internet.

 

 




