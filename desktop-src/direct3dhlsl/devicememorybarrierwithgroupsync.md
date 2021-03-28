---
title: DeviceMemoryBarrierWithGroupSync función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a la memoria del dispositivo y todos los subprocesos del grupo hayan alcanzado esta llamada.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- DeviceMemoryBarrierWithGroupSync de función HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358204"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>DeviceMemoryBarrierWithGroupSync función)

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a la memoria del dispositivo y todos los subprocesos del grupo hayan alcanzado esta llamada.

## <a name="syntax"></a>Sintaxis

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
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

 

 




