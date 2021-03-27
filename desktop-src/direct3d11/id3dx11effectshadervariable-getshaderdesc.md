---
title: Método ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Obtener una descripción del sombreador.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Método GetShaderDesc Direct3D 11
- Método GetShaderDesc Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987103"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a>ID3DX11EffectShaderVariable:: GetShaderDesc (método)

Obtener una descripción del sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)\***

Un puntero a una descripción del sombreador (vea [**D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

