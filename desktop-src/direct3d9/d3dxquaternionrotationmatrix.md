---
description: 'Función D3DXQuaternionRotationMatrix (D3dx9math.h): compila un cuaternión a partir de una matriz de rotación.'
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Función D3DXQuaternionRotationMatrix (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3ad57cc34a7b16b15c49195e39004094a33e2a168c7a3ff2f5f7eb77c267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988455"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a>Función D3DXQuaternionRotationMatrix (D3dx9math.h)

Crea un cuaternión a partir de una matriz de rotación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) creada a partir de una matriz de rotación.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXQuaternionRotationMatrix** se puede usar como parámetro para otra función.

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




