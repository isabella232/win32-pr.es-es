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
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360837"
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

## <a name="remarks"></a>Observaciones

Una barrera de memoria garantiza que se han completado las operaciones de memoria pendientes. Los subprocesos se sincronizan en las barreras groupsync. Esto puede detener un subproceso o subprocesos si las operaciones de memoria están en curso.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




