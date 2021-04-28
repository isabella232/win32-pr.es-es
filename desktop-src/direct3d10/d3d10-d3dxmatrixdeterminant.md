---
description: 'Función D3DXMatrixDeterminant (D3DX10Math.h): devuelve el determinante de una matriz.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Función D3DXMatrixDeterminant (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103463"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a>Función D3DXMatrixDeterminant (D3DX10Math.h)

Devuelve el determinante de una matriz.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pM* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a la estructura D3DXMATRIX de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Devuelve el determinante de la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
