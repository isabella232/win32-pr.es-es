---
title: Personalización del flujo ALE
description: El filtrado de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104358717"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="b2796-103">Personalización del flujo ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-103">ALE Flow Customization</span></span>

<span data-ttu-id="b2796-104">El filtrado de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.</span><span class="sxs-lookup"><span data-stu-id="b2796-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="b2796-105">Tráfico de multidifusión/difusión</span><span class="sxs-lookup"><span data-stu-id="b2796-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="b2796-106">Para bloquear el tráfico entrante en función de los Estados de multidifusión o difusión salientes, agregue un filtro que autorice el tráfico de difusión y multidifusión saliente y que tenga la opción de [**\_ \_ \_ \_ Estado de multidifusión Option reclasificación de FWP**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) establecida en el valor de la **\_ opción FWP \_ \_ denegar el \_ \_ Estado de multidifusión**.</span><span class="sxs-lookup"><span data-stu-id="b2796-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="b2796-107">Homólogos remotos</span><span class="sxs-lookup"><span data-stu-id="b2796-107">Remote Peers</span></span>

<span data-ttu-id="b2796-108">Para agregar paquetes de respuesta de diferentes elementos del mismo nivel al mismo flujo de ALE, agregue un filtro que tenga la opción de [**\_ \_ \_ \_ \_ asignación de código flexible**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) de la opción de clasificación de FWP establecida en el valor de la opción de **FWP \_ \_ \_ habilitar \_ \_ \_ asignación de origen flexible**.</span><span class="sxs-lookup"><span data-stu-id="b2796-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="b2796-109">Vea [usar opciones de clasificación](using-classify-options.md) para el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b2796-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="b2796-110">Duración del flujo de ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="b2796-111">Para modificar los valores de tiempo de espera de inactividad de un flujo ALE, agregue un filtro que tenga la opción de [**\_ \_ duración de \_ MCAST \_ BCAST \_ de FWP**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) y/o la opción de duración de **\_ \_ \_ unidifusión \_** de la opción de clasificación de FWP establecida en el valor de tiempo de espera de inactividad deseado.</span><span class="sxs-lookup"><span data-stu-id="b2796-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="b2796-112">Vea [usar las opciones de clasificación](using-classify-options.md) para obtener un ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b2796-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2796-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2796-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2796-114">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="b2796-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="b2796-115">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="b2796-116">Filtrado con estado ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="b2796-117">Tráfico de multidifusión/difusión ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="b2796-118">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="b2796-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="b2796-119">Usar opciones de clasificación</span><span class="sxs-lookup"><span data-stu-id="b2796-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




