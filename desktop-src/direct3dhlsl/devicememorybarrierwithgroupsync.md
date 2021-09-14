---
title: Función DeviceMemoryBarmoreWithGroupSync
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a la memoria del dispositivo y todos los subprocesos del grupo hayan alcanzado esta llamada.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Función HLSL de DeviceMemoryBarhlWithGroupSync
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264239"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Función DeviceMemoryBarmoreWithGroupSync

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

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




