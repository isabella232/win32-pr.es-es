---
description: 'Función D3DXSphereBoundProbe (D3DX9Mesh.h): determina si un rayo forma una intersección con el volumen del rectángulo de selección de una esfera.'
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Función D3DXSphereBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85dbd46233176d65e7e7abbf0eb266c81868ceba7e67e3257bf902d1775d6a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731158"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>Función D3DXSphereBoundProbe (D3DX9Mesh.h)

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

*pCenter* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la coordenada central de la esfera.

</dd> <dt>

*Radio* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio de la esfera.

</dd> <dt>

*pRayPosition* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la dirección del rayo. Este vector no debe ser (0,0,0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera. De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo con la superficie de la esfera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
