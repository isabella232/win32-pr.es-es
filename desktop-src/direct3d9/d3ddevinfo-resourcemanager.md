---
description: Estadísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_RESOURCEMANAGER estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129984"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>Estructura RESOURCEMANAGER de D3DDEVINFO \_

Estadísticas de uso de recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a>Miembros

<dl> <dt>

**stats**
</dt> <dd>

Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Matriz de elementos de estadísticas de recursos. Vea [**D3DRESOURCESTATS.**](d3dresourcestats.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DRTYPECOUNT hace referencia al número de enumeraciones en [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
