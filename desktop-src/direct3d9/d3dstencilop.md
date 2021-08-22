---
description: Define las operaciones de búfer de galería de símbolos.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumeración D3DSTENCILEVEL (D3D9Types.h)
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
ms.openlocfilehash: 166f670e6e34edd6a3b05584c54e63be274e54161faea242fa701e771a90a771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564945"
---
# <a name="d3dstencilop-enumeration"></a>D3DSTENCILEVEL (enumeración)

Define las operaciones de búfer de galería de símbolos.

## <a name="syntax"></a>Syntax


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

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCI \_ KEEP**
</dt> <dd>

No actualice la entrada en el búfer de galería de símbolos. Este es el valor predeterminado.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ ZERO**
</dt> <dd>

Establezca la entrada stencil-buffer en 0.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCISTONE \_ REPLACE**
</dt> <dd>

Reemplace la entrada stencil-buffer por un valor de referencia.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCISTONE \_ INCRSAT**
</dt> <dd>

Incremente la entrada stencil-buffer, fijando al valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**
</dt> <dd>

Decremento de la entrada stencil-buffer, fijando a cero.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCISTONE \_ INVERT**
</dt> <dd>

Invierta los bits de la entrada stencil-buffer.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCISTONE \_ INCR**
</dt> <dd>

Incremente la entrada stencil-buffer y ajuste a cero si el nuevo valor supera el valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ DECR**
</dt> <dd>

Decremento de la entrada stencil-buffer, ajustando al valor máximo si el nuevo valor es menor que cero.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCISTONE \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las entradas de búfer de galería de símbolos son valores enteros comprendidos entre 0 y 2ⁿ - 1, donde n es la profundidad de bits del búfer de galería de símbolos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




