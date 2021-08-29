---
description: Aplica los medianes a un objeto de búfer ID3DXPRTBuffer.
ms.assetid: db09aa50-3175-4588-8433-dad6bd37cf0c
title: Método ID3DXTextureGutterHelper::ApplyGuttersPRT (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersPRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fcfb4829774dc4fc754b566f531d6e4aff76751ae2d7eb13bc17e0c434b9cff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674645"
---
# <a name="id3dxtexturegutterhelperapplyguttersprt-method"></a>Método ID3DXTextureGutterHelper::ApplyGuttersPRT

Aplica los medianes a un objeto de búfer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyGuttersPRT(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un [**objeto de búfer ID3DXPRTBuffer.**](id3dxprtbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

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

 

 




