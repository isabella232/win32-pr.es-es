---
description: WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden utilizar para obtener información sobre el estado interno de WMI durante las operaciones básicas de WMI y de proveedor.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Clases de solución de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003009"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="45c57-103">Clases de solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="45c57-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="45c57-104">WMI proporciona un conjunto de clases de solución de problemas que los scripts y las aplicaciones pueden utilizar para obtener información sobre el estado interno de WMI durante las operaciones básicas de WMI y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="45c57-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="45c57-105">Para obtener más información acerca de la solución de problemas de WMI, consulte solución de problemas de [WMI](wmi-troubleshooting.md) y [clases de solución de problemas](provider-configuration-and-troubleshooting-classes.md).</span><span class="sxs-lookup"><span data-stu-id="45c57-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="45c57-106">WMI tiene varias clases básicas de solución de problemas para las operaciones básicas y de proveedor de WMI:</span><span class="sxs-lookup"><span data-stu-id="45c57-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="45c57-107">**\_Contadores de msft WmiProvider \_**</span><span class="sxs-lookup"><span data-stu-id="45c57-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="45c57-108">Solo se encuentra una de estas clases en cada sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="45c57-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="45c57-109">Proporciona recuentos de diferentes tipos de operaciones de proveedor en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="45c57-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="45c57-110">**MSFT \_ WmiSelfEvent**</span><span class="sxs-lookup"><span data-stu-id="45c57-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="45c57-111">Las clases de solución de problemas de eventos derivan de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span><span class="sxs-lookup"><span data-stu-id="45c57-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="45c57-112">Las consultas de esta clase devuelven instancias de clases de eventos como [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**msft \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="45c57-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="45c57-113">En la lista siguiente se proporcionan vínculos a distintas categorías de clases de eventos derivadas de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span><span class="sxs-lookup"><span data-stu-id="45c57-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="45c57-114">Clases de solución de problemas de eventos de proveedor</span><span class="sxs-lookup"><span data-stu-id="45c57-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="45c57-115">Clases de solución de problemas de ConsumerProvider</span><span class="sxs-lookup"><span data-stu-id="45c57-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="45c57-116">Clases de solución de problemas de eventos del servicio WMI</span><span class="sxs-lookup"><span data-stu-id="45c57-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="45c57-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45c57-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c57-118">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="45c57-118">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="45c57-119">Recibir un evento de WMI</span><span class="sxs-lookup"><span data-stu-id="45c57-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
