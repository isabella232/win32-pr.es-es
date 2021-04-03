---
title: Cliente del administrador de grupo de multidifusión
description: Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779602"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="15c87-103">Cliente del administrador de grupo de multidifusión</span><span class="sxs-lookup"><span data-stu-id="15c87-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="15c87-104">Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.</span><span class="sxs-lookup"><span data-stu-id="15c87-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="15c87-105">La API MGM la usan principalmente los protocolos de enrutamiento de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="15c87-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="15c87-106">Los desarrolladores de protocolos de enrutamiento de multidifusión usan la API MGM para:</span><span class="sxs-lookup"><span data-stu-id="15c87-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="15c87-107">Mantener la pertenencia a grupos</span><span class="sxs-lookup"><span data-stu-id="15c87-107">Maintain group membership</span></span>
-   <span data-ttu-id="15c87-108">Controlar la propiedad de la interfaz</span><span class="sxs-lookup"><span data-stu-id="15c87-108">Control interface ownership</span></span>
-   <span data-ttu-id="15c87-109">Recibir notificaciones del administrador del grupo de multidifusión con respecto a otras solicitudes de protocolos de enrutamiento de multidifusión para datos de multidifusión</span><span class="sxs-lookup"><span data-stu-id="15c87-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="15c87-110">Las aplicaciones administrativas específicas que deben supervisar entradas de reenvío de multidifusión (MFEs) pueden hacerlo sin agregar ni quitar la pertenencia a grupos.</span><span class="sxs-lookup"><span data-stu-id="15c87-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="15c87-111">Los desarrolladores de aplicaciones administrativas usan funciones MGM específicas para revisar la información en MFEs.</span><span class="sxs-lookup"><span data-stu-id="15c87-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="15c87-112">Los protocolos de enrutamiento de multidifusión también tienen acceso a MFEs.</span><span class="sxs-lookup"><span data-stu-id="15c87-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="15c87-113">Un MFE es la información de reenvío que el administrador del grupo de multidifusión crea en función de la pertenencia a grupos.</span><span class="sxs-lookup"><span data-stu-id="15c87-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="15c87-114">Los MFEs que se recuperan del administrador del grupo de multidifusión pueden proporcionar información estadística.</span><span class="sxs-lookup"><span data-stu-id="15c87-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="15c87-115">Una aplicación administrativa puede usar esta información para determinar las acciones adecuadas.</span><span class="sxs-lookup"><span data-stu-id="15c87-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="15c87-116">Por ejemplo, una aplicación administrativa podría realizar acciones basadas en el volumen de paquetes de una interfaz específica.</span><span class="sxs-lookup"><span data-stu-id="15c87-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




