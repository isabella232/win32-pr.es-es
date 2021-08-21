---
description: Especifica el tamaño del fotograma de audio utilizado por el DSP de captura de voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973294"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE

Especifica el tamaño del fotograma de audio utilizado por el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El algoritmo de cancelación de eco acústico (AEC) procesa muestras de audio PCM fotograma a fotograma. El valor de esta propiedad es el tamaño del marco de audio, en ejemplos. Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP de captura de voz admite los siguientes tamaños de fotograma:

-   80
-   128
-   160
-   240
-   256
-   320

Si el valor de esta propiedad es cero, el DSP selecciona el tamaño del marco en función del modo del sistema y el formato de salida.

Sin embargo, para obtener el mejor rendimiento, se recomienda que las aplicaciones usen el valor predeterminado. Si el modo de procesamiento es solo la matriz de micrófonos, el valor predeterminado es 320 muestras. Para todos los demás modos de procesamiento, el valor predeterminado es 160 muestras. Para obtener más información sobre los modos de procesamiento del DSP de captura de voz, vea [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE](mfpkey-wmaaecma-system-modeproperty.md).

Después de la primera llamada a [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessOutput,**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)puede leer esta propiedad para obtener el tamaño de fotograma real en uso, incluso cuando [**MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE**](mfpkey-wmaaecma-feature-modeproperty.md) es false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
