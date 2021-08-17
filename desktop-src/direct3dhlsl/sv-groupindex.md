---
title: SV_GroupIndex
description: '\ 0034;flattened \ 0034; índice de un subproceso de sombreador de proceso dentro de un grupo de subprocesos, que convierte el valor multidimensional de SV \_ GroupThreadID en un valor 1D. SV \_ GroupIndex varía de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; 1.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508255"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

Índice "aplanado" de un subproceso de sombreador de proceso dentro de un grupo de subprocesos, que convierte sv groupThreadID multidimensional \_ en un valor 1D. SV \_ GroupIndex varía de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Tipo



| Tipo |
|------|
| uint |



 

## <a name="remarks"></a>Comentarios


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



donde dimx y dimy son las dimensiones especificadas en el [atributo numthreads](sm5-attributes-numthreads.md) para el punto de entrada.

Este valor del sistema es opcional. Sin embargo, su uso garantiza que un subproceso solo escribe en su región de memoria asignada en la variable groupshared.

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos (SV \_ GroupIndex,[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID).](sv-groupid.md)

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 