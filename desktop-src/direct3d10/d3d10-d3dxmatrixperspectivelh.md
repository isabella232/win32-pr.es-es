---
description: 'Función D3DXMatrixPerspectiveLH (D3DX10Math.h): crea una matriz de proyección de perspectiva a la izquierda'
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Función D3DXMatrixPerspectiveLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ea9b91fe926ecbab34fa65fd6c21f852501b6d515acaf8b9aaa5b8971a27c37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304509"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a>Función D3DXMatrixPerspectiveLH (D3DX10Math.h)

Crea una matriz de proyección de perspectiva izquierda

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
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

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ancho del volumen de vista en el plano de vista cercano.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Alto del volumen de vista en el plano de vista cercano.

</dd> <dt>

*zn* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Z del plano de vista cercano.

</dd> <dt>

*y* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Z del plano de vista lejano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva a la izquierda.

## <a name="remarks"></a>Comentarios

Todos los parámetros de la función D3DXMatrixPerspectiveLH son distancias en el espacio de la cámara. Los parámetros describen las dimensiones del volumen de vista.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXMatrixPerspectiveLH se puede usar como parámetro para otra función.

Esta función usa la siguiente fórmula para calcular la matriz devuelta.


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
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

 

 
