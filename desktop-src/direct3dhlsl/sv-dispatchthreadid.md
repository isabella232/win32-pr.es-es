---
title: SV_DispatchThreadID
description: Índices para los que se está ejecutando un sombreador de cálculo en el subproceso y el grupo de subprocesos combinados.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567863"
---
# <a name="sv_dispatchthreadid"></a>VP \_ DispatchThreadID

Índices para los que se está ejecutando un sombreador de cálculo en el subproceso y el grupo de subprocesos combinados. VP \_ DispatchThreadID es la suma de SV \_ GroupID \* numthreads y GroupThreadID. Varía en el intervalo especificado en [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) y [numthreads](sm5-attributes-numthreads.md). Por ejemplo, si se llama a dispatch (2, 2, 2) en un sombreador de cálculo con numthreads (3, 3, 3) SV \_ DispatchThreadID tendrá un intervalo de 0.. 5 para cada dimensión.

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Observaciones

Este valor del sistema es opcional.

En la ilustración siguiente se muestra la relación entre los parámetros que se pasan a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md), VP \_ DispatchThreadID,[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md)).

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

Esta función se admite en los siguientes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 