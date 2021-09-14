---
description: Porcentaje de tiempo de procesamiento de datos del sombreador.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: D3DDEVINFO_D3D9STAGETIMINGS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063744"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>D3DDEVINFO \_ D3D9STAGETIMINGS (estructura)

Porcentaje de tiempo de procesamiento de datos del sombreador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**MemoryProcessingPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo dedicado al sombreador en accesos a memoria.

</dd> <dt>

**ComputationProcessingPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de procesamiento de tiempo (mover datos en registros o realizar operaciones matemáticas).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener el mejor rendimiento, se recomienda una carga equilibrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
