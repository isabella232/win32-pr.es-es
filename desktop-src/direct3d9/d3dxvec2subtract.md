---
description: Resta dos vectores 2D.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: Función D3DXVec2Subtract (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7570a3dcf0b6640724c274738a226e1a34cf6a651be69ef0851391074a494d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119025"
---
# <a name="d3dxvec2subtract-function"></a>Función D3DXVec2Subtract

Resta dos vectores 2D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es la diferencia de dos vectores.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec2Subtract** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Agregue**](d3dxvec2add.md)
</dt> <dt>

[**D3DXVec2Scale**](d3dxvec2scale.md)
</dt> </dl>

 

 




