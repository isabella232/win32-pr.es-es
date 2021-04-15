---
description: Crea un objeto de controlador de animación.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Función D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707868"
---
# <a name="d3dxcreateanimationcontroller-function"></a>D3DXCreateAnimationController función)

Crea un objeto de controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxNumAnimationOutputs* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de salidas de animación que el controlador puede admitir.

</dd> <dt>

*MaxNumAnimationSets* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animaciones que se pueden mezclar.

</dd> <dt>

*MaxNumTracks* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animaciones que se pueden mezclar simultáneamente.

</dd> <dt>

*MaxNumEvents* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de eventos pendientes que el controlador admitirá.

</dd> <dt>

*ppAnimController* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Puntero al objeto de controlador de animación creado. Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Un controlador de animación controla un mezclador de animación. El controlador agrega métodos para modificar los parámetros de fusión a lo largo del tiempo para permitir transiciones suaves.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
