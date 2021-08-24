---
description: Describe el estado de trama.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fc8a1e2995a9353a02df120b109eb32ad0914821e5690440c7228fbc8e7b6c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676405"
---
# <a name="d3draster_status-structure"></a>D3DRASTER \_ STATUS (estructura)

Describe el estado de trama.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**InVBlank**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** si el trama está en el período en blanco vertical. **FALSE** si el trama no está en el período en blanco vertical.

</dd> <dt>

**ScanLine**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Si InVBlank es **FALSE,** este valor es un entero que corresponde aproximadamente a la línea de examen actual dibujada por el trama. Las líneas de examen se numeran de la misma manera que las coordenadas de superficie de Direct3D: 0 es la parte superior de la superficie principal, que se extiende al valor (alto de la superficie - 1) en la parte inferior de la pantalla.

Si InVBlank es **TRUE,** este valor se establece en cero y se puede omitir.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
