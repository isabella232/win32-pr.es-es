---
title: Acerca de la API de Network List Manager
description: Acerca de la API de Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779123"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="73a75-103">Acerca de la API de Network List Manager</span><span class="sxs-lookup"><span data-stu-id="73a75-103">About the Network List Manager API</span></span>

<span data-ttu-id="73a75-104">El entorno de red de Microsoft Windows permite que los equipos de host múltiple se conecten a varias redes simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="73a75-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="73a75-105">Puede haber varias redes inalámbricas disponibles junto con las conexiones LAN y de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="73a75-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="73a75-106">Network List Manager identifica las redes disponibles y devuelve datos de atributos de red a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73a75-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="73a75-107">La API del administrador de lista de redes interactúa con el servicio Administrador de lista de redes para identificar y recuperar las propiedades de cada red a la que se conecta el equipo.</span><span class="sxs-lookup"><span data-stu-id="73a75-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="73a75-108">Cada red se identifica de forma exclusiva con una firma de red basada en las propiedades de identificación única de esa red.</span><span class="sxs-lookup"><span data-stu-id="73a75-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="73a75-109">Cuando una aplicación se registra para las notificaciones del administrador de la lista de redes, la aplicación recibe notificaciones sobre la disponibilidad de nuevas conexiones de red o cambios en las conexiones de red existentes.</span><span class="sxs-lookup"><span data-stu-id="73a75-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="73a75-110">Las aplicaciones pueden ajustar su lógica según: la red a la que están conectadas. la conexión de red a la que están conectadas; o cuáles son las propiedades de red.</span><span class="sxs-lookup"><span data-stu-id="73a75-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="73a75-111">Con esta información, las aplicaciones pueden ajustar sus acciones en función de las condiciones de la red actual.</span><span class="sxs-lookup"><span data-stu-id="73a75-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="73a75-112">Windows Vista presenta nuevas interfaces que se pueden usar para obtener información detallada sobre estas características de red y mucho más.</span><span class="sxs-lookup"><span data-stu-id="73a75-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="73a75-113">Con la interfaz [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) es fácil enumerar todas las redes ([**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) que un equipo ha visto alguna vez, o simplemente las redes conectadas o simplemente las redes desconectadas.</span><span class="sxs-lookup"><span data-stu-id="73a75-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="73a75-114">La interfaz **INetworkListManager** también facilita la enumeración de las interfaces de red en un equipo.</span><span class="sxs-lookup"><span data-stu-id="73a75-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="73a75-115">La interfaz [**inetss**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) se usa para determinar las propiedades de una conexión de red: nombre, descripción, identificador, administrado/autenticado, conectado/desconectado, etc.</span><span class="sxs-lookup"><span data-stu-id="73a75-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="73a75-116">Es posible que una red única esté conectada a varias interfaces, por lo que a través de una interfaz de **inet** de usuario también puede enumerar las instancias de la interfaz de usuario de **inet** que se está usando.</span><span class="sxs-lookup"><span data-stu-id="73a75-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="73a75-117">La interfaz de [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) out le indica las propiedades pertinentes de una interfaz: identificador, GUID, tipo (administrado, autenticado) y estado (conectado, desconectado, V4 local, V4 Internet, V6 local, V6 Internet).</span><span class="sxs-lookup"><span data-stu-id="73a75-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="73a75-118">V4 local significa acceso local del Protocolo de Internet versión 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="73a75-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="73a75-119">Internet v4 significa IPv4 con acceso a Internet.</span><span class="sxs-lookup"><span data-stu-id="73a75-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="73a75-120">IPv6 local V6 y V6 de Internet: IPv6.</span><span class="sxs-lookup"><span data-stu-id="73a75-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="73a75-121">La raíz del árbol de objetos de la ubicación de red es la interfaz [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) .</span><span class="sxs-lookup"><span data-stu-id="73a75-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="73a75-122">Esta interfaz se implementa en la coclase **CLSID \_ NetworkListManager** .</span><span class="sxs-lookup"><span data-stu-id="73a75-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="73a75-123">Para usar esta interfaz, es necesario crear el objeto com NetworkListManager de **CLSID \_** como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="73a75-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




