---
description: Agrega un sprite a la lista de sprites por lotes.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: Método ID3DXSprite::D raw (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d453a2e03538b7601b5f73033a4749430e8812ef317a90816cac220e61695279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747375"
---
# <a name="id3dxspritedraw-method"></a>Método ID3DXSprite::D raw

Agrega un sprite a la lista de sprites por lotes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una [**interfaz IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura del sprite.

</dd> <dt>

*pSrcRect* \[ En\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que indica la parte de la textura de origen que se va a usar para el sprite. Si este parámetro es **NULL,** se usa toda la imagen de origen para el sprite.

</dd> <dt>

*pCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica el centro del sprite. Si este argumento es **NULL,** se usa el punto (0,0,0), que es la esquina superior izquierda.

</dd> <dt>

*pPosition* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica la posición del sprite. Si este argumento es **NULL,** se usa el punto (0,0,0), que es la esquina superior izquierda.

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Tipo D3DCOLOR.**](d3dcolor.md) Los canales alfa y de color se modularán con este valor. Un valor de 0xFFFFFFFF mantiene el color de origen original y los datos alfa. Use la [**macro D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para ayudar a generar este color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Para escalar, girar o traducir un sprite, llame a [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) con una matriz que contenga los valores de escala, rotación y traducción (SRT), antes de llamar a ID3DXSprite::D raw. Para obtener información sobre cómo establecer valores de SRT en una matriz, vea [Transformaciones de matriz.](transforms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
