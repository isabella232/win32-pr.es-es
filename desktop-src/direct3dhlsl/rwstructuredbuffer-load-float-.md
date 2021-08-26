---
title: Función RWStructuredBuffer::Load(int)
description: Lee los datos del búfer. | Función RWStructuredBuffer::Load(int)
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cc8fbd0cfa18f2ac6c5d7109e8690d829bbde2175e8808865e68e29e63c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067765"
---
# <a name="rwstructuredbufferloadint-function"></a>Función RWStructuredBuffer::Load(int)

Lee los datos del búfer.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int**

Ubicación del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración del [**objeto RWStructuredBuffer.**](sm5-object-rwstructuredbuffer.md)

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de carga](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




