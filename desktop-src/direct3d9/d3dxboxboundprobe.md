---
description: Determina si un rayo forma una intersección con el volumen del rectángulo de selección de un cuadro.
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
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157200"
---
# <a name="d3dxboxboundprobe-function"></a>D3DXBoxBoundProbe función)

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina inferior izquierda del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pMax* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina superior derecha del cuadro de límite. Vea la sección Comentarios.

</dd> <dt>

*pRayPosition* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la coordenada de origen del rayo.

</dd> <dt>

*pRayDirection* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo. Este vector no debe ser (0, 0, 0), pero no es necesario normalizarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

**D3DXboxBoundProbe** determina si el rayo forma una intersección con el volumen del rectángulo de selección del cuadro, no solo la superficie del cuadro.

Los valores que se pasan a **D3DXboxBoundProbe** son xmin, Xmax, YMIN, YMax, Zmin y Zmax. Por lo tanto, el siguiente código define las esquinas del cuadro de límite.


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
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
