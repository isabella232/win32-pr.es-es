---
description: Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura determinada.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Función D3DXFillTexture (D3dx9tex. h)
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
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362572"
---
# <a name="d3dxfilltexture-function"></a>D3DXFillTexture función)

Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura determinada.

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

*pTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura rellenada.

</dd> <dt>

*pFunction* \[ de\]
</dt> <dd>

Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Puntero a una función evaluadora proporcionada por el usuario, que se utilizará para calcular el valor de cada textura. La función sigue el prototipo de [LPD3DXFILL2D](lpd3dxfill2d.md).

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un bloque arbitrario de datos definidos por el usuario. Este puntero se pasará a la función proporcionada en *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este es un ejemplo en el que se crea una función denominada ColorFill, que se basa en D3DXFillTexture.


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
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
