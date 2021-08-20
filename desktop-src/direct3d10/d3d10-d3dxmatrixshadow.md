---
description: 'Función D3DXMatrixShadow (D3DX10Math.h): crea una matriz que aplana la geometría en un plano.'
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: Función D3DXMatrixShadow (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e9a831eae416986dc4111e9928ffe9c2b09119fb4595119174d745aedbb6ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118809897"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a>Función D3DXMatrixShadow (D3DX10Math.h)

Crea una matriz que aplana la geometría en un plano.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*pLight* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que describe la posición de la luz.

</dd> <dt>

*pPlane* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntero al [**D3DXPLANE de origen.**](d3d10-d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que aplana la geometría en un plano.

## <a name="remarks"></a>Comentarios

La **función D3DXMatrixShadow** aplana la geometría en un plano, como si se hubiera convertido una sombra a partir de una luz.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXMatrixShadow** se puede usar como parámetro para otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Si el componente w de la luz es 0, el rayo del origen a la luz representa una luz direccional. Si es 1, la luz es una luz de punto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
