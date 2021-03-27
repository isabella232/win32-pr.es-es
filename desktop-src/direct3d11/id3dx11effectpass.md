---
title: Interfaz ID3DX11EffectPass (D3dx11effect. h)
description: Una interfaz ID3DX11EffectPass encapsula las asignaciones de estado dentro de una técnica. La duración de un objeto ID3DX11EffectPass es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interfaz ID3DX11EffectPass Direct3D 11
- Interfaz ID3DX11EffectPass Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280454"
---
# <a name="id3dx11effectpass-interface"></a>Interfaz ID3DX11EffectPass

Una interfaz **ID3DX11EffectPass** encapsula las asignaciones de estado dentro de una técnica.

La duración de un objeto **ID3DX11EffectPass** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectPass** tiene estos métodos.



| Método                                                                   | Descripción                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Aplicar**](id3dx11effectpass-apply.md)                                 | Establezca el estado contenido en un paso en el dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Generar una máscara para permitir o evitar cambios de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Obtiene una anotación por índice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Obtiene una anotación por nombre.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Obtener una descripción del sombreador de cálculo.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Obtener una descripción del paso.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Obtiene una descripción del sombreador de dominio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Obtiene una descripción del sombreador de geometría.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Obtiene la descripción del sombreador de casco.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Obtiene una descripción del sombreador de píxeles.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Obtiene una descripción del sombreador de vértices.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Pruebe un paso para ver si contiene una sintaxis válida.<br/>        |



 

## <a name="remarks"></a>Observaciones

Un paso es un bloque de código que establece los objetos y sombreadores de estado de representación. Un paso se declara dentro de una técnica.

Para obtener una interfaz de paso de efecto, llame a un método como [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





