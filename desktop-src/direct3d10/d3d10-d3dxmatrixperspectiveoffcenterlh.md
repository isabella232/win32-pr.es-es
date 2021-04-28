---
description: 'Función D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h): crea una matriz de proyección de perspectiva personalizada con la mano izquierda.'
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: Función D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1116e24b48c9090739511894d28031ca921ed6ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109053"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a>Función D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h)

Crea una matriz de proyección de perspectiva a la izquierda personalizada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*l* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor X mínimo del volumen de vista.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor x máximo del volumen de vista.

</dd> <dt>

*b* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Y mínimo del volumen de vista.

</dd> <dt>

*t* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Y máximo del volumen de vista.

</dd> <dt>

*zn* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z mínimo del volumen de vista.

</dd> <dt>

*y* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z máximo del volumen de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva personalizada y con la mano izquierda.

## <a name="remarks"></a>Comentarios

Todos los parámetros de la función D3DXMatrixPerspectiveOffCenterLH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de vista.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXMatrixPerspectiveOffCenterLH se puede usar como parámetro para otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
