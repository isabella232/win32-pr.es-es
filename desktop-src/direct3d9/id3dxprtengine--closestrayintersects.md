---
description: Usa un seguimiento eficaz de rayos en simulaciones de transferencia de radiancia precalutadas (PRT) para determinar si un rayo forma una intersección con una malla.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: Método ID3DXPRTEngine::ClosestRayIntersects (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974767"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>Método ID3DXPRTEngine::ClosestRayIntersects

Usa un seguimiento eficaz de rayos en simulaciones de transferencia de radiancia precalutadas (PRT) para determinar si un rayo forma una intersección con una malla. Si se encuentra una intersección, el método devuelve el índice de la cara de malla más cercana alcanzado por el rayo y las coordenadas baricéntricas del punto de intersección.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRayPos* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando el punto donde comienza el rayo.

</dd> <dt>

*pRayDir* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la dirección normalizada del rayo.

</dd> <dt>

*pFaceIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al índice de la cara de malla actual que se encuentra primero con el rayo dado, en función del apilamiento de todas las caras de malla de bloqueador delante de la malla actual.

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posición centrada en barras, U, para el vértice 0 del triángulo.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posición centrada en barras, V, para el vértice 1 del triángulo.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a la distancia del punto de intersección a lo largo del rayo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con la malla actual; de lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Observaciones

Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer distancias mínimas y máximas de intersección con el rayo.

La coordenada centrada en barras del tercer vértice (vértice 2) del triángulo es 1 - ( U + V ).

Este método se ejecuta más lentamente [**que ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Use **ID3DXPRTEngine::ShadowRayIntersects** si no se necesita la ubicación del punto de intersección.

Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
