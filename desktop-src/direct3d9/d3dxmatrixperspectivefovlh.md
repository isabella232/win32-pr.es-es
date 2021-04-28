---
description: 'Función D3DXMatrixPerspectiveFovLH (D3dx9math.h): crea una matriz de proyección de perspectiva de la izquierda basada en un campo de vista.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Función D3DXMatrixPerspectiveFovLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118353"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a>Función D3DXMatrixPerspectiveFovLH (D3dx9math.h)

Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*fovy* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Campo de vista en la dirección y, en radianes.

</dd> <dt>

*Aspecto* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Relación de aspecto, definida como ancho del espacio de vista dividido por alto.

</dd> <dt>

*zn* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Z del plano de vista cercano.

</dd> <dt>

*y* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor Z del plano de vista lejana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva con la mano izquierda.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la función **D3DXMatrixPerspectiveFovLH** se puede usar como parámetro para otra función.

Para cambiar el eje de relación de aspecto, use la fórmula de cálculo: fovy = 2 * math.atan(math.tan(fovy * 0.5) / aspect). Como alternativa, agregue variables de relación de aspecto X e Y en la estructura para escalar el espacio de vista vertical: fovy = 2 * math.atan(math.tan(fovy * 0.5) / aspectY), aspect = aspectX * aspect Y.

Esta función calcula la matriz devuelta como se muestra:


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
