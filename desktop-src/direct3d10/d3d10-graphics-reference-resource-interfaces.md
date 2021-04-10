---
description: 'Direct3D 10 define un número de interfaces para los dos tipos básicos de recursos: búferes y texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153014"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfaces de recursos (gráficos de Direct3D 10)

Direct3D 10 define un número de interfaces para los dos tipos básicos de recursos: [búferes](d3d10-graphics-programming-guide-resources-types.md) y texturas.



| Interfaces                                           | Descripción                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Interfaz ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Obtiene acceso a los datos del búfer.                                |
| [**Interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Clase base de un recurso.                           |
| [**Interfaz ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Obtiene acceso a los datos de una textura 1D o de una matriz de textura 1D. |
| [**Interfaz ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Obtiene acceso a los datos de una textura 2D o de una matriz de textura 2D  |
| [**Interfaz ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Obtiene acceso a los datos de una textura 3D o de una matriz de textura 3D. |



 

Una aplicación utiliza una vista para enlazar un recurso a una [fase de canalización](d3d10-graphics-programming-guide-pipeline-stages.md). La [vista](d3d10-graphics-programming-guide-resources-access-views.md) define cómo se puede tener acceso al recurso durante la representación. La API contiene estas interfaces de vista.



| Interfaces                                                               | Descripción                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Interfaz ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Obtiene acceso a los datos en una textura [de estarcido de profundidad](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) . |
| [**Interfaz ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Obtiene acceso a los datos de un [destino de representación](d3d10-graphics-programming-guide-resources-creating-textures.md).        |
| [**Interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Obtiene acceso a los datos de un sombreador-Resource en Direct3D 10,0.                                                         |
| [**Interfaz ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Obtiene acceso a los datos de un sombreador-Resource en Direct3D 10,1.                                                         |
| [**Interfaz ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Clase base para una vista.                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
