---
description: Calcula el producto escalar de un plano y un vector 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Función D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717558"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot función)

Calcula el producto escalar de un plano y un vector 4D.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PP* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a una estructura de [**D3DXPLANE**](d3dxplane.md) de origen.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Producto de punto del plano y el vector 4D.

## <a name="remarks"></a>Observaciones

Dado un plano (a, b, c, d) y un vector 4D (x, y, z, w), el valor devuelto de esta función es \* x + b \* y + c \* z + d \* w. La función **D3DXPlaneDot** es útil para determinar la relación del plano con una coordenada homogénea. Por ejemplo, esta función se puede usar para determinar si una coordenada determinada está en un plano determinado o en qué lado de un plano determinado se encuentra una coordenada determinada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
