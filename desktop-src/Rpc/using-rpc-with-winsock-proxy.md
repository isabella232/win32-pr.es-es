---
title: Usar RPC con el proxy Winsock
description: Usar RPC con el proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078325"
---
# <a name="using-rpc-with-winsock-proxy"></a>Usar RPC con el proxy Winsock

El lanzamiento de Microsoft Internet Access Server incluía Winsock Proxy, una versión mejorada de la API de Windows Sockets, versión 1,1. Winsock Proxy permite que una aplicación de Windows Sockets, que se ejecuta en un cliente de red privada, se comporte como si estuviera conectada directamente a una aplicación de servidor de Internet remoto. El servidor proxy de Microsoft actúa como el host para esta conexión. Esto significa que todas las comunicaciones de nivel de aplicación se canalizan a través de un único equipo protegido: el equipo de puerta de enlace que ejecuta el servidor proxy de Microsoft.

Normalmente, para las transferencias de paquetes de datagramas, la DLL de transporte RPC omite las funciones [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) y [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) proporcionadas en Wsock32.dll y se comunica directamente con el controlador de dispositivo subyacente. Esto mejora la velocidad de las transferencias de paquetes, pero hace que las características de proxy Winsock no estén disponibles para la aplicación.

Cada proveedor de protocolo de red tiene un GUID asociado. La biblioteca en tiempo de ejecución de RPC compara los GUID de UDP e IPX con los identificadores conocidos de Microsoft. Si no coinciden, RPC utiliza automáticamente Winsock.

Otra característica del proxy Winsock es su capacidad de emular el protocolo de transporte TCP a través del transporte de Novell SPX cuando el equipo cliente SPX no tiene TCP instalado. Para usar esta característica con las aplicaciones RPC, edite el registro del sistema en cada equipo cliente para agregar esta entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Edite el registro en cada equipo servidor para agregar esta entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Para obtener más información acerca de los protocolos de transporte RPC, consulte [especificar secuencias de protocolos](specifying-protocol-sequences.md). Para obtener más información acerca del proxy Winsock, consulte la documentación del producto de Microsoft Internet Access Server.

Windows 2000 no implementa las entradas del registro **ClientProtocols** y **ServerProtocols** . Microsoft proporciona todos los transportes bien conocidos como parte de la biblioteca en tiempo de ejecución. Por lo tanto, estas entradas no son necesarias.

 

 