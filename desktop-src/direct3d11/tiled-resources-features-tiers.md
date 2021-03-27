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
# <a name="tiled-resources-features-tiers"></a>Niveles de características de recursos en mosaico

Direct3D 11,2 expone la compatibilidad con los recursos en mosaico en dos niveles con los valores de [**\_ nivel de \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .

Para consultar si el hardware y el controlador admiten recursos en mosaico y en qué nivel de nivel, pase el valor de D3D11 de la [**\_ característica \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) al parámetro de *característica* de [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). También puede pasar un puntero a la [**estructura \_ \_ OPTIONS1 de \_ D3D11 \_ de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al parámetro *pFeatureSupportData* y pasar el tamaño de la estructura D3D11 D3D11 de **\_ datos de características \_ \_ \_** OPTIONS1 al parámetro *FeatureSupportDataSize* . **CheckFeatureSupport** devuelve el nivel de nivel como un valor de nivel de [**\_ \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) en el miembro **TiledResourcesTier** de **D3D11 \_ \_ Data Data \_ D3D11 \_ OPTIONS1**.

En esta sección se describen estos dos niveles.

## <a name="in-this-section"></a>En esta sección



| Tema                           | Descripción                                       |
|---------------------------------|---------------------------------------------------|
| [Nivel 1](tier-1.md)<br/> | En esta sección se describe la compatibilidad de nivel 1.<br/> |
| [Nivel 2](tier-2.md)<br/> | En esta sección se describe la compatibilidad de nivel 2.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 





