---
title: AllMemoryBarrier función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier de función HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419717"
---
# <a name="allmemorybarrier-function"></a>AllMemoryBarrier función)

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria.

## <a name="syntax"></a>Sintaxis

``` syntax
void AllMemoryBarrier(void);
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

 

 




