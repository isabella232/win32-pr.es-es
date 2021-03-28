---
title: Método ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect. h)
description: Obtiene un sombreador de píxeles.
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- Método GetPixelShader Direct3D 11
- Método GetPixelShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetPixelShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548059"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a>ID3DX11EffectShaderVariable:: GetPixelShader (método)

Obtiene un sombreador de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> <dt>

*ppPS* 
</dt> <dd>

Tipo: **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***

Un puntero a un puntero [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) que se establecerá en el sombreador de píxeles de la devolución.

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

 

