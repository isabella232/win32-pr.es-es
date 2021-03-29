---
title: Usar HTTP como transporte RPC
description: RPC a través de HTTP permite a los programas cliente utilizar Internet para ejecutar procedimientos proporcionados por programas de servidor en redes lejanas.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5860757a6c5df9937e77fc078df2526affb967fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486846"
---
# <a name="using-http-as-an-rpc-transport"></a>Usar HTTP como transporte RPC

RPC a través de HTTP permite a los programas cliente utilizar Internet para ejecutar procedimientos proporcionados por programas de servidor en redes lejanas. RPC a través de HTTP tuneliza sus llamadas a través de un puerto HTTP establecido. Por lo tanto, sus llamadas pueden cruzar los firewalls de red en las redes de cliente y de servidor.

RPC a través de HTTP enruta sus llamadas al proxy RPC ubicado en la red del servidor RPC. El proxy RPC establece y mantiene una conexión con el servidor RPC. Actúa como un proxy, enviando llamadas a procedimientos remotos al servidor RPC y enviando las respuestas del servidor a través de Internet a la aplicación cliente. Este proceso se ilustra en el diagrama siguiente.

![interacción entre un servidor RPC e Internet Information Server para RPC http](images/httprpc1.png)

El diagrama muestra un firewall en la red de la aplicación cliente. Esto no es necesario para que RPC a través de HTTP funcione. Sin embargo, si la red de cliente tiene un firewall, también necesitará un programa de servidor proxy como Microsoft Proxy Server.

Cuando el programa cliente emite una llamada a procedimiento remoto mediante HTTP como el transporte, la biblioteca en tiempo de ejecución de RPC en el cliente se pone en contacto con el proxy RPC. Dependiendo de si se pidió al cliente RPC que usara el puerto HTTP o HTTPS (HTTP con SSL) 80 o se usa el puerto 443, respectivamente. El proxy RPC se pone en contacto con el programa de servidor RPC y establece una conexión TCP/IP. El cliente y el proxy RPC mantienen su conexión HTTP o HTTPS a través de Internet. La conexión HTTP o HTTPS del cliente con el proxy RPC puede pasar a través de un firewall (sujeto a los permisos de acceso adecuados) si está presente. A continuación, el servidor puede ejecutar la llamada a procedimiento remoto y utilizar la conexión a través del proxy RPC para responder al cliente. El proxy RPC es una extensión ISAPI que se ejecuta en el contexto de IIS.

Si el cliente o el servidor se desconecta por cualquier motivo, el proxy RPC lo detectará y finalizará la sesión RPC. Siempre y cuando la sesión continúe, el proxy RPC mantendrá sus conexiones con el cliente y el servidor. Reenviará las llamadas de procedimiento remoto desde el cliente al servidor y enviará las respuestas del servidor al cliente.

El programa cliente RPC puede canalizar sus llamadas RPC a través de Internet mediante la creación de un enlace de cadena con el formato:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Donde:

-   *el \_ UUID del objeto* especifica un UUID del objeto RPC. Para obtener más información, vea generación de UUID de [interfaz](generating-interface-uuids.md) y [UUID de cadena](string-uuid.md).
-   **ncacn \_ http** selecciona la especificación de la secuencia de protocolos para RPC a través de http. Para obtener más información, vea [constantes de secuencia de protocolo](protocol-sequence-constants.md) y enlace de [cadenas](string-binding.md).
-   *el \_ servidor RPC* es la dirección de red del equipo que está ejecutando el proceso de servidor RPC. La dirección del servidor debe especificarse en un formato visible y comprensible para el equipo proxy RPC, no para el cliente. Dado que el cliente no se conecta directamente al servidor, no es necesario que pueda resolver el nombre del servidor o establecer una conexión con él. El proxy RPC establecerá la conexión en nombre del cliente y, por tanto, *el \_ servidor RPC* debe ser un nombre reconocible por el proxy RPC.
-   *Endpoint* especifica el puerto TCP/IP que escucha el proceso de servidor RPC para las llamadas a procedimientos remotos. Para obtener más información, vea [Buscar extremos](finding-endpoints.md).
-   **HttpProxy** especifica opcionalmente un servidor proxy http en la red del cliente RPC, como Microsoft Proxy Server. Si se selecciona un servidor proxy, no se especifica ningún número de puerto, el código auxiliar de RPC usa el puerto 80 de forma predeterminada si no se solicita SSL y el puerto 443 si se especifica SSL.
-   **RpcProxy** especifica la dirección y el número de puerto del equipo de IIS que actúa como proxy para el servidor RPC. Solo tiene que especificar esto si el proceso de servidor RPC reside en un equipo diferente del proxy RPC. Si no especifica un número de puerto, el código auxiliar de cliente RPC utiliza de forma predeterminada el puerto 80 si no se especifica SSL y utiliza el puerto 443 si se especifica SSL (HTTPS).
-   **HttpConnectionOption** opcionalmente permite dirigir el comportamiento de RPC al realizar conexiones http. El valor **UseHttpProxy** indica a RPC que enrute su tráfico a través del proxy http en todo momento, incluso cuando el cliente tiene establecidas las opciones de Internet en Internet Explorer para "omitir el servidor proxy para direcciones locales".

    Esta opción es compatible con Windows 7, Windows Server 2008 R2, Windows 8.1 y Windows Server 2012 R2 con KB2916915 instalado. Esta opción no se admite en Windows 8 y Windows Server 2012. Las aplicaciones pueden determinar si esta opción es compatible con el tiempo de ejecución de RPC comprobando el valor del registro **ConnectionOptionsFlag** situado en la siguiente clave del registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC**

    Si se establece el bit 0 (LSB) de este valor del registro, se admite esta opción específica; de lo contrario, esta opción no es compatible con el tiempo de ejecución de RPC en el sistema.

Para obtener más información sobre cómo crear enlaces de cadena, vea [enlazar y controlar](binding-and-handles.md).

El programa de servidor RPC puede aceptar llamadas RPC por túnel escuchando en la \_ secuencia del protocolo http ncacn.

Microsoft tiene dos implementaciones principales de RPC a través de HTTP: la versión 1 y la versión 2.

La versión 1 (llamada RPC a través de HTTP V1) se admite a través de Windows XP. La versión 1 del proxy RPC se admite a través de Windows 2000.

La versión 2 (llamada RPC a través de HTTP V2) es la versión actual.

Las dos versiones tienen capacidades diferentes y una interoperabilidad limitada. Aquí se proporciona un resumen de las diferencias. Para conocer las consideraciones de interoperabilidad, consulte [requisitos del sistema e interoperabilidad de RPC a través de http](system-requirements-and-interoperability-for-rpc-over-http.md).

-   RPC a través de HTTP v1 requiere que el protocolo de túnel SSL esté habilitado en todos los servidores proxy o firewalls HTTP entre el cliente RPC a través de HTTP y el proxy RPC. RPC a través de HTTP v1 intenta crear un túnel SSL a través del puerto 80 aunque los datos que envía no estén cifrados con SSL. Los servidores proxy y los firewalls suelen rechazar dichas solicitudes, a menos que se configure explícitamente para permitirlos. RPC a través de HTTP V2 no tiene este requisito.
-   RPC a través de HTTP v1 no puede establecer una sesión SSL en el proxy RPC. RPC a través de HTTP V2 puede enviar todo el tráfico de RPC a través de HTTP dentro de una sesión SSL; de forma predeterminada, V2 requiere que los datos se envíen en una sesión SSL.
-   RPC a través de HTTP v1 no se puede autenticar en el proxy RPC. RPC a través de HTTP V2 puede autenticarse; de forma predeterminada, V2 requiere autenticación en el proxy RPC.
-   El proxy RPC v1 no funciona correctamente cuando el equipo IIS en el que está instalado forma parte de una granja de servidores Web. El proxy RPC V2 funciona correctamente cuando el equipo IIS en el que está instalado forma parte de una granja de servidores Web.

> [!Note]  
> Si Microsoft Internet Explorer está instalado en el equipo del programa cliente y el cliente no especifica un **HttpProxy** en su enlace de cadena, el código auxiliar del cliente RPC buscará en el registro del equipo cliente una entrada **HttpProxy** . Si encuentra uno, usará el proxy especificado en la entrada del registro.

 

Supongamos, por ejemplo, que el programa cliente necesita conectarse a través de Internet a un servidor RPC en un equipo denominado Server7.microsoft.com. Además, supongamos que el proxy RPC se ejecuta en Major7.microsoft.com. El programa de servidor RPC escucha en el puerto 2225. El cliente usaría el enlace de cadenas:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Si el proxy RPC puede resolver el nombre del servidor como Server7, sin necesidad de un nombre de dominio completo, también puede especificar:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Si la red del cliente usa un firewall y un servidor proxy de Internet denominado mi proxy, e Internet Explorer en el cliente no está configurado para usar ese proxy, deberá modificar el enlace de cadenas del cliente a:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Esto indica al cliente que se conecte al programa de servidor RPC en Server7.microsoft.com. Para ello, el cliente usará primero el puerto 80 (o el puerto 443 si se usa SSL) para conectarse a mi proxy. Esto permitirá que el programa cliente tenga acceso a Internet. Mediante Internet, el programa cliente se conecta al proxy RPC en Major7.microsoft.com. El proxy RPC establecerá una conexión con el programa de servidor RPC que se ejecuta en Server7.microsoft.com.

Si la red del cliente usa un firewall y si no se puede tener acceso al proxy RPC directamente, para obtener una conexión establecida más rápido, el enlace de cadena del cliente se puede modificar para:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption** permite dirigir el comportamiento de RPC al realizar conexiones http. El valor **UseHttpProxy** indica a RPC que enrute su tráfico a través del proxy http en todo momento, incluso cuando el cliente tiene establecidas las opciones de Internet en Internet Explorer para "omitir el servidor proxy para direcciones locales". Esto indica al cliente que se conecte forzosamente al proxy RPC a través del proxy http. Esto acelera el tiempo de establecer una conexión, ya que omite cualquier retraso que busque el servidor RPC directamente antes de usar el proxy HTTP.

Si se usa la opción **HttpConnectionOption** e Internet Explorer en el cliente no está configurado para usar ese proxy http, pueden producirse errores en las conexiones con **\_ \_ \_ \_ las opciones de red no válidas de RPC**.

La gran mayoría de los equipos de hoy en día se configuran para la exploración Web. Por lo tanto, la mayoría de los clientes no necesitan especificar el **HttpProxy**, porque se recuperará de la configuración de conectividad a Internet.

 

 




