---
description: Crea una matriz de proyección ortográfica a la izquierda.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Función D3DXMatrixOrthoLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280469"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>Función D3DXMatrixOrthoLH (D3DX10Math. h)

Crea una matriz de proyección ortográfica a la izquierda.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
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

Valor z mínimo del volumen de vista, al que se hace referencia como z-near.

</dd> <dt>

*ZF* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor z máximo del volumen de vista, al que se hace referencia como z-lejano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.

## <a name="remarks"></a>Observaciones

Todos los parámetros de la función D3DXMatrixOrthoLH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de la vista.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXMatrixOrthoLH se puede usar como parámetro de otra función.

Esta función usa la fórmula siguiente para calcular la matriz devuelta.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
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

 

 
