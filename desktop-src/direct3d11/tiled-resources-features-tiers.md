---
title: Niveles de características de recursos en mosaico
description: Direct3D 11,2 expone la compatibilidad con los recursos en mosaico en dos niveles con los \_ valores de nivel de recursos en mosaico D3D11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993982"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="75e45-103">Niveles de características de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="75e45-103">Tiled resources features tiers</span></span>

<span data-ttu-id="75e45-104">Direct3D 11,2 expone la compatibilidad con los recursos en mosaico en dos niveles con los valores de [**\_ nivel de \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="75e45-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="75e45-105">Para consultar si el hardware y el controlador admiten recursos en mosaico y en qué nivel de nivel, pase el valor de D3D11 de la [**\_ característica \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) al parámetro de *característica* de [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="75e45-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="75e45-106">También puede pasar un puntero a la [**estructura \_ \_ OPTIONS1 de \_ D3D11 \_ de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al parámetro *pFeatureSupportData* y pasar el tamaño de la estructura D3D11 D3D11 de **\_ datos de características \_ \_ \_** OPTIONS1 al parámetro *FeatureSupportDataSize* .</span><span class="sxs-lookup"><span data-stu-id="75e45-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="75e45-107">**CheckFeatureSupport** devuelve el nivel de nivel como un valor de nivel de [**\_ \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) en el miembro **TiledResourcesTier** de **D3D11 \_ \_ Data Data \_ D3D11 \_ OPTIONS1**.</span><span class="sxs-lookup"><span data-stu-id="75e45-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="75e45-108">En esta sección se describen estos dos niveles.</span><span class="sxs-lookup"><span data-stu-id="75e45-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75e45-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="75e45-109">In this section</span></span>



| <span data-ttu-id="75e45-110">Tema</span><span class="sxs-lookup"><span data-stu-id="75e45-110">Topic</span></span>                           | <span data-ttu-id="75e45-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="75e45-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="75e45-112">Nivel 1</span><span class="sxs-lookup"><span data-stu-id="75e45-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="75e45-113">En esta sección se describe la compatibilidad de nivel 1.</span><span class="sxs-lookup"><span data-stu-id="75e45-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="75e45-114">Nivel 2</span><span class="sxs-lookup"><span data-stu-id="75e45-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="75e45-115">En esta sección se describe la compatibilidad de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="75e45-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="75e45-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75e45-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75e45-117">Recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="75e45-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





