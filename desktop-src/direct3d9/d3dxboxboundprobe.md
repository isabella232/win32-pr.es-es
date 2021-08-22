---
description: Determina si un rayo forma una intersección con el volumen del rectángulo delimitador de un cuadro.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Función D3DXBoxBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676395"
---
# <a name="d3dxboxboundprobe-function"></a>Función D3DXBoxBoundProbe

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la esquina inferior izquierda del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la esquina superior derecha del cuadro de límite. Vea la sección Comentarios.

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

Devuelve **TRUE** si el rayo forma una intersección con el volumen del cuadro de límite del cuadro. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

**D3DXboxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo delimitador del cuadro, no solo con la superficie del cuadro.

Los valores pasados a **D3DXboxBoundProbe** son xmin, xmax, ymin, ymax, zmin y zmax. Por lo tanto, lo siguiente define las esquinas del cuadro de límite.


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



La profundidad del cuadro de límite en la dirección z es zmax - zmin, en la dirección y es ymax - ymin, y en la dirección x es xmax - xmin. Por ejemplo, con los siguientes vectores mínimo y máximo, min (-1, -1, -1) y max (1, 1, 1), el cuadro de límite se define de la siguiente manera.


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
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
