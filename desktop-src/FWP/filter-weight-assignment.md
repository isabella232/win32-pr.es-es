---
title: Asignación del peso del filtro
description: Cada filtro de la plataforma de filtrado de Windows (WFP) tiene un peso asociado, que se utiliza durante el arbitraje del filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/26/2020
ms.locfileid: "104420463"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="db7e7-103">Asignación del peso del filtro</span><span class="sxs-lookup"><span data-stu-id="db7e7-103">Filter Weight Assignment</span></span>

<span data-ttu-id="db7e7-104">Cada filtro de la plataforma de filtrado de Windows (WFP) tiene un peso asociado, que se utiliza durante el [arbitraje del filtro](filter-arbitration.md).</span><span class="sxs-lookup"><span data-stu-id="db7e7-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="db7e7-105">El peso de filtro usado por el motor de filtrado de base (BFE) es de tipo [**FWP \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="db7e7-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="db7e7-106">Los llamadores tienen tres opciones al agregar filtros.</span><span class="sxs-lookup"><span data-stu-id="db7e7-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="db7e7-107">Establezca el peso en un valor de [**FWP \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="db7e7-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="db7e7-108">BFE usa el peso proporcionado tal cual.</span><span class="sxs-lookup"><span data-stu-id="db7e7-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="db7e7-109">Establezca el peso en el valor de [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="db7e7-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="db7e7-110">BFE genera automáticamente un peso en el intervalo comprendido entre \[ 0 y 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="db7e7-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="db7e7-111">Establezca el peso en un valor de [**FWP \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) en el intervalo de \[ 0 a 15 \] .</span><span class="sxs-lookup"><span data-stu-id="db7e7-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="db7e7-112">BFE usa el peso proporcionado como identificador de intervalo de peso.</span><span class="sxs-lookup"><span data-stu-id="db7e7-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="db7e7-113">BFE genera automáticamente los bits 60 de orden inferior (exactamente como si el peso se hubiera establecido en [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) y, a continuación, usa el valor proporcionado para establecer los 4 bits de orden superior.</span><span class="sxs-lookup"><span data-stu-id="db7e7-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="db7e7-114">Esto permite a los autores de llamadas dividir manualmente el espacio de peso en 16 intervalos, a la vez que se sigue usando la ponderación automática dentro de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="db7e7-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="db7e7-115">Cuando dos o más llamadas se registran en la misma subcapa, pueden producirse problemas cuando se asigna el mismo peso a los filtros.</span><span class="sxs-lookup"><span data-stu-id="db7e7-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="db7e7-116">Este problema se puede evitar al hacer que las llamadas creen su propia subcapa mediante [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span><span class="sxs-lookup"><span data-stu-id="db7e7-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="db7e7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db7e7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7e7-118">**Identificadores de peso de filtro**</span><span class="sxs-lookup"><span data-stu-id="db7e7-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




