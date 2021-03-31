---
description: La API de la tabla de enrutamiento distribuida (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: Table API de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082659"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="088f4-103">Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="088f4-103">Distributed Routing Table API</span></span>

<span data-ttu-id="088f4-104">La API de la tabla de enrutamiento distribuida (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="088f4-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="088f4-105">Una aplicación que usa DRT puede realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="088f4-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="088f4-106">Cree tablas de enrutamiento distribuido específicas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="088f4-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="088f4-107">Registrar claves y asociarlas con direcciones IP y datos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="088f4-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="088f4-108">Busque claves y recupere las direcciones IP y los datos de aplicación asociados a ellas.</span><span class="sxs-lookup"><span data-stu-id="088f4-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="088f4-109">Esta funcionalidad se puede usar para crear tablas de hash distribuidas (DHTs), sistemas de resolución de nombres sin servidor y redes de malla superpuestas de muchas topologías.</span><span class="sxs-lookup"><span data-stu-id="088f4-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="088f4-110">Los administradores y los usuarios de aplicaciones habilitadas para DRT deben tener en cuenta la información que se publica en los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="088f4-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="088f4-111">Los servidores de Microsoft no se emplean en esta tecnología y la información no se envía a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="088f4-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="088f4-112">La documentación proporcionada para esta API se divide en tres secciones.</span><span class="sxs-lookup"><span data-stu-id="088f4-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="088f4-113">Sección</span><span class="sxs-lookup"><span data-stu-id="088f4-113">Section</span></span>                                                                                | <span data-ttu-id="088f4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="088f4-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="088f4-115">Acerca de las tablas de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="088f4-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="088f4-116">Información que detalla el ciclo de vida y los cambios de estado de la API de DRT.</span><span class="sxs-lookup"><span data-stu-id="088f4-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="088f4-117">Usar el Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="088f4-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="088f4-118">Información que detalla el uso general de la API de DRT.</span><span class="sxs-lookup"><span data-stu-id="088f4-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="088f4-119">Referencia de Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="088f4-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="088f4-120">Información que detalla las funciones, estructuras de datos y constantes enumeradas que componen la API de DRT.</span><span class="sxs-lookup"><span data-stu-id="088f4-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 




