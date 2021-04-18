---
description: Crea una matriz de proyección ortográfica personalizada y de mano derecha.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Función D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7de5e4b3a872ea7466840e511fc0a57448861b55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718394"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a>Función D3DXMatrixOrthoOffCenterRH (D3dx9math. h)

Crea una matriz de proyección ortográfica personalizada y de mano derecha.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
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

La función [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) es un caso especial de la función **D3DXMatrixOrthoOffCenterRH** . Para crear la misma proyección mediante **D3DXMatrixOrthoOffCenterRH**, use los siguientes valores: l =-w/2, r = w/2, b =-h/2 y t = h/2.

Todos los parámetros de la función **D3DXMatrixOrthoOffCenterRH** son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de la vista.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixOrthoOffCenterRH** se puede usar como parámetro de otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
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

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
