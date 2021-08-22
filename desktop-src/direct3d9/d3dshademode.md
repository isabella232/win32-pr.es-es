---
description: Define constantes que describen los modos de sombreado admitidos.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumeración D3DSHADEMODE (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6a8c937000912eb203986bed4889785b9484afec7682418aed43fcc58c438e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241565"
---
# <a name="d3dshademode-enumeration"></a>D3DSHADEMODE (enumeración)

Define constantes que describen los modos de sombreado admitidos.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ FLAT**
</dt> <dd>

Modo de sombreado plano. El color y el componente especular del primer vértice del triángulo se usan para determinar el color y el componente especular de la cara. Estos colores permanecen constantes en el triángulo; es decir, no se interpolan. El alfa especular se interpola. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Modo de sombreado de Gouraud. Los componentes de color y especular de la cara se determinan mediante una interpolación lineal entre los tres vértices del triángulo.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PONG**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El primer vértice de un triángulo para el modo de sombreado plano se define de la siguiente manera.

-   Para una lista de triángulos, el primer vértice del triángulo i es i \* 3.
-   Para una franja de triángulo, el primer vértice del triángulo i es el vértice i.
-   Para un ventilador de triángulo, el primer vértice del triángulo i es el vértice i + 1.

Los miembros de este tipo enumerado definen los vales para el estado de representación \_ SHADEMODE de D3DRS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
