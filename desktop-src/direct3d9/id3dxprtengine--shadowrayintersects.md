---
description: Usa un seguimiento de rayos eficaz en simulaciones de transferencia de radiancia precalcaladas (PRT) para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en la sombra.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: Método ID3DXPRTEngine::ShadowRayIntersects (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072755"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>Método ID3DXPRTEngine::ShadowRayIntersects

Usa un seguimiento de rayos eficaz en simulaciones de transferencia de radiancia precalcaladas (PRT) para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en la sombra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con la malla actual; de lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Observaciones

Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer las distancias mínima y máxima de intersección con el rayo.

Este método se ejecuta más rápido que [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
