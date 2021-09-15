---
title: Interfaz ID3DX11EffectShaderVariable (D3dx11effect.h)
description: Una interfaz de sombreador y variable accede a una variable de sombreador.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interfaz ID3DX11EffectShaderVariable Direct3D 11
- Id3DX11EffectShaderVariable interface Direct3D 11 , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581237"
---
# <a name="id3dx11effectshadervariable-interface"></a>Interfaz ID3DX11EffectShaderVariable

Una interfaz de sombreador y variable accede a una variable de sombreador.

## <a name="members"></a>Members

La **interfaz ID3DX11EffectShaderVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectShaderVariable** tiene estos métodos.



| Método                                                                                                           | Descripción                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**GetComputeShader**](id3dx11effectshadervariable-getcomputeshader.md)                                         | Obtiene un sombreador de proceso.<br/>                       |
| [**GetDomainShader**](id3dx11effectshadervariable-getdomainshader.md)                                           | Obtiene un sombreador de dominio.<br/>                        |
| [**GetGeometryShader**](id3dx11effectshadervariable-getgeometryshader.md)                                       | Obtiene un sombreador de geometría.<br/>                      |
| [**GetHullShader**](id3dx11effectshadervariable-gethullshader.md)                                               | Obtiene un sombreador de casco.<br/>                          |
| [**GetInputSignatureElementDesc**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | Obtenga una descripción de la firma de entrada.<br/>         |
| [**GetOutputSignatureElementDesc**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | Obtenga una descripción de la firma de salida.<br/>        |
| [**GetPatchConstantSignatureElementDesc**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | Obtiene una descripción de firma de constante de revisión.<br/> |
| [**GetPixelShader**](id3dx11effectshadervariable-getpixelshader.md)                                             | Obtiene un sombreador de píxeles.<br/>                         |
| [**GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)                                               | Obtiene una descripción del sombreador.<br/>                   |
| [**GetVertexShader**](id3dx11effectshadervariable-getvertexshader.md)                                           | Obtiene un sombreador de vértices.<br/>                        |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





