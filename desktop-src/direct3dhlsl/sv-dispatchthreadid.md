---
title: SV_DispatchThreadID
description: Índices para los que el subproceso combinado y el grupo de subprocesos se ejecutan en un sombreador de proceso.
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
ms.openlocfilehash: a5f7dbc7f4aa4b508d801736529628dbb25c29fb6c37f1db04f91874e85ee9a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023395"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Índices para los que el subproceso combinado y el grupo de subprocesos se ejecutan en un sombreador de proceso. SV \_ DispatchThreadID es la suma de SV \_ GroupID \* numthreads y GroupThreadID. Varía según el intervalo especificado en [**Dispatch y**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) [numthreads](sm5-attributes-numthreads.md). Por ejemplo, si se llama a Dispatch(2,2,2) en un sombreador de proceso con numthreads(3,3,3) SV DispatchThreadID tendrá un intervalo de \_ 0,.5 para cada dimensión.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Comentarios

Este valor del sistema es opcional.

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
