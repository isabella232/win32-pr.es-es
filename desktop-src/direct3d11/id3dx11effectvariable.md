---
title: Interfaz ID3DX11EffectVariable (D3dx11effect. h)
description: La interfaz ID3DX11EffectVariable es la clase base para todas las variables de efecto. La duración de un objeto ID3DX11EffectVariable es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interfaz ID3DX11EffectVariable Direct3D 11
- Interfaz ID3DX11EffectVariable Direct3D 11, descrita
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
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821287"
---
# <a name="id3dx11effectvariable-interface"></a>Interfaz ID3DX11EffectVariable

La interfaz **ID3DX11EffectVariable** es la clase base para todas las variables de efecto.

La duración de un objeto **ID3DX11EffectVariable** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectVariable** tiene estos métodos.



| Método                                                                           | Descripción                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**Asblend**](id3dx11effectvariable-asblend.md)                                 | Obtiene una variable Effect-Blend.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Obtiene una variable de instancia de clase.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Obtiene un búfer de constantes.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Obtiene una variable de estarcido de profundidad.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Obtiene una variable de vista de estarcido de profundidad.<br/>          |
| [**Asinterface**](id3dx11effectvariable-asinterface.md)                         | Obtiene una variable de interfaz.<br/>                  |
| [**Asmatrix**](id3dx11effectvariable-asmatrix.md)                               | Obtiene una variable de matriz.<br/>                      |
| [**Asrasterizador**](id3dx11effectvariable-asrasterizer.md)                       | Obtiene una variable de rasterizador.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Obtiene una variable de vista de destino de representación.<br/>          |
| [**Asmuestreador**](id3dx11effectvariable-assampler.md)                             | Obtiene una variable de muestra.<br/>                     |
| [**Asescalar**](id3dx11effectvariable-asscalar.md)                               | Obtiene una variable escalar.<br/>                      |
| [**Assombreador**](id3dx11effectvariable-asshader.md)                               | Obtiene una variable de sombreador.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Obtiene una variable de recurso de sombreador.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Obtiene una variable de cadena.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Obtiene una variable de vista de acceso sin ordenar.<br/>      |
| [**Asvector**](id3dx11effectvariable-asvector.md)                               | Obtiene una variable de vector.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Obtiene una anotación por índice.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Obtiene una anotación por nombre.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Obtener una descripción.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Obtiene un elemento de matriz.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Obtiene un miembro de estructura por índice.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Obtiene un miembro de estructura por nombre.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Obtiene un miembro de estructura por semántica.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Obtiene un búfer de constantes.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Obtener datos.<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Obtener información de tipo.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Comparar el tipo de datos con los datos almacenados.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Establecer datos.<br/>                                   |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





