---
title: Aplicación del nivel de aplicación (ALE)
description: ALE es un conjunto de niveles de modo kernel de la plataforma de filtrado de Windows (WFP) que se usan para el filtrado con estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420666"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="0aef4-103">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="0aef4-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="0aef4-104">ALE es un conjunto de niveles de modo kernel de la plataforma de filtrado de Windows (WFP) que se usan para el filtrado con estado.</span><span class="sxs-lookup"><span data-stu-id="0aef4-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="0aef4-105">El filtrado con estado realiza un seguimiento del estado de las conexiones de red y solo permite los paquetes que coinciden con un estado de conexión conocido.</span><span class="sxs-lookup"><span data-stu-id="0aef4-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="0aef4-106">Por ejemplo, el filtrado con estado para una conexión TCP iniciada desde detrás de un Firewall puede permitir que solo los paquetes entrantes que coincidan con los paquetes salientes anteriores enviados por la entidad protegida.</span><span class="sxs-lookup"><span data-stu-id="0aef4-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="0aef4-107">Los filtros de las capas ALE autorizan la creación de conexiones entrantes y salientes, las asignaciones de puerto, las operaciones de socket como [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la creación de sockets sin formato y la recepción en modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="0aef4-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="0aef4-108">El tráfico que se encuentra en los niveles de ALE se clasifica en función de la conexión o del socket.</span><span class="sxs-lookup"><span data-stu-id="0aef4-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="0aef4-109">En las capas que no son ALE, los filtros solo pueden clasificar el tráfico por paquete.</span><span class="sxs-lookup"><span data-stu-id="0aef4-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="0aef4-110">Los niveles ALE son los únicos niveles de WFP en los que se puede filtrar el tráfico de red en función de la identidad de la aplicación, mediante un nombre de archivo normalizado, y según la identidad del usuario, mediante un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0aef4-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="0aef4-111">(Consulte FLT \_ \_Información sobre \_ el nombre de archivo en la documentación del kit de controladores de Windows (WDK), para obtener más información sobre los nombres de archivo normalizados.</span><span class="sxs-lookup"><span data-stu-id="0aef4-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="0aef4-112">Además, cuando se usa IPsec para proteger la conexión, el filtrado en las capas de ALE también puede realizarse en la identidad del equipo remoto y en la identidad del usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="0aef4-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="0aef4-113">Las identidades de usuario y equipo remoto se obtienen a partir de las credenciales usadas en la creación de una sesión de IPsec.</span><span class="sxs-lookup"><span data-stu-id="0aef4-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="0aef4-114">Por este motivo, las directivas que aplican quién (por ejemplo, "administrador") o la aplicación (por ejemplo, "Internet Explorer") pueden realizar las operaciones de red mencionadas anteriormente se crean en los niveles de ALE.</span><span class="sxs-lookup"><span data-stu-id="0aef4-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="0aef4-115">ALE permite el cumplimiento de directivas como "permitir que Windows Messenger todo el acceso a la red mientras se bloquea el resto de las aplicaciones".</span><span class="sxs-lookup"><span data-stu-id="0aef4-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="0aef4-116">En este ejemplo, cuando la aplicación "Messenger" se conecta a través de la red, ALE captura el evento, determina que se inició mediante Messenger y consulta el motor de filtros de WFP para determinar si se debe permitir que el socket continúe.</span><span class="sxs-lookup"><span data-stu-id="0aef4-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="0aef4-117">Debido a la naturaleza de los verdaderos sockets de dos IP, es posible que no se produzcan clasificaciones en la capa de ALE de IPv4.</span><span class="sxs-lookup"><span data-stu-id="0aef4-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="0aef4-118">Esto es así por diseño, ya que para todos los fines y propósitos, el socket es un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="0aef4-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="0aef4-119">Para ver el tráfico V4 para este tipo de socket, cree filtros en la capa V6 mediante la dirección asignada por IPv6.</span><span class="sxs-lookup"><span data-stu-id="0aef4-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0aef4-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aef4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aef4-121">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="0aef4-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="0aef4-122">Filtrado con estado ALE</span><span class="sxs-lookup"><span data-stu-id="0aef4-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="0aef4-123">Tráfico de multidifusión/difusión ALE</span><span class="sxs-lookup"><span data-stu-id="0aef4-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="0aef4-124">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="0aef4-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="0aef4-125">Personalización del flujo ALE</span><span class="sxs-lookup"><span data-stu-id="0aef4-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 