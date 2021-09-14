---
title: Función GroupMemoryBarmoreWithGroupSync
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo y todos los subprocesos del grupo hayan alcanzado esta llamada.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Función HLSL de GroupMemoryBarhlWithGroupSync
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361561"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>Función GroupMemoryBarmoreWithGroupSync

Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo y todos los subprocesos del grupo hayan alcanzado esta llamada.

## <a name="syntax"></a>Sintaxis

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
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

 

 




