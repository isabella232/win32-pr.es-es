---
title: Función GroupMemoryBarmore
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- Función HlSL de GroupMemoryBarhl
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9889be841df54f6ae18b7ac52d7117f780af37662c5a1d4f6c29af858350345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743865"
---
# <a name="groupmemorybarrier-function"></a>Función GroupMemoryBarmore

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.

## <a name="syntax"></a>Sintaxis

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




