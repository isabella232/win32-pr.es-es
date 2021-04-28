---
description: 'Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h): crea un cuaternión con el yaw, pitch y roll dados.'
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118003"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>Función D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)

Crea un cuaternión con el guión, el lanzamiento y el lanzamiento dados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*Yaw* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Eje Y alrededor del eje Y, en radianes.

</dd> <dt>

*Pitch* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Inclinar alrededor del eje X, en radianes.

</dd> <dt>

*Roll* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Revierte el eje Z, en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) con el guión, el paso y el lanzamiento especificados.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la función **D3DXQuaternionRotationYawPitchRoll** se puede usar como parámetro para otra función.

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

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
