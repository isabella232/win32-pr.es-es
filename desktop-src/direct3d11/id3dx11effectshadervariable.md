---
title: Interfaz ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Una interfaz de variable de sombreador tiene acceso a una variable de sombreador.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interfaz ID3DX11EffectShaderVariable Direct3D 11
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998437"
---
# <a name="id3dx11effectshadervariable-interface"></a>Interfaz ID3DX11EffectShaderVariable

Una interfaz de variable de sombreador tiene acceso a una variable de sombreador.

## <a name="members"></a>Miembros

La interfaz **ID3DX11EffectShaderVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectShaderVariable** tiene estos métodos.



| Método                                                                                                           | Descripción                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**GetComputeShader**](id3dx11effectshadervariable-getcomputeshader.md)                                         | Obtener un sombreador de cálculo.<br/>                       |
| [**GetDomainShader**](id3dx11effectshadervariable-getdomainshader.md)                                           | Obtiene un sombreador de dominios.<br/>                        |
| [**GetGeometryShader**](id3dx11effectshadervariable-getgeometryshader.md)                                       | Obtiene un sombreador de geometría.<br/>                      |
| [**GetHullShader**](id3dx11effectshadervariable-gethullshader.md)                                               | Obtener un sombreador de casco.<br/>                          |
| [**GetInputSignatureElementDesc**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | Obtiene una descripción de la firma de entrada.<br/>         |
| [**GetOutputSignatureElementDesc**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | Obtiene una descripción de la firma de salida.<br/>        |
| [**GetPatchConstantSignatureElementDesc**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | Obtiene una descripción de la firma de la constante patch.<br/> |
| [**GetPixelShader**](id3dx11effectshadervariable-getpixelshader.md)                                             | Obtiene un sombreador de píxeles.<br/>                         |
| [**GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)                                               | Obtener una descripción del sombreador.<br/>                   |
| [**GetVertexShader**](id3dx11effectshadervariable-getvertexshader.md)                                           | Obtiene un sombreador de vértices.<br/>                        |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





