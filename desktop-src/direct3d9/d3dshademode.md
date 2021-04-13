---
description: Define constantes que describen los modos de sombreado admitidos.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumeración D3DSHADEMODE (D3d9types. h)
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
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362507"
---
# <a name="d3dshademode-enumeration"></a>Enumeración D3DSHADEMODE

Define constantes que describen los modos de sombreado admitidos.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ plano**
</dt> <dd>

Modo de sombreado plano. El color y el componente especular del primer vértice del triángulo se usan para determinar el color y el componente especular de la superficie. Estos colores permanecen constantes a lo largo del triángulo; es decir, no se interpolan. El alfa especular está interpolado. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Modo de sombreado Gouraud. Los componentes de color y especular de la superficie se determinan mediante una interpolación lineal entre los tres vértices del triángulo.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**
</dt> <dd>

No se admite.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El primer vértice de un triángulo para el modo de sombreado plano se define de la manera siguiente.

-   En el caso de una lista de triángulos, el primer vértice del triángulo i es i \* 3.
-   En el caso de una franja de triángulo, el primer vértice del triángulo i es el vértice i.
-   En el caso de un ventilador de triángulo, el primer vértice del triángulo i es el vértice i + 1.

Los miembros de este tipo enumerado definen el valores para el estado de representación de D3DRS \_ SHADEMODE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
