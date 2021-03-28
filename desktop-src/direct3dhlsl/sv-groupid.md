---
title: SV_GroupID
description: Índices para los que se está ejecutando un sombreador de cálculo en el grupo de subprocesos.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149347"
---
# <a name="sv_groupid"></a>ID. de \_ la SV

Índices para los que se está ejecutando un sombreador de cálculo en el grupo de subprocesos. Los índices están en todo el grupo y no en un subproceso individual. Los valores posibles varían en el intervalo pasado como parámetros a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Por ejemplo, llamar a dispatch (2, 1, 1) da como resultado valores posibles de 0, 0, 0 y 1, 0, 0.

Define el desplazamiento de grupo dentro de una llamada de [**envío**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , por dimensión de la llamada de envío.

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Observaciones

Este valor del sistema es opcional.

En la ilustración siguiente se muestra la relación entre los parámetros que se pasan a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md),[VP \_ DispatchThreadID](sv-dispatchthreadid.md),[VP \_ GroupThreadID](sv-groupthreadid.md), VP \_ GroupID).

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

 

 