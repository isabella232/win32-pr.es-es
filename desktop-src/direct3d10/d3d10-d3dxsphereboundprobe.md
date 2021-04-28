---
description: 'Función D3DXSphereBoundProbe (D3DX10math.h): determina si un rayo forma una intersección con el volumen del cuadro de límite de una esfera.'
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Función D3DXSphereBoundProbe (D3DX10math.h)
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
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108473"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>Función D3DXSphereBoundProbe (D3DX10math.h)

Determina si un rayo forma una intersección con el volumen del rectángulo delimitador de una esfera.

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

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la coordenada central de la esfera.

</dd> <dt>

*Radio* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio de la esfera.

</dd> <dt>

*pRayPosition* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la dirección del rayo. Este vector no debe ser (0,0,0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con el volumen del cuadro de límite de la esfera. De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

**D3DXSphereBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección de la esfera, no solo con la superficie de la esfera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
