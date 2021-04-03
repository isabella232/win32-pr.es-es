---
description: Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en sombra.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine:: ShadowRayIntersects (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083747"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>ID3DXPRTEngine:: ShadowRayIntersects (método)

Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en sombra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con la malla actual; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer las distancias mínima y máxima de intersección con el rayo.

Este método se ejecuta más rápido que [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
