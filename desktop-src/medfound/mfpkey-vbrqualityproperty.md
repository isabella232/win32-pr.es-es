---
description: Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Propiedad MFPKEY_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001624"
---
# <a name="mfpkey_vbrquality-property"></a>\_Propiedad VBRQUALITY de MFPKEY

Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

No todos los valores del intervalo tienen un significado único. Los valores que representan un paso en la calidad del nivel anterior son: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 y 100.

En el caso de los objetos de codificador de audio, los modos de calidad se proporcionan en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) de los tipos de salida que se recuperan mediante [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeración de los tipos de audio para los modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
