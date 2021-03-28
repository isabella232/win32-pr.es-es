---
title: AllMemoryBarrierWithGroupSync función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria y todos los subprocesos del grupo hayan alcanzado esta llamada.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- AllMemoryBarrierWithGroupSync de función HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076902"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>AllMemoryBarrierWithGroupSync función)

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria y todos los subprocesos del grupo hayan alcanzado esta llamada.

## <a name="syntax"></a>Sintaxis

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una barrera de memoria garantiza que se han completado las operaciones de memoria pendientes. Los subprocesos se sincronizan a barreras GroupSync. Esto puede bloquear un subproceso o subprocesos si hay operaciones de memoria en curso.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




