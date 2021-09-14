---
description: Porcentaje de tiempo de procesamiento de datos en la canalización.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063746"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>D3DDEVINFO \_ D3D9PIPELINETIMINGS (estructura)

Porcentaje de tiempo de procesamiento de datos en la canalización.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo dedicado a ejecutar sombreadores de vértices.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo dedicado a ejecutar sombreadores de píxeles.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo dedicado a realizar otro procesamiento.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que no procesa nada.

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

 

 
