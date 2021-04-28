---
description: 'Función D3DXMatrixRotationZ (D3DX10Math.h): crea una matriz que gira alrededor del eje Z.'
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: Función D3DXMatrixRotationZ (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b952e310dd463d07a35fb294c4a50168361658a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108943"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a>Función D3DXMatrixRotationZ (D3DX10Math.h)

Crea una matriz que gira alrededor del eje Z.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Ángulo* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación, en radianes. Los ángulos se miden en el sentido de las agujas del reloj cuando se ven desde el eje de rotación (lado positivo) hacia el origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX girada alrededor del eje Z.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXMatrixRotationZ se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
