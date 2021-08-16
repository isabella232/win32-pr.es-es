---
description: Crea un objeto de controlador de animación.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Función D3DXCreateAnimationController (D3dx9anim.h)
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
ms.openlocfilehash: 0edda07aa5ae443a268bd5df50a154aa2a7f2ec9ca1873dc486e8e46532ae468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526640"
---
# <a name="d3dxcreateanimationcontroller-function"></a>Función D3DXCreateAnimationController

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

*MaxNumAnimationOutputs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de salidas de animación que el controlador puede admitir.

</dd> <dt>

*MaxNumAnimationSets* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animación que se pueden mezclar.

</dd> <dt>

*MaxNumTracks* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animación que se pueden mezclar simultáneamente.

</dd> <dt>

*MaxNumEvents* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de eventos pendientes que admitirá el controlador.

</dd> <dt>

*ppAnimController* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Puntero al objeto de controlador de animación creado. Vea [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Un controlador de animación controla un mezclador de animación. El controlador agrega métodos para modificar los parámetros de combinación a lo largo del tiempo para permitir transiciones fluidas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
