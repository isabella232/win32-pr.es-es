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
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="02ca8-103">Usar RPC con el proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="02ca8-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="02ca8-104">El lanzamiento de Microsoft Internet Access Server incluía Winsock Proxy, una versión mejorada de la API de Windows Sockets, versión 1,1.</span><span class="sxs-lookup"><span data-stu-id="02ca8-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="02ca8-105">Winsock Proxy permite que una aplicación de Windows Sockets, que se ejecuta en un cliente de red privada, se comporte como si estuviera conectada directamente a una aplicación de servidor de Internet remoto.</span><span class="sxs-lookup"><span data-stu-id="02ca8-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="02ca8-106">El servidor proxy de Microsoft actúa como el host para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="02ca8-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="02ca8-107">Esto significa que todas las comunicaciones de nivel de aplicación se canalizan a través de un único equipo protegido: el equipo de puerta de enlace que ejecuta el servidor proxy de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="02ca8-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="02ca8-108">Normalmente, para las transferencias de paquetes de datagramas, la DLL de transporte RPC omite las funciones [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) y [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) proporcionadas en Wsock32.dll y se comunica directamente con el controlador de dispositivo subyacente.</span><span class="sxs-lookup"><span data-stu-id="02ca8-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="02ca8-109">Esto mejora la velocidad de las transferencias de paquetes, pero hace que las características de proxy Winsock no estén disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02ca8-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="02ca8-110">Cada proveedor de protocolo de red tiene un GUID asociado.</span><span class="sxs-lookup"><span data-stu-id="02ca8-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="02ca8-111">La biblioteca en tiempo de ejecución de RPC compara los GUID de UDP e IPX con los identificadores conocidos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="02ca8-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="02ca8-112">Si no coinciden, RPC utiliza automáticamente Winsock.</span><span class="sxs-lookup"><span data-stu-id="02ca8-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="02ca8-113">Otra característica del proxy Winsock es su capacidad de emular el protocolo de transporte TCP a través del transporte de Novell SPX cuando el equipo cliente SPX no tiene TCP instalado.</span><span class="sxs-lookup"><span data-stu-id="02ca8-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="02ca8-114">Para usar esta característica con las aplicaciones RPC, edite el registro del sistema en cada equipo cliente para agregar esta entrada:</span><span class="sxs-lookup"><span data-stu-id="02ca8-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

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

<span data-ttu-id="02ca8-115">Edite el registro en cada equipo servidor para agregar esta entrada:</span><span class="sxs-lookup"><span data-stu-id="02ca8-115">Edit the registry on each server computer to add this entry:</span></span>

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

<span data-ttu-id="02ca8-116">Para obtener más información acerca de los protocolos de transporte RPC, consulte [especificar secuencias de protocolos](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="02ca8-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="02ca8-117">Para obtener más información acerca del proxy Winsock, consulte la documentación del producto de Microsoft Internet Access Server.</span><span class="sxs-lookup"><span data-stu-id="02ca8-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="02ca8-118">Windows 2000 no implementa las entradas del registro **ClientProtocols** y **ServerProtocols** .</span><span class="sxs-lookup"><span data-stu-id="02ca8-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="02ca8-119">Microsoft proporciona todos los transportes bien conocidos como parte de la biblioteca en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="02ca8-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="02ca8-120">Por lo tanto, estas entradas no son necesarias.</span><span class="sxs-lookup"><span data-stu-id="02ca8-120">Therefore, these entries are not necessary.</span></span>

 

 