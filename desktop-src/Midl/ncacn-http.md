---
title: ncacn_http atributo)
description: La \_ palabra clave http ncacn identifica Microsoft Internet Information Server (IIS) como la familia de protocolos para el extremo.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790905"
---
# <a name="ncacn_http-attribute"></a>\_atributo http ncacn

La palabra clave **\_ http Ncacn** identifica Microsoft Internet Information Server (IIS) como la familia de protocolos para el extremo.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*\_servidor RPC* 
</dt> <dd>

La dirección de Internet o el nombre del equipo en el que se ejecuta el proceso del servidor RPC.

</dd> <dt>

*finales* 
</dt> <dd>

El puerto TCP/IP conocido (estático) en el que el proceso de servidor RPC está escuchando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La identificación de Microsoft Internet Information Server (IIS) como la familia de protocolos permite que las aplicaciones cliente y servidor se comuniquen a través de Internet mediante Microsoft Internet Information Server (IIS) como proxy. Dado que las llamadas se tunelizan a través de un puerto HTTP establecido, pueden atravesar firewalls.

Todas las aplicaciones de cliente y servidor RPC pueden admitir el protocolo **\_ http ncacn** siempre que se encuentren en la red de un servidor de Internet Information Server. IIS se pone en contacto con el servidor RPC y establece un socket TCP/IP, que mantiene para el cliente. IIS negocia una conexión TCP/IP con el servidor RPC y, una vez completada la negociación, actúa como proxy RPC y reenvía datos entre el socket TCP/IP del cliente y el socket TCP/IP del servidor. Cuando el proxy RPC de IIS detecta un cierre de sesión en el cliente o en el lado del servidor, cierra el socket restante.

La aplicación cliente utiliza implícitamente el enlace estático a IIS, pero el servidor puede utilizar extremos dinámicos, con la RPCSS del servidor (asignador de extremos) que resuelve el puerto del servidor RPC. Si IIS está en un equipo diferente que el servidor RPC, IIS recibe la llamada remota, Contacts RPCSS en el equipo del servidor RPC para obtener el extremo de proceso del servidor y, a continuación, reenvía la llamada al servidor RPC adecuado.

Si está instalado Internet Explorer, el transporte comprobará el registro para ver si hay una configuración para un proxy HTTP. Si existe un proxy, el transporte lo usará.

## <a name="examples"></a>Ejemplos

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 