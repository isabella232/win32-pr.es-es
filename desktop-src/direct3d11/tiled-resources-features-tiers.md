---
title: Niveles de características de recursos en mosaico
description: Direct3D 11.2 expone la compatibilidad con recursos en mosaico en dos niveles con los valores de NIVEL DE RECURSOS EN MOSAICO de D3D11. \_ \_ \_
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b76c1d90cc48210f02983817b317eb830224b8f87bb8b4904ee3e11d6cdd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894385"
---
# <a name="tiled-resources-features-tiers"></a>Niveles de características de recursos en mosaico

Direct3D 11.2 expone la compatibilidad con recursos en mosaico en dos niveles con los valores de NIVEL DE RECURSOS EN MOSAICO de [**\_ \_ \_ D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier)

Para consultar si el hardware y el controlador admiten recursos en mosaico y en qué nivel, pase el valor [**\_ D3D11 FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) al parámetro *Feature* de [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Además, pase un puntero a la estructura [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al *parámetro pFeatureSupportData* y pase el tamaño de la estructura **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1** al *parámetro FeatureSupportDataSize.* **CheckFeatureSupport** devuelve el nivel como un valor [**D3D11 \_ TILED RESOURCES \_ \_ TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) en el miembro **TiledResourcesTier** de **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1**.

En esta sección se describen estos dos niveles.

## <a name="in-this-section"></a>En esta sección



| Tema                           | Descripción                                       |
|---------------------------------|---------------------------------------------------|
| [Nivel 1](tier-1.md)<br/> | En esta sección se describe la compatibilidad con el nivel 1.<br/> |
| [Nivel 2](tier-2.md)<br/> | En esta sección se describe la compatibilidad con el nivel 2.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 





