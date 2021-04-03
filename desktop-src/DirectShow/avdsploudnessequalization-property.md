---
description: Habilita o deshabilita la ecualización de sonoridad en un descodificador de audio o en un procesador de señal digital (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propiedad AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997993"
---
# <a name="avdsploudnessequalization-property"></a>Propiedad AVDSPLoudnessEqualization

Habilita o deshabilita la ecualización de sonoridad en un descodificador de audio o en un procesador de señal digital (DSP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .

## <a name="remarks"></a>Observaciones

La ecualización de sonoridad es un proceso de DSP que mantiene un nivel de volumen coherente cuando cambia la secuencia de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




