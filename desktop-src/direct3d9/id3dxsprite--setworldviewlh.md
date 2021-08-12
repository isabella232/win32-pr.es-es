---
description: Establece la transformación de la vista del mundo de la izquierda para un sprite. Se requiere una llamada a este método antes de agrupar u ordenar sprites.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: Método ID3DXSprite::SetWorldViewLH (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67ee276b90629a18f93bd9a26879e8a7ad62d71ae46baf2d2c0a6bfba82a53a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292577"
---
# <a name="id3dxspritesetworldviewlh-method"></a>Método ID3DXSprite::SetWorldViewLH

Establece la transformación de la vista del mundo de la izquierda para un sprite. Se requiere una llamada a este método antes de agrupar u ordenar sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWorld* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación mundial. Si **es NULL,** la matriz de identidad se usa para la transformación del mundo.

</dd> <dt>

*pView* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a [**D3DXMATRIX que**](d3dxmatrix.md) contiene una transformación de vista. Si **es NULL,** la matriz de identidad se usa para la transformación de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

Se requiere una llamada a este método (o a [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) si el sprite se representará con el valor de marca [BACKTOFRONT D3DXSprite \_ \_ HISTOGRAM,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ FRONTTOBACK o \_ D3DXSprite \_ \_ SORT DEPTH \_ BACKTOFRONT en \_ [**ID3DXSprite::Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




