---
description: Define constantes que describen el modo de relleno.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Enumeración D3DFILLMODE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e92d91c13718462487eb3dac07ba1d5fc61a2d428bf610dd9575b080d375676d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857455"
---
# <a name="d3dfillmode-enumeration"></a>D3DFILLMODE (enumeración)

Define constantes que describen el modo de relleno.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**PUNTO D3DFILL \_**
</dt> <dd>

Puntos de relleno.

</dd> <dt>

<span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ WIREFRAME**
</dt> <dd>

Rellene los wireframes.

</dd> <dt>

<span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ SOLID**
</dt> <dd>

Rellene los sólidos.

</dd> <dt>

<span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El estado de representación FILLMODE de D3DRS usa los valores \_ de este tipo enumerado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
