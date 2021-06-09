---
title: SV_GroupThreadID
description: Índices para los que se ejecuta un subproceso individual dentro de un grupo de subprocesos en el que se ejecuta un sombreador de proceso.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827034"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Índices para los que se ejecuta un subproceso individual dentro de un grupo de subprocesos en el que se ejecuta un sombreador de proceso. SV \_ GroupThreadID varía según el intervalo especificado para el sombreador de proceso en el [atributo numthreads.](sm5-attributes-numthreads.md) Por ejemplo, si se especificó numthreads(3,2,1) los valores posibles para el valor de entrada groupThreadID sv tienen este intervalo de valores \_ (0-2,0-1,0).

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Comentarios

Este valor del sistema es opcional y siempre está dentro de los límites de los valores pasados al [atributo numthreads.](sm5-attributes-numthreads.md)

En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
