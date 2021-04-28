---
description: 'Función D3DXFillCubeTextureTX: usa una función compilada de lenguaje de sombreador de alto nivel (HLSL) para rellenar cada texel de cada nivel de mapa mip de una textura.'
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Función D3DXFillCubeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107673"
---
# <a name="d3dxfillcubetexturetx-function"></a>Función D3DXFillCubeTextureTX

Usa una función de lenguaje de sombreador de alto nivel (HLSL) compilada para rellenar cada texel de cada nivel de mapa mip de una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Puntero a un [**objeto IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa la textura que se va a rellenar.

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

Los parámetros de entrada pueden estar en cualquier orden. Para obtener un ejemplo, [ **vea D3DXFillTextureTX.**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
