---
description: 'Función D3DXPlaneFromPointNormal (D3DX10Math.h): construye un plano a partir de un punto y un normal.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Función D3DXPlaneFromPointNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965095"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a>Función D3DXPlaneFromPointNormal (D3DX10Math.h)

Construye un plano a partir de un punto y un normal.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que es el resultado de la operación.

</dd> <dt>

*pPoint* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que define el punto utilizado para construir el plano.

</dd> <dt>

*pNormal* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, que define la normal usada para construir el plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntero a la estructura D3DXPLANE construida a partir del punto y el valor normal.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXPlaneFromPointNormal se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
