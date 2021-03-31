---
description: Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Función D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821335"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>Función D3DXSphereBoundProbe (D3DX10math. h)

Determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCenter* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la coordenada central de la esfera.

</dd> <dt>

*RADIUS* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Radio de la esfera.

</dd> <dt>

*pRayPosition* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la dirección del rayo. Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo la superficie de la esfera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
