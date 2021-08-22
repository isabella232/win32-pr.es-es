---
description: Crea una matriz de identidad.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Función D3DXMatrixIdentity (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce7d891eb446372b749c7085a37e80241c52f1cf862a61b3fc9edeb544776b2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044903"
---
# <a name="d3dxmatrixidentity-function"></a>Función D3DXMatrixIdentity

Crea una matriz de identidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es la matriz de identidad.

## <a name="remarks"></a>Comentarios

La matriz de identidad es una matriz en la que todos los coeficientes son 0 excepto \[ los coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, \] que se establecen en 1. La matriz de identidad es especial en que, cuando se aplica a los vértices, no se modifican. La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de vértice para crear rotaciones, traducciones y cualquier otra transformación que se pueda representar mediante una matriz de 4 x4.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXMatrixIdentity** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




