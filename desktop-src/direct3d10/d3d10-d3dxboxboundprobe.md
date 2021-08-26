---
description: La función D3DXBoxBoundProbe (D3DX10math.h) determina si un rayo forma una intersección con el volumen del rectángulo delimitador de un cuadro.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Función D3DXBoxBoundProbe (D3DX10math.h)
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
ms.openlocfilehash: ae06fa2e42e99dc64a0684844e341f26e30d797e75d3a822aa0b1ddee690703d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028815"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Función D3DXBoxBoundProbe (D3DX10math.h)

Determina si un rayo forma una intersección con el volumen del rectángulo delimitador de un cuadro.

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

*pMin* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que describe la esquina inferior izquierda del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la esquina superior derecha del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pRayPosition* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, especificando la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3, especificando la dirección del rayo. Este vector no debe ser (0,0,0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si el rayo forma una intersección con el volumen del rectángulo delimitador del cuadro. De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

**D3DXBoxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo delimitador del cuadro, no solo con la superficie del cuadro.

Los valores pasados a **D3DXBoxBoundProbe** son xmin, xmax, ymin, ymax, zmin y zmax. Por lo tanto, lo siguiente define las esquinas del cuadro de límite.


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



La profundidad del rectángulo delimitador en la dirección z es zmax - zmin, en la dirección y es ymax - ymin, y en la dirección x es xmax - xmin. Por ejemplo, con los siguientes vectores mínimo y máximo, min (-1, -1, -1) y max (1, 1, 1), el cuadro de límite se define de la siguiente manera.


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
| Encabezado  | D3DX10math.h |
| Biblioteca | D3DX10.lib  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
