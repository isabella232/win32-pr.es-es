---
title: Exenciones de IKE/AuthIP
description: Intercambio de claves por red (IKE) y protocolo de Internet autenticado (AuthIP), para poder funcionar, deben eximir el tráfico de red del filtrado IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420325"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="b55d3-103">Exenciones de IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="b55d3-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="b55d3-104">Los módulos de creación de claves del Protocolo de seguridad de Internet (IPsec), Intercambio de claves por red (IKE) y protocolo de Internet autenticado (AuthIP), para que funcionen, deben eximir el tráfico de red del filtrado IPsec.</span><span class="sxs-lookup"><span data-stu-id="b55d3-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="b55d3-105">En la plataforma de filtrado de Windows (WFP), el motor de filtrado de base (BFE) agrega automáticamente filtros de exención de IKE y AuthIP cuando se agrega el primer filtro de directiva de modo principal IKE o AuthIP (MM) y los elimina cuando se elimina el último filtro de directiva IKE o AuthIP MM.</span><span class="sxs-lookup"><span data-stu-id="b55d3-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="b55d3-106">De esta manera, los proveedores de directivas no tienen que administrar las exenciones de filtrado de IKE y AuthIP de forma individual.</span><span class="sxs-lookup"><span data-stu-id="b55d3-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="b55d3-107">Un filtro de directiva de IKE MM es un filtro en la capa del motor [**FWPM \_ capa \_ \_ \|**](management-filtering-layer-identifiers-.md) de la capa de la capa de la capa de la versión de tipo [**FWPM \_ IPSec \_ IKE \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="b55d3-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="b55d3-108">Un filtro de directiva de AuthIP MM es un filtro en la capa de motor FWPM de nivel de motor de la capa de sistema [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que hace referencia a un contexto de proveedor de tipo [**FWPM de \_ contexto de IPSec \_ AuthIP \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="b55d3-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="b55d3-109">Un filtro de exención de IKE o AuthIP es un filtro en la capa del motor [**FWPM \_ capa de transporte de \_ entrada \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) o en el **transporte de salida de \_ capa FWPM \_ \_ \_ v {4 \| 6}** ponderado automáticamente en el intervalo de peso de las [**\_ \_ \_ \_ exenciones de IKE del intervalo de ponderación de FWPM**](filter-weight-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="b55d3-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="b55d3-110">Las exenciones IKE y AuthIP implementadas por BFE son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="b55d3-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="b55d3-111">Versión de la dirección IP</span><span class="sxs-lookup"><span data-stu-id="b55d3-111">IP version</span></span>      | <span data-ttu-id="b55d3-112">Port</span><span class="sxs-lookup"><span data-stu-id="b55d3-112">Port</span></span>                        | <span data-ttu-id="b55d3-113">Exención</span><span class="sxs-lookup"><span data-stu-id="b55d3-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b55d3-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="b55d3-114">IPv4</span></span><br/> | <span data-ttu-id="b55d3-115">UDP: 500 UDP: 4500</span><span class="sxs-lookup"><span data-stu-id="b55d3-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="b55d3-116">Permita el tráfico de IKE y AuthIP en el nivel de transporte de entrada y en la capa de transporte de salida.</span><span class="sxs-lookup"><span data-stu-id="b55d3-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="b55d3-117">Permita el tráfico de IKE y AuthIP en las capas de recepción y aceptación y conexión de ALE, pero restrinja el sistema local.</span><span class="sxs-lookup"><span data-stu-id="b55d3-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="b55d3-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="b55d3-118">IPv6</span></span><br/> | <span data-ttu-id="b55d3-119">UDP: 500</span><span class="sxs-lookup"><span data-stu-id="b55d3-119">UDP:500</span></span><br/>          | <span data-ttu-id="b55d3-120">Permita el tráfico de IKE y AuthIP en el nivel de transporte de entrada y en la capa de transporte de salida.</span><span class="sxs-lookup"><span data-stu-id="b55d3-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="b55d3-121">Permita el tráfico de IKE y AuthIP en las capas de recepción y aceptación y conexión de ALE, pero restrinja el sistema local.</span><span class="sxs-lookup"><span data-stu-id="b55d3-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="b55d3-122">Los filtros de exención de IKE y AuthIP están abiertos a todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="b55d3-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="b55d3-123">Para implementar un firewall con un control más granular, los proveedores de directivas deben agregar filtros en un intervalo de peso superior a las [**\_ \_ \_ \_ exenciones IKE del intervalo de peso de FWPM**](filter-weight-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b55d3-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b55d3-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b55d3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b55d3-125">Configuración de IPsec</span><span class="sxs-lookup"><span data-stu-id="b55d3-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="b55d3-126">Asignación del peso del filtro</span><span class="sxs-lookup"><span data-stu-id="b55d3-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





