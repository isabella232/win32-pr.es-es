---
description: Contiene la marca de tiempo del controlador del dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474067"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>Atributo MFSampleExtension \_ DeviceTimestamp

Contiene la marca de tiempo del controlador del dispositivo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Este atributo se establece en ejemplos de medios creados por un origen multimedia para un dispositivo de captura. El valor de este atributo está en el dominio [**MFTIME,**](mftime.md) comparte una época con el tiempo del contador de rendimiento de consultas (QPC) y siempre se expresa en unidades de 100ns. Este atributo está disponible para las MTO insertadas en la canalización de captura.

Para obtener la marca de tiempo con respecto al inicio del streaming, llame al [**métodoSAMPLESample::GetSampleTime.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo en Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> </dl>

 

 




