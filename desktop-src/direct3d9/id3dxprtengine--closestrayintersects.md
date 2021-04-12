---
description: Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine:: ClosestRayIntersects (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280479"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>ID3DXPRTEngine:: ClosestRayIntersects (método)

Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Si se encuentra una intersección, el método devuelve el índice de la superficie de malla más cercana que el rayo y las coordenadas Barycentric del punto de intersección.

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

*pRayPos* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.

</dd> <dt>

*pRayDir* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección normalizada del rayo.

</dd> <dt>

*pFaceIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al índice de la cara de la malla actual que se alcanza primero por el rayo dado, en función de la pila de todas las caras de la malla del bloqueador delante de la malla actual.

</dd> <dt>

*PU* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posicionamiento de Barycentric, U, para el vértice 0 del triángulo.

</dd> <dt>

*PV* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una coordenada de posicionamiento de Barycentric, V, para el vértice 1 del triángulo.

</dd> <dt>

*pDist* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a la distancia del punto de intersección a lo largo del rayo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con la malla actual; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer las distancias mínima y máxima de intersección con el rayo.

La coordenada Barycentric del tercer vértice (vértice 2) del triángulo es 1-(U + V).

Este método se ejecuta más lentamente que [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Use **ID3DXPRTEngine:: ShadowRayIntersects** si no se necesita la ubicación del punto de intersección.

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
