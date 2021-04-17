---
description: Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuida (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumeraciones de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667446"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="cf143-103">Enumeraciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="cf143-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="cf143-104">Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuida (DRT).</span><span class="sxs-lookup"><span data-stu-id="cf143-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="cf143-105">Enumeración</span><span class="sxs-lookup"><span data-stu-id="cf143-105">Enumeration</span></span>                                                            | <span data-ttu-id="cf143-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf143-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf143-107">**ámbito de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="cf143-108">Define el conjunto de ámbitos IPv6 en el que la DRT funcionará cuando se use el transporte UDP de IPv6 creado por [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span><span class="sxs-lookup"><span data-stu-id="cf143-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="cf143-109">**\_marcas de dirección de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="cf143-110">Define el conjunto de respuestas que puede devolver un nodo intermedio al realizar una búsqueda de una clave.</span><span class="sxs-lookup"><span data-stu-id="cf143-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="cf143-111">**Estado de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="cf143-112">Define los posibles estados de conectividad y error de un nodo local.</span><span class="sxs-lookup"><span data-stu-id="cf143-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="cf143-113">**\_tipo de coincidencia de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="cf143-114">Define la exactitud de los resultados que se devuelven cuando se realiza una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cf143-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="cf143-115">**\_tipo de \_ cambio de clave de LEAFSET de DRT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="cf143-116">Define el conjunto de tipos de cambios que se pueden realizar en un nodo de conjunto de hoja local en la caché de DRT local.</span><span class="sxs-lookup"><span data-stu-id="cf143-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="cf143-117">**\_tipo de evento DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="cf143-118">Define el conjunto de eventos que puede generar la DRT.</span><span class="sxs-lookup"><span data-stu-id="cf143-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="cf143-119">**\_modo de seguridad de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="cf143-120">Define los posibles modos de seguridad de DRT.</span><span class="sxs-lookup"><span data-stu-id="cf143-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="cf143-121">Esta enumeración es un campo de la estructura de [**\_ configuración de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="cf143-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="cf143-122">**\_Estado de registro de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="cf143-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="cf143-123">Define el estado de una clave registrada.</span><span class="sxs-lookup"><span data-stu-id="cf143-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="cf143-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf143-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf143-125">Estructuras de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="cf143-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="cf143-126">Funciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="cf143-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="cf143-127">Referencia de Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="cf143-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



