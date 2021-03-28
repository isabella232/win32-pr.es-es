---
title: GroupMemoryBarrier función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- GroupMemoryBarrier de función HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076470"
---
# <a name="groupmemorybarrier-function"></a>GroupMemoryBarrier función)

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.

## <a name="syntax"></a>Sintaxis

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

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

 

 




