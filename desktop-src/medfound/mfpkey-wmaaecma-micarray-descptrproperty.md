---
description: Especifica la geometría de la matriz de micrófonos para el DSP de captura de voz.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263204"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR

Especifica la geometría de la matriz de micrófonos para el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BLOB

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es una [**estructura GEOMETRY de KSAUDIO \_ MIC \_ ARRAY. \_**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) Esta estructura se define en el archivo de encabezado KsMedia.h. Para obtener la geometría de la matriz de micrófonos, consulte en el dispositivo de audio la propiedad GEOMETRY KSPROPERTY AUDIO MIC ARRAY llamando al método \_ \_ \_ \_ **IKsControl::KSProperty** en el dispositivo. Para obtener más información sobre las matrices de micrófonos, descargue las white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Establezca esta propiedad si usa el DSP en modo de filtro y el procesamiento de la matriz de micrófonos está habilitado. Si usa el DSP en modo de origen, el DSP consulta automáticamente al dispositivo la información de geometría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
