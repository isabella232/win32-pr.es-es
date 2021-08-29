---
title: Uso de RPC con Winsock Proxy
description: Uso de RPC con Winsock Proxy
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc841cb1a3fdecf1f0493f27ef9224ec540dcebbbeaacdb7b287102a246c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010653"
---
# <a name="using-rpc-with-winsock-proxy"></a>Uso de RPC con Winsock Proxy

La versión de Microsoft Internet Access Server incluía Winsock Proxy, una versión mejorada de Windows Sockets API versión 1.1. Winsock Proxy permite que una aplicación Windows Sockets, que se ejecuta en un cliente de red privada, se comporte como si estuviera conectada directamente a una aplicación de servidor de Internet remota. El servidor proxy de Microsoft actúa como host para esta conexión. Esto significa que todas las comunicaciones de nivel de aplicación se canaliza a través de un único equipo protegido: el equipo de puerta de enlace que ejecuta Microsoft Proxy Server.

Normalmente, para las transferencias de paquetes de datagramas, el archivo DLL de transporte RPC omite las funciones [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) y [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) proporcionadas en Wsock32.dll y se comunica directamente con el controlador de dispositivo subyacente. Esto mejora la velocidad de las transferencias de paquetes, pero hace que las características del proxy winsock no estén disponibles para la aplicación.

Cada proveedor de protocolos de red debe tener un GUID asociado. La biblioteca en tiempo de ejecución de RPC compara los GUID UDP e IPX con los identificadores conocidos de Microsoft. Si no coinciden, RPC usa automáticamente Winsock.

Otra característica de Winsock Proxy es su capacidad para emular el protocolo de transporte TCP sobre el transporte de SpX de Kerberos cuando el equipo cliente de SPX no tiene TCP instalado. Para usar esta característica con aplicaciones RPC, edite el Registro del sistema en cada equipo cliente para agregar esta entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Edite el Registro en cada equipo servidor para agregar esta entrada:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Para obtener más información sobre los protocolos de transporte RPC, [vea Especificar secuencias de protocolo.](specifying-protocol-sequences.md) Para obtener más información sobre Winsock Proxy, consulte la documentación del producto para Microsoft Internet Access Server.

Windows 2000 no implementa las entradas del Registro **ClientProtocols** y **ServerProtocols.** Microsoft proporciona todos los transportes conocidos como parte de la biblioteca en tiempo de ejecución. Por lo tanto, estas entradas no son necesarias.

 

 