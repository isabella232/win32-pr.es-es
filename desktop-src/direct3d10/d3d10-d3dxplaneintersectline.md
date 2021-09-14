---
description: 'Función D3DXPlaneIntersectLine (D3DX10Math.h): busca la intersección entre un plano y una línea.'
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Función D3DXPlaneIntersectLine (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965091"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>Función D3DXPlaneIntersectLine (D3DX10Math.h)

Busca la intersección entre un plano y una línea.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que identifica la intersección entre el plano y la línea especificados.

</dd> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntero al [**D3DXPLANE de origen.**](d3d10-d3dxplane.md)

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 de origen, definiendo un punto inicial de línea.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 de origen, que define un punto final de línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 que es la intersección entre el plano y la línea especificados.

## <a name="remarks"></a>Observaciones

Si la línea es paralela al plano, **se devuelve NULL.**

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXPlaneIntersectLine se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
