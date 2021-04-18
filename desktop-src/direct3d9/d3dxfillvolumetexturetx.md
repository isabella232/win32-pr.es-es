---
description: Usa una función de lenguaje de sombreado de alto nivel (HLSL) compilada para rellenar cada textura de cada nivel de mipmap de una textura.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Función D3DXFillVolumeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678791"
---
# <a name="d3dxfillvolumetexturetx-function"></a>D3DXFillVolumeTextureTX función)

Usa una función de lenguaje de sombreado de alto nivel (HLSL) compilada para rellenar cada textura de cada nivel de mipmap de una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Puntero a un objeto [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa la textura que se va a rellenar.

</dd> <dt>

*pTextureShader* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Puntero a un objeto de sombreador de textura de [**ID3DXTextureShader**](id3dxtextureshader.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

El destino de la textura debe ser una función HLSL que tenga la semántica siguiente:

-   Un parámetro de entrada debe utilizar una semántica de posición.
-   Un parámetro de entrada debe utilizar una semántica PSIZE.
-   La función debe devolver un parámetro que use la semántica de COLOR.

Los parámetros de entrada pueden estar en cualquier orden. Para obtener un ejemplo, consulte [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
