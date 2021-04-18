---
description: Define las operaciones de Blend admitidas. Vea comentarios para obtener definiciones de términos.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumeración D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717670"
---
# <a name="d3dblendop-enumeration"></a>Enumeración D3DBLENDOP

Define las operaciones de Blend admitidas. Vea comentarios para obtener definiciones de términos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Agregar**
</dt> <dd>

El resultado es el destino agregado al origen. Resultado = origen + destino

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**Resta de D3DBLENDOP \_**
</dt> <dd>

El resultado es el destino que se resta de al origen. Resultado = origen-destino

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**
</dt> <dd>

El resultado es el origen que se resta del destino. Resultado = destino-origen

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ mín.**
</dt> <dd>

El resultado es el mínimo del origen y del destino. Resultado = MIN (origen, destino)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ máx.**
</dt> <dd>

El resultado es el máximo del origen y del destino. Resultado = MAX (origen, destino)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Origen, destino y resultado se definen como:



| Término        | Tipo   | Descripción                                                            |
|-------------|--------|------------------------------------------------------------------------|
| Source      | Entrada  | Color del píxel de origen antes de la operación.                        |
| Destination | Entrada  | Color del píxel en el búfer de destino antes de la operación.     |
| Resultado      | Output | Valor devuelto que es el color mezclado resultante de la operación. |



 

Este tipo enumerado define los valores utilizados por los siguientes Estados de representación:

-   D3DRS \_ BLENDOP
-   D3DRS \_ BLENDOPALPHA

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
