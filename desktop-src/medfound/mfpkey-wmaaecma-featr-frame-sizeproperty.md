---
description: Especifica el tamaño del fotograma de audio usado por el DSP de captura de voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Propiedad MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696697"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>\_Propiedad de \_ tamaño de \_ marco \_ del MFPKEY de WMAAECMA

Especifica el tamaño del fotograma de audio usado por el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El algoritmo de cancelación del eco acústico (AEC) procesa las muestras de audio PCM en un fotograma cada vez. El valor de esta propiedad es el tamaño del fotograma de audio, en ejemplos. Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

El DSP de captura de voz admite los siguientes tamaños de fotogramas:

-   80
-   128
-   160
-   240
-   256
-   320

Si el valor de esta propiedad es cero, el DSP selecciona el tamaño del marco según el modo del sistema y el formato de salida.

Sin embargo, para obtener el mejor rendimiento, se recomienda que las aplicaciones usen el valor predeterminado. Si el modo de procesamiento es solo una matriz de micrófono, el valor predeterminado es 320 ejemplos. En todos los demás modos de procesamiento, el valor predeterminado es 160 ejemplos. Para obtener más información acerca de los modos de procesamiento del DSP de captura de voz, consulte [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md).

Después de la primera llamada a [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), puede leer esta propiedad para obtener el tamaño real de los fotogramas en uso, aunque el [**modo de \_ \_ característica \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) sea false.

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

 

 
