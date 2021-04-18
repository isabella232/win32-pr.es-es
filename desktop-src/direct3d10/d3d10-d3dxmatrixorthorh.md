---
description: Crea una matriz de proyección ortográfica de mano derecha.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Función D3DXMatrixOrthoRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721494"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a>Función D3DXMatrixOrthoRH (D3DX10Math. h)

Crea una matriz de proyección ortográfica de mano derecha.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.

</dd> <dt>

*w* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ancho del volumen de vista.

</dd> <dt>

*h* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Alto del volumen de vista.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.

## <a name="remarks"></a>Observaciones

Todos los parámetros de la función D3DXMatrixOrthoRH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de la vista.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXMatrixOrthoRH se puede usar como parámetro de otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
