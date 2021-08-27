---
title: Función RWBuffer::Load(int)
description: Lee los datos del búfer. | Función RWBuffer::Load(int)
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: d3e3f9c9714cb4cc7f0f29bfa801e767b468d526836a7bd09f0f9823d9ff8868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118305"
---
# <a name="rwbufferloadint-function"></a>Función RWBuffer::Load(int)

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

El tipo de valor devuelto coincide con el tipo de la declaración del [**objeto RWBuffer.**](sm5-object-rwbuffer.md)

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de carga](rwbuffer-load.md)
</dt> </dl>

 

 




