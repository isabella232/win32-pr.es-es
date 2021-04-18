---
description: Normaliza los coeficientes del plano para que el plano normal tenga una longitud de unidad.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Función D3DXPlaneNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707733"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Función D3DXPlaneNormalize (D3dx9math. h)

Normaliza los coeficientes del plano para que el plano normal tenga una longitud de unidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.

</dd> <dt>

*PP* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura de [**D3DXPLANE**](d3dxplane.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a una estructura [**D3DXPLANE**](d3dxplane.md) que representa el normal del plano.

## <a name="remarks"></a>Observaciones

Esta función normaliza un plano para que \| a, b, c \| = = 1.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, esta función se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




