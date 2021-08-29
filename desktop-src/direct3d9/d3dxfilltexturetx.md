---
description: 'Función D3DXFillTextureTX: usa una función compilada de lenguaje de sombreador de alto nivel (HLSL) para rellenar cada texel de cada nivel de mapa mip de una textura.'
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Función D3DXFillTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1a71d6a31e3df645532cc73f836c3645621bb8f94c6115c56018c5eed3839313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045043"
---
# <a name="d3dxfilltexturetx-function"></a>Función D3DXFillTextureTX

Usa una función de lenguaje de sombreador de alto nivel (HLSL) compilada para rellenar cada elemento texel de cada nivel de mapa mip de una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un [**objeto IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura que se va a rellenar.

</dd> <dt>

*pTextureShader* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Puntero a un [**objeto de sombreador de textura ID3DXTextureShader.**](id3dxtextureshader.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

El destino de textura debe ser una función HLSL que tome la semántica siguiente:

-   Un parámetro de entrada debe usar una semántica POSITION.
-   Un parámetro de entrada debe usar una semántica PSIZE.
-   La función debe devolver un parámetro que use la semántica COLOR.

A continuación se muestra un ejemplo de una función HLSL de este tipo:


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



Tenga en cuenta que los parámetros de entrada pueden estar en cualquier orden, pero se debe representar ambas semánticas de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
