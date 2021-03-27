---
title: Interfaces de recursos (gráficos Direct3D 11)
description: Hay una serie de interfaces para los dos tipos básicos de búferes de recursos y texturas.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- interfaces, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d8f01e8d485fcdf575e8aea1a5beeb2184946b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800860"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Interfaces de recursos (gráficos Direct3D 11)

Hay una serie de interfaces para los dos tipos básicos de recursos: búferes y texturas. También hay interfaces para las vistas de recursos.

Una aplicación utiliza una vista para enlazar un recurso a una fase de canalización. La vista define cómo se puede tener acceso al recurso durante la representación. En esta sección se describen las interfaces de vista.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Una interfaz de búfer tiene acceso a un recurso de búfer, que es memoria no estructurada. Normalmente, los búferes almacenan datos de vértices o índices.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Una interfaz de vista de estarcido de profundidad tiene acceso a un recurso de textura durante las pruebas de la galería de símbolos de profundidad.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Una interfaz de representación-destino-vista identifica los Subrecursos de destino de representación a los que se puede tener acceso durante la representación.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Una interfaz de representación-destino-vista representa los Subrecursos de destino de representación a los que se puede tener acceso durante la representación.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Una interfaz de recursos proporciona acciones comunes en todos los recursos.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Una interfaz de vista de recursos del sombreador: especifica los Subrecursos a los que puede tener acceso un sombreador durante la representación. Entre los ejemplos de recursos del sombreador se incluyen un búfer de constantes, un búfer de textura y una textura.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Una interfaz de la vista de recursos del sombreador representa los Subrecursos a los que puede tener acceso un sombreador durante la representación. Entre los ejemplos de recursos del sombreador se incluyen un búfer de constantes, un búfer de textura y una textura.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Una interfaz de textura 1D obtiene acceso a los datos de textura, que es la memoria estructurada.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Una interfaz de textura 2D administra los datos de textura, que es la memoria estructurada.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Una interfaz de textura 2D representa los datos de textura, que es la memoria estructurada.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Una interfaz de textura 3D obtiene acceso a los datos de textura, que es la memoria estructurada.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Una interfaz de textura 3D representa los datos de textura, que es la memoria estructurada.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Una interfaz de vista especifica los elementos de un recurso a los que la canalización puede tener acceso durante la representación.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Una interfaz de vista de acceso sin ordenar representa los elementos de un recurso a los que la canalización puede tener acceso durante la representación.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Una interfaz de vista especifica los elementos de un recurso a los que la canalización puede tener acceso durante la representación.<br/>                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





