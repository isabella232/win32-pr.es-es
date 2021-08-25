---
description: Aplica los canales a un objeto de textura IDirect3DTexture9.
ms.assetid: e8f4a4cf-4d3b-419b-9486-08aa3bd3d8a4
title: Método ID3DXTextureGutterHelper::ApplyGuttersTex (D3DX9Mesh.h)
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
ms.openlocfilehash: a289eede9b55a3560408caf71a20aaf1811bb82780488b886cade8aaa5e96d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893245"
---
# <a name="id3dxtexturegutterhelperapplygutterstex-method"></a>Método ID3DXTextureGutterHelper::ApplyGuttersTex

Aplica los canales a un objeto de textura [**IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyGuttersTex(
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un [**objeto de textura IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTPLANTDRAWING, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

[**Los elementos de textura de clase 2**](id3dxtexturegutterhelper.md) se generan mediante el remuestreo de las clases 1 y 4.

El ancho y el alto de la textura deben ser los mismos que los devueltos por [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
