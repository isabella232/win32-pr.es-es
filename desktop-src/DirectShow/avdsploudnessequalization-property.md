---
description: Habilita o deshabilita la igualdad de sonoridad en un descodificador de audio o un procesador de señales digitales (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propiedad AVDSPLoudnessEqualization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61696b51996d6fe57cf15372d511704e2dad482f0a5e99eb165795f56256656a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052835"
---
# <a name="avdsploudnessequalization-property"></a>Propiedad AVDSPLoudnessEqualization

Habilita o deshabilita la igualdad de sonoridad en un descodificador de audio o un procesador de señales digitales (DSP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDSPLoudnessEqualization.**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)

## <a name="remarks"></a>Comentarios

La igualdad de sonoridad es un proceso de DSP que mantiene un nivel de volumen coherente cuando cambia la secuencia de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




