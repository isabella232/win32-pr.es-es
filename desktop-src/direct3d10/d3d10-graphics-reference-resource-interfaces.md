---
description: 'Direct3D 10 define una serie de interfaces para los dos tipos básicos de recursos: búferes y texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282825"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfaces de recursos (gráficos de Direct3D 10)

Direct3D 10 define una serie de interfaces para los dos tipos básicos de recursos: [búferes](d3d10-graphics-programming-guide-resources-types.md) y texturas.



| Interfaces                                           | Descripción                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Interfaz ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Accede a los datos del búfer.                                |
| [**Interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Clase base para un recurso.                           |
| [**Interfaz ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Accede a los datos en una textura 1D o en una matriz de textura 1D. |
| [**Interfaz ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Accede a datos en una textura 2D o en una matriz de texturas 2D  |
| [**Interfaz ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Accede a los datos en una textura 3D o en una matriz de texturas 3D. |



 

Una aplicación usa una vista para enlazar un recurso a una fase [de canalización.](d3d10-graphics-programming-guide-pipeline-stages.md) La [vista](d3d10-graphics-programming-guide-resources-access-views.md) define cómo se puede acceder al recurso durante la representación. La API contiene estas interfaces de vista.



| Interfaces                                                               | Descripción                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Interfaz ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Accede a los datos en una [textura de galería de símbolos de](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) profundidad. |
| [**Interfaz ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Accede a los datos de un [destino de representación.](d3d10-graphics-programming-guide-resources-creating-textures.md)        |
| [**Interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Accede a los datos de un recurso de sombreador en Direct3D 10.0.                                                         |
| [**Interfaz ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Accede a los datos de un recurso de sombreador en Direct3D 10.1.                                                         |
| [**Interfaz ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Clase base para una vista.                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
