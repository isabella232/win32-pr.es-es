---
title: Interfaz (RRAS)
description: Una interfaz es una conexión lógica a una red. Cada interfaz se identifica mediante un índice único. Los protocolos de enrutamiento de multidifusión (como MOSPF) abordan todos los tipos de interfaces de forma similar.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995830"
---
# <a name="interface-rras"></a><span data-ttu-id="ab577-105">Interfaz (RRAS)</span><span class="sxs-lookup"><span data-stu-id="ab577-105">Interface (RRAS)</span></span>

<span data-ttu-id="ab577-106">Una interfaz es una conexión lógica a una red.</span><span class="sxs-lookup"><span data-stu-id="ab577-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="ab577-107">Cada interfaz se identifica mediante un índice único.</span><span class="sxs-lookup"><span data-stu-id="ab577-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="ab577-108">Los protocolos de enrutamiento de multidifusión (como MOSPF) abordan todos los tipos de interfaces de forma similar.</span><span class="sxs-lookup"><span data-stu-id="ab577-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="ab577-109">En el caso de una interfaz LAN, la interfaz corresponde a un dispositivo físico real del equipo (el adaptador de LAN).</span><span class="sxs-lookup"><span data-stu-id="ab577-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="ab577-110">En el caso de una interfaz WAN, la interfaz se asigna a un puerto cuando se establece una conexión.</span><span class="sxs-lookup"><span data-stu-id="ab577-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="ab577-111">Las interfaces WAN pueden basarse en túneles y el puerto puede ser un puerto de red privada virtual (VPN).</span><span class="sxs-lookup"><span data-stu-id="ab577-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="ab577-112">Los sistemas operativos Windows 2000 y versiones posteriores admiten una interfaz "Point-to-multipunto".</span><span class="sxs-lookup"><span data-stu-id="ab577-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="ab577-113">Este tipo de interfaz se puede ver como una colección de vínculos de punto a punto que comparten un único punto de finalización.</span><span class="sxs-lookup"><span data-stu-id="ab577-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="ab577-114">Para identificar de forma única un vínculo exacto en una interfaz de punto a multipunto, la API MGM usa la dirección del próximo salto del identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="ab577-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="ab577-115">Para admitir esta identificación, la API MGM usa un identificador de interfaz extendida, que incluye una dirección del [próximo salto](next-hop.md) .</span><span class="sxs-lookup"><span data-stu-id="ab577-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




