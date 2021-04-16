---
description: En esta sección se describe la programación de multidifusión basada en el estado final con ioctl en lugar de las opciones de socket. Para obtener información general sobre el modo en que la programación de multidifusión basada en el estado final difiere de la programación multidifusión basada en cambios, vea programación con multidifusión.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programación de multidifusión basada en el estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705624"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="22dd3-104">Programación de multidifusión basada en el estado final</span><span class="sxs-lookup"><span data-stu-id="22dd3-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="22dd3-105">En esta sección se describe la programación de multidifusión basada en el estado final con ioctl en lugar de las opciones de socket.</span><span class="sxs-lookup"><span data-stu-id="22dd3-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="22dd3-106">Para obtener información general sobre el modo en que la programación de multidifusión basada en el estado final difiere de la programación multidifusión basada en cambios, vea [programación con multidifusión](multicast-programming.md).</span><span class="sxs-lookup"><span data-stu-id="22dd3-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="22dd3-107">En la tabla siguiente se describen los ioctl de Windows Sockets usados para la programación de multidifusión en Windows.</span><span class="sxs-lookup"><span data-stu-id="22dd3-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="22dd3-108">INSERCIÓN</span><span class="sxs-lookup"><span data-stu-id="22dd3-108">IOCTL</span></span>                       | <span data-ttu-id="22dd3-109">Tipo de argumento</span><span class="sxs-lookup"><span data-stu-id="22dd3-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="22dd3-110">SIOCSMSFILTER</span><span class="sxs-lookup"><span data-stu-id="22dd3-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="22dd3-111">[**Grupo \_ de**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estructura del filtro</span><span class="sxs-lookup"><span data-stu-id="22dd3-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="22dd3-112">SIOCGMSFILTER</span><span class="sxs-lookup"><span data-stu-id="22dd3-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="22dd3-113">[**Grupo \_ de**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estructura del filtro</span><span class="sxs-lookup"><span data-stu-id="22dd3-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="22dd3-114">SIO \_ obtener \_ filtro de multidifusión \_</span><span class="sxs-lookup"><span data-stu-id="22dd3-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="22dd3-115">estructura de [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="22dd3-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="22dd3-116">SIO \_ establecer \_ filtro de multidifusión \_</span><span class="sxs-lookup"><span data-stu-id="22dd3-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="22dd3-117">estructura de [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="22dd3-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="22dd3-118">Tenga en cuenta que los ioctl **SIOCSMSFILTER** y **SIOCGMSFILTER** están disponibles en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="22dd3-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="22dd3-119">El uso de estos ioctl para la programación multidifusión tiene ventajas de rendimiento al trabajar con listas de orígenes de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="22dd3-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="22dd3-120">Para obtener más información acerca de los parámetros y la configuración asociados con el uso de SIO \_ Get \_ Multicast \_ Filter o SiO \_ set \_ Multicast \_ Filter, consulte la página de referencia del [**\_ filtro de grupo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) .</span><span class="sxs-lookup"><span data-stu-id="22dd3-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="22dd3-121">Para obtener más información sobre los parámetros y la configuración asociados con el uso de SIO \_ Get \_ Multicast \_ Filter o el \_ filtro de \_ multidifusión set de \_ [**\_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) , consulte la página de referencia de IP.</span><span class="sxs-lookup"><span data-stu-id="22dd3-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



