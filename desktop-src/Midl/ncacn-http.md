---
title: ncacn_http atributo
description: La palabra clave http ncacn \_ identifica Microsoft Internet Information Server (IIS) como la familia de protocolos para el punto de conexión.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7eed41849f59e497000e9ad56ae7c3166cf2d0212986fa9ba5f5ea910ed364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642216"
---
# <a name="ncacn_http-attribute"></a>Atributo http ncacn \_

La **palabra clave \_ http ncacn** identifica Microsoft Internet Information Server (IIS) como la familia de protocolos para el punto de conexión.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*servidor \_ rpc* 
</dt> <dd>

La dirección de Internet o el nombre de la máquina en la que se ejecuta el proceso de servidor RPC.

</dd> <dt>

*endpoint* 
</dt> <dd>

Puerto TCP/IP conocido (estático) en el que escucha el proceso del servidor RPC.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La identificación de Microsoft Internet Information Server (IIS) como familia de protocolos permite que las aplicaciones cliente y servidor se comuniquen a través de Internet mediante Microsoft Internet Information Server (IIS) como proxy. Dado que las llamadas se tunelización a través de un puerto HTTP establecido, pueden cruzar firewalls.

Cualquier aplicación cliente y servidor RPC puede admitir el protocolo **\_ http ncacn** siempre y cuando estén en red a un servidor de Internet Information Server. IIS se pone en contacto con el servidor RPC y establece un socket TCP/IP, que mantiene para el cliente. IIS negocia una conexión TCP/IP con el servidor RPC y, una vez completada la negociación, actúa como proxy RPC, reenviando datos entre el socket TCP/IP del lado cliente y el socket TCP/IP del lado servidor. Cuando el proxy RPC de IIS detecta un cierre de sesión en el cliente o en el lado servidor, cierra el socket restante.

La aplicación cliente usa implícitamente el enlace estático a IIS, pero el servidor puede usar puntos de conexión dinámicos, con el RPCSS del servidor (asignador de puntos de conexión) resolviendo el puerto del servidor RPC. Si IIS está en un equipo diferente al servidor RPC, recibe la llamada remota, se pone en contacto con RPCSS en el equipo del servidor RPC para obtener el punto de conexión de proceso del servidor y, a continuación, reenvía la llamada al servidor RPC adecuado.

Si Internet Explorer está instalado, el transporte comprobará el Registro para ver si hay una configuración para un proxy HTTP. Si existe un proxy, el transporte lo usará.

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

[**Extremo**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 