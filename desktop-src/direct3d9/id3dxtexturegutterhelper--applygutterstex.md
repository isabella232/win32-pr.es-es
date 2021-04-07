---
description: Aplica medianils a un objeto de textura IDirect3DTexture9.
ms.assetid: e8f4a4cf-4d3b-419b-9486-08aa3bd3d8a4
title: 'ID3DXTextureGutterHelper:: ApplyGuttersTex (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c15bbc981bad3a670923e24e7d0745e91d0d9fcf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003854"
---
# <a name="id3dxtexturegutterhelperapplygutterstex-method"></a>ID3DXTextureGutterHelper:: ApplyGuttersTex (método)

Aplica medianils a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyGuttersTex(
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La [**clase 2 textura**](id3dxtexturegutterhelper.md) se generan al volver a muestrear las clases 1 y 4 textura.

El ancho y el alto de la textura deben ser los mismos que los devueltos por [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) y [**ID3DXTextureGutterHelper:: getHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
