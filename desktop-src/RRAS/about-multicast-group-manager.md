---
title: Acerca del administrador de grupo de multidifusión
description: En esta documentación se describe la tecnología del administrador de grupos de multidifusión (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS de administrador de grupo de multidifusión
- RRAS de administrador de grupo de multidifusión, descrito
- RRAS del servicio de enrutamiento y acceso remoto, administrador de grupo de multidifusión
- RRAS del servicio de enrutamiento y acceso remoto, administrador de grupo de multidifusión, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676172"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="d75ce-107">Acerca del administrador de grupo de multidifusión</span><span class="sxs-lookup"><span data-stu-id="d75ce-107">About Multicast Group Manager</span></span>

<span data-ttu-id="d75ce-108">En esta documentación se describe la tecnología del administrador de grupos de multidifusión (MGM).</span><span class="sxs-lookup"><span data-stu-id="d75ce-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="d75ce-109">La multidifusión permite a un host enviar datos solo a los destinos que solicitan específicamente la recepción de los datos.</span><span class="sxs-lookup"><span data-stu-id="d75ce-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="d75ce-110">De esta manera, la multidifusión difiere del envío de datos de difusión, ya que los datos de difusión se envían a todos los hosts.</span><span class="sxs-lookup"><span data-stu-id="d75ce-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="d75ce-111">La multidifusión ahorra ancho de banda de red, ya que los datos de multidifusión solo los reciben los hosts que solicitan los datos, y los datos viajan solo una vez.</span><span class="sxs-lookup"><span data-stu-id="d75ce-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="d75ce-112">La multidifusión ahorra ancho de banda de servidor porque un servidor solo tiene que enviar un mensaje de multidifusión por red en lugar de un mensaje de unidifusión por receptor.</span><span class="sxs-lookup"><span data-stu-id="d75ce-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="d75ce-113">Ejemplos de aplicaciones de multidifusión populares son las reuniones en línea y la radio por Internet.</span><span class="sxs-lookup"><span data-stu-id="d75ce-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="d75ce-114">La API MGM permite a los desarrolladores escribir protocolos de enrutamiento de multidifusión que interoperan con los enrutadores que ejecutan el administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="d75ce-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="d75ce-115">Cuando se habilita más de un protocolo de enrutamiento de multidifusión en un enrutador, el administrador del grupo de multidifusión coordina las operaciones entre todos los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="d75ce-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="d75ce-116">El administrador del grupo de multidifusión informa a cada protocolo de enrutamiento cuando se producen cambios en la pertenencia a grupos y cuando se reciben datos de multidifusión procedentes de un nuevo origen o de un nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="d75ce-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="d75ce-117">La API MGM proporciona las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="d75ce-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="d75ce-118">Registro de protocolo</span><span class="sxs-lookup"><span data-stu-id="d75ce-118">Protocol registration</span></span>
-   <span data-ttu-id="d75ce-119">Administración de grupos</span><span class="sxs-lookup"><span data-stu-id="d75ce-119">Group management</span></span>
-   <span data-ttu-id="d75ce-120">Enumeración de entradas de reenvío de multidifusión (MFE)</span><span class="sxs-lookup"><span data-stu-id="d75ce-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="d75ce-121">Definiciones de devolución de llamada para los protocolos de enrutamiento de multidifusión</span><span class="sxs-lookup"><span data-stu-id="d75ce-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="d75ce-122">En esta información general se describen los componentes de la arquitectura de multidifusión, los escenarios de cliente que se usan para interoperar con el administrador de grupos de multidifusión y las consideraciones de programación para usar la API MGM.</span><span class="sxs-lookup"><span data-stu-id="d75ce-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




