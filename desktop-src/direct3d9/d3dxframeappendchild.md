---
description: Agrega un marco secundario a un marco.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Función D3DXFrameAppendChild (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072789"
---
# <a name="d3dxframeappendchild-function"></a>Función D3DXFrameAppendChild

Agrega un marco secundario a un marco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrameParent* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntero al nodo primario.

</dd> <dt>

*pFrameChild* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Puntero al nodo secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




