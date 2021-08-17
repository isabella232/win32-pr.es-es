---
title: Interfaces de recursos (gráficos de Direct3D 11)
description: Hay una serie de interfaces para los dos tipos básicos de búferes y texturas de recursos.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- interfaces, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0896bd04a51a989e502676ee314e17d1bf94a110df8a5af9dfe82210dd1b6b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125349"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Interfaces de recursos (gráficos de Direct3D 11)

Hay una serie de interfaces para los dos tipos básicos de recursos: búferes y texturas. También hay interfaces para vistas de recursos.

Una aplicación usa una vista para enlazar un recurso a una fase de canalización. La vista define cómo se puede acceder al recurso durante la representación. En esta sección se describen las interfaces de vista.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Una interfaz de búfer accede a un recurso de búfer, que es memoria no estructurada. Los búferes suelen almacenar datos de vértices o índices.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Una interfaz de vista de galería de símbolos de profundidad accede a un recurso de textura durante las pruebas de galería de símbolos de profundidad.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Una interfaz render-target-view identifica los subrecursos de destino de representación a los que se puede acceder durante la representación.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Una interfaz render-target-view representa los subrecursos de destino de representación a los que se puede acceder durante la representación.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Una interfaz de recursos proporciona acciones comunes en todos los recursos.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Una interfaz de vista de recursos de sombreador especifica los subrecursos a los que puede acceder un sombreador durante la representación. Algunos ejemplos de recursos de sombreador son un búfer constante, un búfer de textura y una textura.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Una interfaz de vista de recursos de sombreador representa los subrecursos a los que puede acceder un sombreador durante la representación. Algunos ejemplos de recursos de sombreador son un búfer constante, un búfer de textura y una textura.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Una interfaz de textura 1D accede a los datos de textura, que es memoria estructurada.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Una interfaz de textura 2D administra los datos de texel, que es la memoria estructurada.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Una interfaz de textura 2D representa datos de textura, que es memoria estructurada.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Una interfaz de textura 3D accede a los datos de textura, que es la memoria estructurada.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Una interfaz de textura 3D representa datos de textura, que es memoria estructurada.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Una interfaz de vista especifica las partes de un recurso al que la canalización puede acceder durante la representación.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Una interfaz unordered-access-view representa las partes de un recurso al que la canalización puede acceder durante la representación.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Una interfaz de vista especifica las partes de un recurso al que la canalización puede acceder durante la representación.<br/>                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





