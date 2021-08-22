---
description: Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura de volumen determinada.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Función D3DXFillVolumeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e0ef21c3fb9b5443cc488a3b6fc953953cffee6e5d0dc417dee69969907f86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123295"
---
# <a name="d3dxfillvolumetexture-function"></a>Función D3DXFillVolumeTexture

Usa una función proporcionada por el usuario para rellenar cada texel de cada nivel de mip de una textura de volumen determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Puntero a una [**interfaz IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa la textura rellena.

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

## <a name="remarks"></a>Comentarios

Si el volumen no es dinámico (porque el uso se establece en 0 cuando se crea) y se encuentra en la memoria de vídeo (el grupo de memoria establecido en \_ D3DPOOL DEFAULT), **D3DXFillVolumeTexture** producirá un error porque el volumen no se puede bloquear.

En este ejemplo se crea una función denominada ColorVolumeFill, que se basa en D3DXFillVolumeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
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

 

 
