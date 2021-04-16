---
description: Define operaciones de búfer de estarcido.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumeración D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678787"
---
# <a name="d3dstencilop-enumeration"></a>Enumeración D3DSTENCILOP

Define operaciones de búfer de estarcido.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ mantener**
</dt> <dd>

No actualice la entrada en el búfer de estarcido. Este es el valor predeterminado.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ cero**
</dt> <dd>

Establezca la entrada de búfer de estarcido en 0.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ reemplazar**
</dt> <dd>

Reemplace la entrada del búfer de la galería de símbolos por un valor de referencia.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**
</dt> <dd>

Incremente la entrada del búfer de la galería de símbolos y la fijación al valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**
</dt> <dd>

Disminuya la entrada del búfer de la galería de símbolos, de la abrazadera a cero.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**\_Invertir D3DSTENCILOP**
</dt> <dd>

Invierta los bits en la entrada de búfer de la galería de símbolos.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ incr**
</dt> <dd>

Incremente la entrada del búfer de la galería de símbolos, ajustándola a cero si el nuevo valor supera el valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ decr (**
</dt> <dd>

Disminuye la entrada del búfer de estarcido, ajustándola al valor máximo si el nuevo valor es menor que cero.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las entradas de búfer de estarcido son valores enteros comprendidos entre 0 y 2 ⁿ-1, donde n es la profundidad de bits del búfer de estarcido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




