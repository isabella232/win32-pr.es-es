---
description: Describe el estado de la trama.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS estructura (D3D9Types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707926"
---
# <a name="d3draster_status-structure"></a>Estructura de estado de D3DRASTER \_

Describe el estado de la trama.

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

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** si la trama está en el período en blanco vertical. **False** si la trama no está en el período en blanco vertical.

</dd> <dt>

**ScanLine**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Si InVBlank es **false**, este valor es un entero que se corresponde aproximadamente con la línea de recorrido actual dibujada por la trama. Las líneas de recorrido se numeran de la misma manera que las coordenadas de la superficie de Direct3D: 0 es la parte superior de la superficie principal, que se extiende hasta el valor (alto de la superficie-1) en la parte inferior de la pantalla.

Si InVBlank es **true**, este valor se establece en cero y se puede omitir.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
