---
description: Crea un objeto Sprite que está asociado a un dispositivo determinado. Los objetos Sprite se usan para dibujar imágenes 2D en la pantalla.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Función D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718215"
---
# <a name="d3dxcreatesprite-function"></a>D3DXCreateSprite función)

Crea un objeto Sprite que está asociado a un dispositivo determinado. Los objetos Sprite se usan para dibujar imágenes 2D en la pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al Sprite.

</dd> <dt>

*ppSprite* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Dirección de un puntero a una interfaz [**ID3DXSprite**](id3dxsprite.md) . Esta interfaz permite al usuario tener acceso a las funciones de Sprite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta interfaz se puede usar para dibujar dos imágenes dimensionales en el espacio de pantalla del dispositivo asociado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
