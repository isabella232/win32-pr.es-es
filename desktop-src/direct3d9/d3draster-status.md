---
description: Describe el estado del trama.
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
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888660"
---
# <a name="d3draster_status-structure"></a>D3DRASTER \_ STATUS (estructura)

Describe el estado del trama.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**InVBlank**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** si el trama está en el punto en blanco vertical. **FALSE** si el trama no está en el punto en blanco vertical.

</dd> <dt>

**ScanLine**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Si InVBlank es **FALSE,** este valor es un entero que corresponde aproximadamente a la línea de examen actual dibujada por el trama. Las líneas de examen se numeran de la misma manera que las coordenadas de superficie de Direct3D: 0 es la parte superior de la superficie principal, extendiendo hasta el valor (alto de la superficie - 1) en la parte inferior de la pantalla.

Si InVBlank es **TRUE,** este valor se establece en cero y se puede omitir.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
