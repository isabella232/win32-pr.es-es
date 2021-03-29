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
# <a name="ncacn_http-attribute"></a><span data-ttu-id="8882c-104">\_atributo http ncacn</span><span class="sxs-lookup"><span data-stu-id="8882c-104">ncacn\_http attribute</span></span>

<span data-ttu-id="8882c-105">La palabra clave **\_ http Ncacn** identifica Microsoft Internet Information Server (IIS) como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="8882c-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="8882c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8882c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8882c-107">*\_servidor RPC*</span><span class="sxs-lookup"><span data-stu-id="8882c-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="8882c-108">La dirección de Internet o el nombre del equipo en el que se ejecuta el proceso del servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="8882c-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="8882c-109">*finales*</span><span class="sxs-lookup"><span data-stu-id="8882c-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="8882c-110">El puerto TCP/IP conocido (estático) en el que el proceso de servidor RPC está escuchando.</span><span class="sxs-lookup"><span data-stu-id="8882c-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8882c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8882c-111">Remarks</span></span>

<span data-ttu-id="8882c-112">La identificación de Microsoft Internet Information Server (IIS) como la familia de protocolos permite que las aplicaciones cliente y servidor se comuniquen a través de Internet mediante Microsoft Internet Information Server (IIS) como proxy.</span><span class="sxs-lookup"><span data-stu-id="8882c-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="8882c-113">Dado que las llamadas se tunelizan a través de un puerto HTTP establecido, pueden atravesar firewalls.</span><span class="sxs-lookup"><span data-stu-id="8882c-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="8882c-114">Todas las aplicaciones de cliente y servidor RPC pueden admitir el protocolo **\_ http ncacn** siempre que se encuentren en la red de un servidor de Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="8882c-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="8882c-115">IIS se pone en contacto con el servidor RPC y establece un socket TCP/IP, que mantiene para el cliente.</span><span class="sxs-lookup"><span data-stu-id="8882c-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="8882c-116">IIS negocia una conexión TCP/IP con el servidor RPC y, una vez completada la negociación, actúa como proxy RPC y reenvía datos entre el socket TCP/IP del cliente y el socket TCP/IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="8882c-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="8882c-117">Cuando el proxy RPC de IIS detecta un cierre de sesión en el cliente o en el lado del servidor, cierra el socket restante.</span><span class="sxs-lookup"><span data-stu-id="8882c-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="8882c-118">La aplicación cliente utiliza implícitamente el enlace estático a IIS, pero el servidor puede utilizar extremos dinámicos, con la RPCSS del servidor (asignador de extremos) que resuelve el puerto del servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="8882c-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="8882c-119">Si IIS está en un equipo diferente que el servidor RPC, IIS recibe la llamada remota, Contacts RPCSS en el equipo del servidor RPC para obtener el extremo de proceso del servidor y, a continuación, reenvía la llamada al servidor RPC adecuado.</span><span class="sxs-lookup"><span data-stu-id="8882c-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="8882c-120">Si está instalado Internet Explorer, el transporte comprobará el registro para ver si hay una configuración para un proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="8882c-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="8882c-121">Si existe un proxy, el transporte lo usará.</span><span class="sxs-lookup"><span data-stu-id="8882c-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="8882c-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8882c-122">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="8882c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8882c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8882c-124">**finales**</span><span class="sxs-lookup"><span data-stu-id="8882c-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="8882c-125">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="8882c-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8882c-126">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="8882c-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 