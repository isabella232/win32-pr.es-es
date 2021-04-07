---
description: Crea una matriz de proyección ortográfica personalizada y de mano izquierda.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Función D3DXMatrixOrthoOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003908"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a>Función D3DXMatrixOrthoOffCenterLH (D3dx9math. h)

Crea una matriz de proyección ortográfica personalizada y de mano izquierda.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
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

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.

</dd> <dt>

*l* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor x mínimo del volumen de vista.

</dd> <dt>

*r* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor x máximo del volumen de vista.

</dd> <dt>

*b* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor y mínimo del volumen de vista.

</dd> <dt>

*t* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor y máximo del volumen de vista.

</dd> <dt>

*Zn* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor z mínimo del volumen de vista.

</dd> <dt>

*ZF* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor z máximo del volumen de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.

## <a name="remarks"></a>Observaciones

La función [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) es un caso especial de la función **D3DXMatrixOrthoOffCenterLH** . Para crear la misma proyección mediante **D3DXMatrixOrthoOffCenterLH**, use los siguientes valores: l =-w/2, r = w/2, b =-h/2 y t = h/2.

Todos los parámetros de la función **D3DXMatrixOrthoOffCenterLH** son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de la vista.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixOrthoOffCenterLH** se puede usar como parámetro de otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md)
</dt> <dt>

[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
