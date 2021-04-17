---
description: Especifica la geometría de la matriz de micrófono para el DSP de captura de voz.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Propiedad MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696692"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR

Especifica la geometría de la matriz de micrófono para el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

BLOB de VT \_

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es una estructura de geometría de la [**\_ \_ matriz \_ KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Esta estructura se define en el archivo de encabezado KsMedia. h. Para obtener la geometría de la matriz de micrófono, consulte el dispositivo de audio para la \_ propiedad Geometry de la matriz KSPROPERTY audio \_ MIC llamando \_ \_ al método **IKsControl:: KSPROPERTY** en el dispositivo. Para obtener más información acerca de las matrices de micrófono, descargue las notas del producto [Cómo crear y usar matrices de micrófonos para Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Establezca esta propiedad si usa el DSP en modo de filtro y el procesamiento de matriz de micrófono está habilitado. Si usa el DSP en modo de origen, el DSP consulta automáticamente la información de geometría en el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
