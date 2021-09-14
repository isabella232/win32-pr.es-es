---
description: Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura de cubo determinada.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Función D3DXFillCubeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072801"
---
# <a name="d3dxfillcubetexture-function"></a>Función D3DXFillCubeTexture

Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura de cubo determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Puntero a una [**interfaz IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa la textura rellena.

</dd> <dt>

*pFunction* \[ En\]
</dt> <dd>

Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Puntero a una función de evaluador proporcionada por el usuario, que se usará para calcular el valor de cada elemento de textura. La función sigue el prototipo de [LPD3DXFILL3D](lpd3dxfill3d.md).

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un bloque arbitrario de datos definidos por el usuario. Este puntero se pasará a la función proporcionada en *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este es un ejemplo que crea una función denominada ColorCubeFill, que se basa en D3DXFillCubeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
