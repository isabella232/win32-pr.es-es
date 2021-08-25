---
description: Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura determinada.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Función D3DXFillTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28df3b7396ea0c34c39a87d2285f565f25d6ff6dc89dcfb8613890e79c4c5cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849775"
---
# <a name="d3dxfilltexture-function"></a>Función D3DXFillTexture

Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura rellena.

</dd> <dt>

*pFunction* \[ En\]
</dt> <dd>

Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Puntero a una función de evaluador proporcionada por el usuario, que se usará para calcular el valor de cada elemento de textura. La función sigue el prototipo de [LPD3DXFILL2D.](lpd3dxfill2d.md)

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un bloque arbitrario de datos definidos por el usuario. Este puntero se pasará a la función proporcionada en *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este es un ejemplo que crea una función denominada ColorFill, que se basa en D3DXFillTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
