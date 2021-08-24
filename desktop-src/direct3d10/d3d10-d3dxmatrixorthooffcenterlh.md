---
description: 'Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h): crea una matriz de proyección ortográfica a la izquierda personalizada.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4396f060d33efef454e87d8594c2b4ca29e46cbcbc08151cacaa76a7a4965735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852855"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a>Función D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)

Crea una matriz de proyección ortográfica personalizada y a la izquierda.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*l* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor x mínimo del volumen de vista.

</dd> <dt>

*r* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor x máximo del volumen de vista.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Y mínimo del volumen de vista.

</dd> <dt>

*t* \[ in\]
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

Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Comentarios

[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) es un caso especial de la función D3DXMatrixOrthoOffCenterLH. Para crear la misma proyección mediante D3DXMatrixOrthoOffCenterLH, use los valores siguientes:

l = -w/2,

r = w/2,

b = -h/2 y

t = h/2.

Todos los parámetros de la función D3DXMatrixOrthoOffCenterLH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de vista.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXMatrixOrthoOffCenterLH se puede usar como parámetro para otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
