---
description: Informa del número de triángulos que el procesamiento de vértices de software del runtime ha procesado y recortado.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: D3DDEVINFO_D3DVERTEXSTATS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3baa6738e5d90d2353beb6c7d7bf0ab85770af4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174829"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>D3DDEVINFO \_ D3DVERTEXSTATS (estructura)

Informa del número de triángulos que el procesamiento de vértices de software del runtime ha procesado y recortado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de triángulos que no se recortan en este marco.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de triángulos nuevos generados por el recorte.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el tiempo de ejecución de depuración y el procesamiento de vértices de software para obtener el número de primitivas no recortadas y recortadas para una escena determinada. Las primitivas normalmente se recortarán en función de una banda de protección (si hay una). La banda de protección de recorte se establece con parámetros como GuardBandLeft en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
