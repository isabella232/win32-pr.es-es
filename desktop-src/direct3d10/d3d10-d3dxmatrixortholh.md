---
description: 'Función D3DXMatrixOrthoLH (D3DX10Math.h): crea una matriz de proyección ortográfica de mano izquierda.'
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Función D3DXMatrixOrthoLH (D3DX10Math.h)
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
ms.openlocfilehash: b8b1b64818f4c0903897dc5b1de83b1aaa963461e909edbbfc9ba8dc4a1f10f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282965"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>Función D3DXMatrixOrthoLH (D3DX10Math.h)

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

Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ancho del volumen de vista.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Alto del volumen de vista.

</dd> <dt>

*zn* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z mínimo del volumen de vista que se conoce como z-near.

</dd> <dt>

*y* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z máximo del volumen de vista al que se hace referencia como z-far.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Comentarios

Todos los parámetros de la función D3DXMatrixOrthoLH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de vista.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la función D3DXMatrixOrthoLH se puede usar como parámetro para otra función.

Esta función usa la siguiente fórmula para calcular la matriz devuelta.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
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

 

 
