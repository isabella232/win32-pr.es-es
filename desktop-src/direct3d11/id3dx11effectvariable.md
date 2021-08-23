---
title: Interfaz ID3DX11EffectVariable (D3dx11effect.h)
description: La interfaz ID3DX11EffectVariable es la clase base para todas las variables de efecto. La duración de un objeto ID3DX11EffectVariable es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interfaz ID3DX11EffectVariable Direct3D 11
- Interfaz ID3DX11EffectVariable Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3340ba231785edb9446c8578d886fca4a28ecbb09e69230d7f8661a5650afa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045813"
---
# <a name="id3dx11effectvariable-interface"></a>Interfaz ID3DX11EffectVariable

La **interfaz ID3DX11EffectVariable** es la clase base para todas las variables de efecto.

La duración de **un objeto ID3DX11EffectVariable** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectVariable** tiene estos métodos.



| Método                                                                           | Descripción                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | Obtiene una variable de combinación de efecto.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Obtiene una variable de instancia de clase.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Obtiene un búfer constante.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Obtiene una variable de galería de símbolos de profundidad.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Obtiene una variable depth-stencil-view.<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | Obtiene una variable de interfaz.<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | Obtiene una variable de matriz.<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Obtiene una variable rasterizadora.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Obtiene una variable render-target-view.<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | Obtenga una variable sampler.<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | Obtiene una variable escalar.<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | Obtiene una variable de sombreador.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Obtiene una variable de recurso de sombreador.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Obtiene una variable de cadena.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Obtiene una variable unordered-access-view.<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | Obtiene una variable de vector.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Obtiene una anotación por índice.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Obtiene una anotación por nombre.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Obtenga una descripción.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Obtiene un elemento de matriz.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Obtener un miembro de estructura por índice.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Obtener un miembro de estructura por nombre.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Obtener un miembro de estructura por semántica.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Obtiene un búfer constante.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Obtener datos.<br/>                                   |
| [**Gettype**](id3dx11effectvariable-gettype.md)                                 | Obtener información de tipo.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Compare el tipo de datos con los datos almacenados.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Establecer datos.<br/>                                   |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





