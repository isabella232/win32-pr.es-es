---
description: Recopilación de métricas de partición
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Recopilación de métricas de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152950"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="068ca-103">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="068ca-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="068ca-104">En algunos casos, es posible que una organización desee recopilar información sobre el uso de aplicaciones COM+ con fines de supervisión, planeamiento de capacidad y contabilidad de recursos.</span><span class="sxs-lookup"><span data-stu-id="068ca-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="068ca-105">Por ejemplo, un proveedor de servicios de aplicaciones (ASP) podría querer cobrar un cliente por su uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="068ca-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="068ca-106">Para ello, COM+ le permite recopilar información de eventos y métricas por partición.</span><span class="sxs-lookup"><span data-stu-id="068ca-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="068ca-107">La manera de recopilar esta información para una partición específica es especificando, para cada interfaz de instrumentación de COM+, el miembro de ID. de partición dentro de la estructura de eventos estándar.</span><span class="sxs-lookup"><span data-stu-id="068ca-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="068ca-108">La estructura de eventos es el primer valor de una interfaz de instrumentación de COM+.</span><span class="sxs-lookup"><span data-stu-id="068ca-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="068ca-109">Para obtener más información, vea [interfaces de instrumentación de com+](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="068ca-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="068ca-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="068ca-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="068ca-111">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="068ca-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="068ca-112">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="068ca-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="068ca-113">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="068ca-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="068ca-114">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="068ca-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="068ca-115">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="068ca-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



