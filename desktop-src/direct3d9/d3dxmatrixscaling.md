---
description: Crea una matriz que se escala a lo largo del eje x, el eje y y el eje z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Función D3DXMatrixScaling (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717568"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a>Función D3DXMatrixScaling (D3dx9math. h)

Crea una matriz que se escala a lo largo del eje x, el eje y y el eje z.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*SX* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de escala que se aplica a lo largo del eje x.

</dd> <dt>

*SY* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de escala que se aplica a lo largo del eje y.

</dd> <dt>

*SZ* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de escala que se aplica a lo largo del eje z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la transformación de escala [**D3DXMATRIX**](d3dxmatrix.md).

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixScaling** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
