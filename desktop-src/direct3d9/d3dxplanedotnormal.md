---
description: Calcula el producto de punto de un plano y un vector 3D. Se supone que el parámetro w del vector es 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Función D3DXPlaneDotNormal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95259cd880d22678ef91765d38c68e85f5f0443ac7058de4b3a2dd078d7ad55a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910522"
---
# <a name="d3dxplanedotnormal-function"></a>Función D3DXPlaneDotNormal

Calcula el producto de punto de un plano y un vector 3D. Se supone que el parámetro w del vector es 0.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXPlaneDotNormal(
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

## <a name="remarks"></a>Comentarios

Dado un plano (a, b, c, d) y un vector 3D (x, y, z), el valor devuelto de esta función es \* x + b y + c z + d \* \* \* 0. La **función D3DXPlaneDotNormal** es útil para calcular el ángulo entre la normal del plano y otra normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
