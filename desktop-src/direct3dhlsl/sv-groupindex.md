---
title: SV_GroupIndex
description: '\ 0034; aplanad \ 0034; Índice de un subproceso del sombreador de cálculo dentro de un grupo de subprocesos, que convierte el GroupThreadID VP multidimensional \_ en un valor 1D. SV \_ GroupIndex varía de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; dimensional.'
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
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792285"
---
# <a name="sv_groupindex"></a>VP \_ GroupIndex

Índice "plano" de un subproceso del sombreador de cálculo dentro de un grupo de subprocesos, que convierte el valor de la VP multidimensional \_ GroupThreadID en un valor 1D. SV \_ GroupIndex varía de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Tipo



| Tipo |
|------|
| uint |



 

## <a name="remarks"></a>Observaciones


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



donde dimx y dimy son las dimensiones especificadas en el atributo [numthreads](sm5-attributes-numthreads.md) para el punto de entrada.

Este valor del sistema es opcional. Sin embargo, su uso garantiza que un subproceso solo escribe en su región de memoria asignada en la variable groupshared.

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso (VP \_ GroupIndex,[VP \_ DispatchThreadID](sv-dispatchthreadid.md),[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md))

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 