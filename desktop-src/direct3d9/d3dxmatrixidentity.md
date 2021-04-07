---
description: Crea una matriz de identidad.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Función D3DXMatrixIdentity (D3dx9math. h)
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
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003764"
---
# <a name="d3dxmatrixidentity-function"></a>D3DXMatrixIdentity función)

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

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es la matriz de identidad.

## <a name="remarks"></a>Observaciones

La matriz de identidad es una matriz en la que todos los coeficientes son 0 excepto los \[ \] \[ coeficientes 1, 1 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , que se establecen en 1. La matriz de identidad es especial, ya que, cuando se aplica a los vértices, no cambian. La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de los vértices para crear rotaciones, traducciones y cualquier otra transformación que pueda representarse mediante una matriz de 4 x4.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixIdentity** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




