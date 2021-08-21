---
title: Método ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect.h)
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
ms.openlocfilehash: ddf94d3e4686bcbc0206601938e8cf8ab5d0d81a1925aaf7bb814eb30a82ba4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533261"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a>Método ID3DX11EffectShaderVariable::GetPixelShader

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> <dt>

*App* 
</dt> <dd>

Tipo: **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***

Puntero a un puntero [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) que se establecerá en el sombreador de píxeles en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

