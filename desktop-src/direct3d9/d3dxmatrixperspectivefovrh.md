---
description: 'Función D3DXMatrixPerspectiveFovRH (D3dx9math.h): crea una matriz de proyección de perspectiva con la derecha basada en un campo de vista.'
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Función D3DXMatrixPerspectiveFovRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8860a5d9fed13e8acdedfe67ed94a97911a6de0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567849"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a>Función D3DXMatrixPerspectiveFovRH (D3dx9math.h)

Crea una matriz de proyección de perspectiva a la derecha basada en un campo visual.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
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

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva con la mano derecha.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la función **D3DXMatrixPerspectiveFovRH** se puede usar como parámetro para otra función.

Para cambiar el eje de relación de aspecto, use la fórmula de cálculo: fovy = 2 * math.atan(math.tan(fovy * 0.5) / aspect). Como alternativa, agregue variables de relación de aspecto X e Y en la estructura para escalar el espacio de vista vertical: fovy = 2 * math.atan(math.tan(fovy * 0.5) / aspectY), aspect = aspectX * aspect Y.

Esta función calcula la matriz devuelta como se muestra.


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
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

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
