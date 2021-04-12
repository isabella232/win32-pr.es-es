---
title: SV_GroupThreadID
description: Índices para los que un subproceso individual dentro de un grupo de subprocesos se está ejecutando en un sombreador de cálculo.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359351"
---
# <a name="sv_groupthreadid"></a>VP \_ GroupThreadID

Índices para los que un subproceso individual dentro de un grupo de subprocesos se está ejecutando en un sombreador de cálculo. SV \_ GroupThreadID varía en el intervalo especificado para el sombreador de cálculo en el atributo [numthreads](sm5-attributes-numthreads.md) . Por ejemplo, si se especifica numthreads (3, 2, 1), los valores posibles para el \_ valor de entrada VP GroupThreadID tienen este intervalo de valores (0-2, 0-1, 0).

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Observaciones

Este valor del sistema es opcional y siempre se encuentra dentro de los límites de los valores pasados al atributo [numthreads](sm5-attributes-numthreads.md) .

En la ilustración siguiente se muestra la relación entre los parámetros que se pasan a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md),[VP \_ DispatchThreadID](sv-dispatchthreadid.md), VP \_ GroupThreadID,[VP \_ GroupID](sv-groupid.md)).

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

 

 