---
description: Calcula el producto escalar de un plano y un vector 3D. Se supone que el parámetro w del vector es 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Función D3DXPlaneDotCoord (D3dx9math. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280240"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord función)

Calcula el producto escalar de un plano y un vector 3D. Se supone que el parámetro w del vector es 1.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Producto de punto del plano y Vector 3D.

## <a name="remarks"></a>Observaciones

Dado un plano (a, b, c, d) y un vector 3D (x, y, z), el valor devuelto de esta función es \* x + b \* y + c \* z + d \* 1. La función **D3DXPlaneDotCoord** es útil para determinar la relación del plano con una coordenada en el espacio 3D.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
