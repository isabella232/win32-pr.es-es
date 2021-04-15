---
description: Devuelve el factor determinante de una matriz.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Función D3DXMatrixDeterminant (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362441"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a>Función D3DXMatrixDeterminant (D3dx9math. h)

Devuelve el factor determinante de una matriz.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Devuelve el factor determinante de la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
