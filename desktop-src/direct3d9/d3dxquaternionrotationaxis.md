---
description: 'Función D3DXQuaternionRotationAxis (D3dx9math.h): gira un cuaternión sobre un eje arbitrario.'
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Función D3DXQuaternionRotationAxis (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4879cec21f356399d2f98c7c3286da9ae3994c81fa64911177f287c9f0e216b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524607"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a>Función D3DXQuaternionRotationAxis (D3dx9math.h)

Gira un cuaternión sobre un eje arbitrario.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que identifica el eje sobre el que se va a girar el cuaternión.

</dd> <dt>

*Ángulo* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación, en radianes. Los ángulos se miden en el sentido de las agujas del reloj al mirar a lo largo del eje de rotación hacia el origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) girada alrededor del eje especificado.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXQuaternionRotationAxis** se puede usar como parámetro para otra función.

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
