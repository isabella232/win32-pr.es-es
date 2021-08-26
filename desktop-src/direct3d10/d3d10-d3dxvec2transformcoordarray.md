---
description: 'Función D3DXVec2TransformCoordArray (D3DX10Math.h): transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado en w = 1.'
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: Función D3DXVec2TransformCoordArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d4f7e48a274b8a1b590adc76dff683019e9e0ec7ae523d16decd09421093ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989875"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a>Función D3DXVec2TransformCoordArray (D3DX10Math.h)

Transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.

</dd> <dt>

*OutStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Pasos entre vectores en el flujo de datos de salida.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntero a la matriz D3DXVECTOR2 de origen.

</dd> <dt>

*VStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Pasos entre vectores en el flujo de datos de entrada.

</dd> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntero a una [**matriz transformada D3DXVECTOR4.**](d3d10-d3dxvector4.md)

## <a name="remarks"></a>Comentarios

Esta función transforma la matriz pV (x, y, 0, 1) mediante el pM de matriz, proyectando el resultado de nuevo en w = 1.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXVec2TransformCoordArray se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
