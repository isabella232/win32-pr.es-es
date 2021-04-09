---
title: Servidores proxy y WinRM
description: Administración remota de Windows (WinRM) usa HTTP y HTTPS para enviar mensajes entre los equipos cliente y servidor. En general, el cliente WinRM envía mensajes directamente al servidor WinRM. Los clientes de WinRM también se pueden configurar para usar un servidor proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07bbfebb4c8f0eb9e77a8942d54677b55c60006
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791698"
---
# <a name="proxy-servers-and-winrm"></a>Servidores proxy y WinRM

Administración remota de Windows (WinRM) usa HTTP y HTTPS para enviar mensajes entre los equipos cliente y servidor. En general, el cliente WinRM envía mensajes directamente al servidor WinRM. Los clientes de WinRM también se pueden configurar para usar un servidor proxy.

Para obtener más información, consulte las secciones siguientes:

-   [Configuración de un servidor proxy para WinRM 2,0](#configuring-a-proxy-server-for-winrm-20)
    -   [Conexiones proxy basadas en HTTPS](#https-based-proxy-connections)
    -   [Conexiones proxy basadas en HTTP](#http-based-proxy-connections)
-   [Configuración de un servidor proxy para WinRM 1,1 y versiones anteriores](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configuración de un servidor proxy para WinRM 2,0

WinRM 2,0 admite una amplia gama de configuraciones de proxy. Por ejemplo, WinRM admite servidores proxy para transportes HTTP y HTTPS, así como para servidores proxy autenticados y no autenticados.

### <a name="https-based-proxy-connections"></a>Conexiones proxy HTTPS-Based

Para mejorar la seguridad y la afinidad basada en la conexión, se debe usar HTTPS como mecanismo de transporte.

Si el servidor proxy requiere autenticación, los clientes y servidores de WinRM deben usar HTTPS.

> [!Note]  
> La autenticación en el servidor proxy es independiente de la autenticación en el servidor de destino.

 

### <a name="http-based-proxy-connections"></a>Conexiones proxy HTTP-Based

Si no se requiere autenticación del servidor proxy, se puede usar HTTP o HTTPs para el transporte. Sin embargo, las conexiones basadas en HTTP desde un cliente WinRM a un servidor WinRM a través de un servidor proxy pueden ser problemáticas.

Pueden surgir los siguientes problemas al usar conexiones basadas en HTTP:

-   El servidor proxy no admite la autenticación basada en conexión, lo que puede provocar que se produzca un error de acceso denegado en la autenticación en el servidor de destino.
-   Se necesita más de un conjunto de credenciales para conectarse al servidor de destino y al servidor proxy.
-   Es posible que los servidores proxy basados en HTTP no admitan la capacidad de mantener las conexiones basadas en el cliente y en el servidor asociadas. Si el proxy no vincula de un cliente a un servidor y mantiene la conexión TCP/IP, es posible que los clientes no autenticados obtengan acceso a los datos. Además, la falta de afinidad de conexión podría provocar un error de autenticación en el servidor.

Si se debe usar HTTP como el transporte, el servidor proxy debe admitir la configuración siguiente para lograr una respuesta de WinRM mejor y evitar errores de acceso denegado para los clientes de WinRM:

-   Compatibilidad con HTTP/1.1. HTTP/1.1 es más estricto en la asignación de afinidad de conexión entre el cliente y el servidor.
-   Autenticación basada en conexión para la autenticación Negotiate, Kerberos y CredSSP.

    La autenticación de una solicitud requiere varios recorridos de ida y vuelta entre el cliente y el servidor. La mayor parte de la negociación de la autenticación se completa después de que el servidor de autenticación (WinRM) envía una respuesta al cliente que no es una respuesta 401 (no autorizado). Si el servidor WinRM devuelve una respuesta al cliente que no es una respuesta 401, el proxy no debe cerrar la conexión.

    Se pueden enviar varios pares de solicitud/respuesta entre el cliente y el servidor antes de que se envíen los datos del paquete real. WinRM 2,0 usa los esquemas de autenticación Negotiate y Kerberos con cifrado, que puede Agregar viajes de ida y vuelta adicionales. No se pueden enviar datos al servidor hasta que se complete la autenticación.

    El servidor WinRM devuelve una respuesta de nivel 200 que indica que se ha completado la autenticación. Los servidores proxy basados en HTTP pueden finalizar la afinidad de autenticación basada en conexión y cerrar la conexión TCP/IP después de recibir la respuesta de nivel 200 desde el servidor WinRM. El recorrido de ida y vuelta final del cliente al servidor no incluye el paquete de solicitud original. Si el servidor proxy cierra la conexión, el servidor intentará volver a autenticar el cliente y la solicitud del cliente nunca se puede enviar al servidor. Si no se mantiene la afinidad basada en conexión, se puede producir un error de acceso denegado en la autenticación con el servidor de destino.

-   Persistencia de la conexión. La conexión TCP/IP del cliente con el proxy debe seguir asignando a la misma conexión TCP/IP desde el proxy al servidor. Mantener esta conexión ayuda a lograr un mayor nivel de rendimiento. Si no se mantiene la conexión, se debe volver a autenticar cada solicitud, lo que puede afectar al rendimiento.

### <a name="encryption-and-winrm-20"></a>Cifrado e WinRM 2,0

WinRM 2,0 admite el cifrado a través de HTTP mediante los esquemas de autenticación Negotiate, Kerberos y CredSSP. Si un servidor WinRM admite HTTP y se obtiene acceso a él a través de un proxy, el servidor WinRM debe aplicar el cifrado y no permitir el tráfico de red no cifrado.

En ningún caso, se deben enviar solicitudes HTTP sin cifrar a través de servidores proxy. Cuando los datos deben pasar a través de un servidor proxy antes de enviarse al servidor de destino, son muy importantes los siguientes problemas de seguridad:

-   Es posible que un servidor proxy malintencionado examine cada par solicitud-respuesta, incluidas las credenciales.
-   Si las conexiones TCP/IP no se asignan de forma segura entre el cliente WinRM y el servidor proxy y entre el servidor proxy y el servidor de destino, un cliente no autorizado podría conectarse al servidor de destino utilizando la misma conexión autenticada del servidor proxy con el servidor de destino. El servidor de destino podría permitir el acceso del cliente no autenticado a los datos. Si se aplica el cifrado, el servidor de destino envía un mensaje de acceso denegado al cliente no autenticado.

El uso del cifrado mitigaría estos posibles problemas de seguridad.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configuración de un servidor proxy para WinRM 1,1 y versiones anteriores

Si se requiere un proxy para llegar al servidor WinRM, el cliente WinRM se basa en la configuración del proxy de servicios HTTP de Windows (WinHTTP). De forma predeterminada, WinHTTP no está configurado para usar un servidor proxy. La configuración del proxy WinHTTP se puede cambiar mediante las utilidades de línea de comandos [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) o [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) .

**WinRM 1,1 y versiones anteriores:** WinRM no utiliza la configuración de proxy de Internet Explorer.

 

 