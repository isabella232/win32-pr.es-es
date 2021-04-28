---
description: 'Función D3DXQuaternionToAxisAngle (D3DX10Math.h): calcula el eje y el ángulo de rotación de un cuaternión.'
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Función D3DXQuaternionToAxisAngle (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108703"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>Función D3DXQuaternionToAxisAngle (D3DX10Math.h)

Calcula el eje y el ángulo de rotación de un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntero al [**D3DXQUATERNION de origen.**](d3d10-d3dxquaternion.md)

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Esta función devuelve un puntero a [**un D3DXVECTOR3**](d3d10-d3dxvector3.md) que identifica el eje de rotación del cuaternión.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Esta función devuelve un puntero a un valor FLOAT que identifica el ángulo de rotación del cuaternión en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
