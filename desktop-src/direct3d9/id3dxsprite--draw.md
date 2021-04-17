---
description: Agrega un objeto Sprite a la lista de objetos Sprite por lotes.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D método RAW (D3dx9core. h)
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
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718477"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite::D método sin formato

Agrega un objeto Sprite a la lista de objetos Sprite por lotes.

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

*pTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de Sprite.

</dd> <dt>

*pSrcRect* \[ de\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que indica la parte de la textura de origen que se va a usar para el sprite. Si este parámetro es **null**, se usa la imagen de origen completa para el sprite.

</dd> <dt>

*pCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica el centro del objeto Sprite. Si este argumento es **null**, se usa el punto (0,0), que es la esquina superior izquierda.

</dd> <dt>

*pPosition* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica la posición del objeto Sprite. Si este argumento es **null**, se usa el punto (0,0), que es la esquina superior izquierda.

</dd> <dt>

*Color* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Tipo [**D3DCOLOR**](d3dcolor.md) . El color y los canales alfa se modulan con este valor. Un valor de 0xFFFFFFFF mantiene el color de origen y los datos alfa originales. Use la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para ayudar a generar este color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Para escalar, girar o traducir un Sprite, llame a [**ID3DXSprite:: SetTransform**](id3dxsprite--settransform.md) con una matriz que contenga los valores Scale, Rotate y translate (SRT) antes de llamar a ID3DXSprite::D RAW. Para obtener información sobre cómo establecer los valores de SRT en una matriz, vea [transformaciones de matriz](transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
