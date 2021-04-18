---
description: Proyecta una matriz (x, y, z, 0) del espacio de objeto en el espacio de la pantalla.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Función D3DXVec3ProjectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718535"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a>Función D3DXVec3ProjectArray (D3dx9math. h)

Proyecta una matriz (x, y, z, 0) del espacio de objeto en el espacio de la pantalla.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

Retrasos  \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Intervalo entre vectores en el flujo de datos de salida.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> <dt>

*VStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Intervalo entre vectores en el flujo de datos de entrada.

</dd> <dt>

*pViewport* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla.

</dd> <dt>

*pProjection* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de proyección.

</dd> <dt>

*pView* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de la vista.

</dd> <dt>

*pWorld* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz universal.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la matriz proyectada desde el espacio de objeto hasta el espacio de la pantalla.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec3ProjectArray** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 
