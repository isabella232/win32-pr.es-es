---
description: La función D3DXBoxBoundProbe (D3DX10math. h) determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Función D3DXBoxBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187818"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Función D3DXBoxBoundProbe (D3DX10math. h)

Determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMin* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que describe la esquina inferior izquierda del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina superior derecha del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pRayPosition* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, que especifica la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, que especifica la dirección del rayo. Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

**D3DXBoxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro, no solo la superficie del cuadro.

Los valores que se pasan a **D3DXBoxBoundProbe** son xmin, Xmax, YMIN, YMax, Zmin y Zmax. Por lo tanto, el siguiente código define las esquinas del cuadro de límite.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



La profundidad del cuadro de límite en la dirección z es Zmax-Zmin, en la dirección y es YMAX-YMIN y en la dirección x es XMax-xmin. Por ejemplo, con los siguientes vectores mínimo y máximo, min (-1,-1,-1) y Max (1, 1, 1), el cuadro de límite se define de la manera siguiente.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado  | D3DX10math. h |
| Biblioteca | D3DX10. lib  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
