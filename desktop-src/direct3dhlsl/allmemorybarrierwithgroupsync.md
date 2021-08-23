---
title: Función AllMemoryBargroupWithGroupSync
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria y todos los subprocesos del grupo hayan alcanzado esta llamada.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Función HLSL de AllMemoryBarhlWithGroupSync
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d3c146ff04597b7eca13dd5cbef93dc1c79f81709353bf5b4fa1a993a8da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626695"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>Función AllMemoryBargroupWithGroupSync

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria y todos los subprocesos del grupo hayan alcanzado esta llamada.

## <a name="syntax"></a>Sintaxis

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una barrera de memoria garantiza que se han completado las operaciones de memoria pendientes. Los subprocesos se sincronizan en las barreras groupsync. Esto puede detener un subproceso o subprocesos si las operaciones de memoria están en curso.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




