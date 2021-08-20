---
title: Servidores proxy y WinRM
description: Windows Administración remota (WinRM) usa HTTP y HTTPS para enviar mensajes entre los equipos cliente y servidor. En general, el cliente winRM envía mensajes directamente al servidor WinRM. Los clientes winRM también se pueden configurar para usar un servidor proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663493f9c3e71e44be000f436ad4573f911652a8e142b77ffab41acbff250b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112943"
---
# <a name="proxy-servers-and-winrm"></a>Servidores proxy y WinRM

Windows Administración remota (WinRM) usa HTTP y HTTPS para enviar mensajes entre los equipos cliente y servidor. En general, el cliente winRM envía mensajes directamente al servidor WinRM. Los clientes winRM también se pueden configurar para usar un servidor proxy.

Para obtener más información, consulte las secciones siguientes:

-   [Configuración de un servidor proxy para WinRM 2.0](#configuring-a-proxy-server-for-winrm-20)
    -   [Conexiones de proxy basadas en HTTPS](#https-based-proxy-connections)
    -   [Conexiones de proxy basadas en HTTP](#http-based-proxy-connections)
-   [Configuración de un servidor proxy para WinRM 1.1 y versiones anteriores](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configuración de un servidor proxy para WinRM 2.0

WinRM 2.0 admite una amplia gama de configuraciones de proxy. Por ejemplo, WinRM admite servidores proxy para transportes HTTP y HTTPS y para servidores proxy autenticados y no autenticados.

### <a name="https-based-proxy-connections"></a>HTTPS-Based proxy de conexión

Para mejorar la seguridad y la afinidad basada en conexiones, se debe usar HTTPS como mecanismo de transporte.

Si el servidor proxy requiere autenticación, los clientes y servidores WinRM deben usar HTTPS.

> [!Note]  
> La autenticación en el servidor proxy es independiente de la autenticación en el servidor de destino.

 

### <a name="http-based-proxy-connections"></a>HTTP-Based proxy de conexión

Si no se requiere autenticación de servidor proxy, se puede usar HTTP o HTTPs para el transporte. Sin embargo, las conexiones basadas en HTTP desde un cliente WinRM a un servidor WinRM a través de un servidor proxy pueden ser problemáticas.

Se pueden encontrar los siguientes problemas al usar conexiones basadas en HTTP:

-   El servidor proxy no admite la autenticación basada en conexiones, lo que puede provocar un error de acceso denegado en la autenticación en el servidor de destino.
-   Se necesita más de un conjunto de credenciales para conectarse al servidor de destino y al servidor proxy.
-   Es posible que los servidores proxy basados en HTTP no admitan la capacidad de mantener las conexiones basadas en cliente y basadas en servidor asociadas. Si el proxy no vincula fuertemente un cliente a un servidor y mantiene la conexión TCP/IP, es posible que los clientes no autenticados obtengan acceso a los datos. Además, la falta de afinidad de conexión podría provocar un error en la autenticación en el servidor.

Si se debe usar HTTP como transporte, el servidor proxy debe admitir la siguiente configuración para lograr una mejor respuesta de WinRM y evitar errores de acceso denegado para los clientes winRM:

-   Compatibilidad con HTTP/1.1. HTTP/1.1 es más estricto en la asignación de afinidad de conexión entre cliente y servidor.
-   Autenticación basada en conexiones para la autenticación Negotiate, Kerberos y CredSSP.

    La autenticación de una solicitud requiere varios recorridos de ida y vuelta entre el cliente y el servidor. La mayor parte de la negociación para la autenticación se completa después de que el servidor de autenticación (WinRM) envíe una respuesta al cliente que no sea una respuesta 401 (No autorizado). Si el servidor WinRM devuelve una respuesta al cliente que no es una respuesta 401, el proxy no debe cerrar la conexión.

    Se pueden enviar varios pares de solicitud/respuesta entre el cliente y el servidor antes de que se envíen los datos reales del paquete. WinRM 2.0 usa los esquemas de autenticación Negotiate y Kerberos con cifrado, que pueden agregar recorridos de ida y vuelta adicionales. Los datos no se pueden enviar al servidor hasta que se complete la autenticación.

    El servidor WinRM devuelve una respuesta de 200 niveles que indica que la autenticación se ha completado. Los servidores proxy basados en HTTP podrían finalizar la afinidad de autenticación basada en conexiones y cerrar la conexión TCP/IP después de recibir la respuesta de nivel 200 del servidor WinRM. El último recorrido de ida y vuelta del cliente al servidor no incluye el paquete de solicitud original. Si el servidor proxy cierra la conexión, el servidor intentará volver a autenticar el cliente y es posible que la solicitud de cliente nunca se envíe al servidor. Si no se mantiene la afinidad basada en la conexión, la autenticación en el servidor de destino puede producir un error de acceso denegado.

-   Persistencia de la conexión. La conexión TCP/IP del cliente al proxy debe seguir asignando a la misma conexión TCP/IP desde el proxy al servidor. Mantener esta conexión ayuda a lograr un mayor nivel de rendimiento. Si no se mantiene la conexión, todas las solicitudes se deben volver a autenticar, lo que podría afectar al rendimiento.

### <a name="encryption-and-winrm-20"></a>Cifrado y WinRM 2.0

WinRM 2.0 admite el cifrado a través de HTTP mediante los esquemas de autenticación Negotiate, Kerberos y CredSSP. Si un servidor WinRM admite HTTP y se accede a través de un proxy, el servidor WinRM debe aplicar el cifrado y no permitir el tráfico de red sin cifrar.

En ningún caso, las solicitudes HTTP sin cifrar se deben enviar a través de servidores proxy. Cuando los datos deben pasar a través de un servidor proxy antes de enviarse al servidor de destino, los siguientes problemas de seguridad son muy importantes:

-   Es posible que un servidor proxy malintencionado pueda examinar cada par de solicitud/respuesta, incluidas las credenciales.
-   Si las conexiones TCP/IP no están fuertemente asignadas entre el cliente WinRM y el servidor proxy y entre el servidor proxy y el servidor de destino, un cliente no autorizado podría conectarse al servidor de destino mediante la misma conexión autenticada desde el servidor proxy al servidor de destino. El servidor de destino podría permitir el acceso de cliente no autenticado a los datos. Si se aplica el cifrado, el servidor de destino envía un mensaje de acceso denegado al cliente no autenticado.

El uso del cifrado mitigaría estos posibles problemas de seguridad.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configuración de un servidor proxy para WinRM 1.1 y versiones anteriores

Si se requiere un proxy para llegar al servidor WinRM, el cliente de WinRM se basa en la configuración de proxy Windows servicios HTTP (WinHTTP). De forma predeterminada, WinHTTP no está configurado para usar un servidor proxy. La configuración del proxy WinHTTP se puede cambiar mediante las [ utilidadesProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) o [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) de la línea de comandos.

**WinRM 1.1 y versiones anteriores:** WinRM no usa la configuración Internet Explorer proxy.

 

 