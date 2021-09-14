---
description: Habilita o deshabilita la igualdad de sonoridad en un descodificador de audio o un procesador de señales digitales (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propiedad AVDSPLoudnessEqualization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162077"
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

## <a name="remarks"></a>Observaciones

La igualdad de sonoridad es un proceso de DSP que mantiene un nivel de volumen coherente cuando cambia la secuencia de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




