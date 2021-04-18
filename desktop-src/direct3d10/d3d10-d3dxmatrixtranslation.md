---
description: Cree una matriz de traslación.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: Función D3DXMatrixTranslation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721525"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a>Función D3DXMatrixTranslation (D3DX10Math. h)

Cree una matriz de traslación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matriz que se convertirá en una matriz de traslación. Vea [**D3DXMATRIX**](d3d10-d3dxmatrix.md).

</dd> <dt>

*x* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Componente x de la traducción.

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Componente y de la traducción.

</dd> <dt>

*z* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Componente z de la traducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matriz de traslación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
