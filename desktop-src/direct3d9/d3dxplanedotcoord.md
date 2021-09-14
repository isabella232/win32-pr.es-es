---
description: Calcula el producto de puntos de un plano y un vector 3D. Se supone que el parámetro w del vector es 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Función D3DXPlaneDotCoord (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974301"
---
# <a name="d3dxplanedotcoord-function"></a>Función D3DXPlaneDotCoord

Calcula el producto de puntos de un plano y un vector 3D. Se supone que el parámetro w del vector es 1.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a una estructura [**D3DXPLANE de**](d3dxplane.md) origen.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Producto de punto del plano y vector 3D.

## <a name="remarks"></a>Observaciones

Dado un plano (a, b, c, d) y un vector 3D (x, y, z), el valor devuelto de esta función es \* x + b y + c z + d \* \* \* 1. La **función D3DXPlaneDotCoord** es útil para determinar la relación del plano con una coordenada en el espacio 3D.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
