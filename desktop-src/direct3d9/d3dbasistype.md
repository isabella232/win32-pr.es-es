---
description: Define el tipo base de una superficie de revisión de orden superior.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumeración D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157152"
---
# <a name="d3dbasistype-enumeration"></a>Enumeración D3DBASISTYPE

Define el tipo base de una superficie de revisión de orden superior.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bézier**
</dt> <dd>

Los vértices de entrada se tratan como una serie de revisiones de Bézier. El número de vértices especificado debe ser divisible por 4. No se representarán las partes de la malla que superen este criterio. Se supone una continuidad completa entre las subrevisiones en el interior de la superficie representada por cada llamada. Solo se garantiza que los vértices de las esquinas de cada subrevisión se encuentran en la superficie resultante.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**
</dt> <dd>

Los vértices de entrada se tratan como puntos de control de una superficie de spline B. El número de aberturas representadas es dos veces menor que el número de aberturas en esa dirección. En general, la superficie generada no contiene los vértices de control especificados.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

Una base de interpolación define la superficie para que la superficie pase por todos los vértices de entrada especificados. En DirectX 8, esto era D3DBASIS \_ Interpolate.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de **D3DBASISTYPE** especifican la formulación que se va a usar en la evaluación de la primitiva de la superficie de revisión de orden superior durante la teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**Información de D3DRECTPATCH \_**](d3drectpatch-info.md)
</dt> <dt>

[**Información de D3DTRIPATCH \_**](d3dtripatch-info.md)
</dt> </dl>

 

 




