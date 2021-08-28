---
description: Define el tipo base de una superficie de revisión de orden alto.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumeración D3DBASISTYPE (D3D9Types.h)
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
ms.openlocfilehash: 9129184f778394f5095218b6808aa5940a7670fb3eb30c77c2edeafecf847228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989275"
---
# <a name="d3dbasistype-enumeration"></a>D3DBASISTYPE (enumeración)

Define el tipo base de una superficie de revisión de orden alto.

## <a name="syntax"></a>Syntax


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

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ BEZIER**
</dt> <dd>

Los vértices de entrada se tratan como una serie de revisiones de Bézier. El número de vértices especificados debe ser divisible entre 4. Las partes de la malla más allá de este criterio no se representarán. Se supone una continuidad completa entre las suba patches en el interior de la superficie que representa cada llamada. Solo se garantiza que los vértices de las esquinas de cada sub revisión se encuentran en la superficie resultante.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**
</dt> <dd>

Los vértices de entrada se tratan como puntos de control de una superficie B-spline. El número de aperturas representadas es dos menos que el número de aperturas en esa dirección. En general, la superficie generada no contiene los vértices de control especificados.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

Una base de interpolación define la superficie para que pase por todos los vértices de entrada especificados. En DirectX 8, era D3DBASIS \_ INTERPOLATE.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de **D3DBASISTYPE** especifican la formulación que se usará para evaluar la primitiva de superficie de revisión de orden superior durante la teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**INFORMACIÓN DE D3DRECTPATCH \_**](d3drectpatch-info.md)
</dt> <dt>

[**INFORMACIÓN DE D3DTRIPATCH \_**](d3dtripatch-info.md)
</dt> </dl>

 

 




