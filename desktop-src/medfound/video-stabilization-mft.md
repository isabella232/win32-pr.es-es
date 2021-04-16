---
description: La MFT de estabilización de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la estabilización de la imagen en una secuencia de vídeo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Video Stabilization MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671607"
---
# <a name="video-stabilization-mft"></a>Video Stabilization MFT

La MFT de estabilización de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la estabilización de la imagen en una secuencia de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CMSVideoDSPMFT

## <a name="interfaces"></a>Interfaces

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Formatos de entrada

El tipo de medio de entrada y las combinaciones de subtipos aceptadas por el MFT de estabilización de vídeo para el vídeo sin comprimir son:

-   **vídeo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**
-   **MEDIASUBTYPE \_ YUY2**

## <a name="output-formats"></a>Formatos de salida

El tipo de medio de salida y las combinaciones de subtipos aceptadas por la MFT de estabilización de vídeo son:

-   **vídeo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**

El tipo de medio de entrada debe establecerse antes que el tipo de medio de salida. En la mayoría de los casos, la compatibilidad con formato limitado no es un problema porque la canalización inserta automáticamente las conversiones de color necesarias.

El componente MFT de estabilización de vídeo es capaz de cambiar el formato dinámico cuando cambia la entrada. Cuando cambia el tamaño de la imagen de entrada o cambia el subtipo, se desencadena un cambio de formato dinámico en el flujo de salida.

La MFT de estabilización de vídeo realizará la conversión de colores en los casos siguientes:

-   Cuando el formato de entrada es **MEDIASUBTYPE \_ YUY2**.
-   Cuando se utiliza el modo de compatibilidad de Microsoft DirectX 9,0.

### <a name="attributes"></a>Atributos

Los siguientes atributos son compatibles con la MFT de estabilización de vídeo a través de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

-   El atributo [MF \_ VIDEODSP \_ mode](mf-videodsp-mode.md) coloca el MFT de estabilización de vídeo en el modo de estabilización o en el modo de paso a través. La aplicación debe llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el **\_ \_ tipo VIDEODSP** de GUID MF con un entero correspondiente a uno de los siguientes valores válidos: **\_ estabilización MFVideoDSPMode** = 4, **MFVideoDSPMode \_ passthrough** = 1. \_ \_ El modo MF VIDEODSP se puede cambiar en cualquier momento durante la reproducción. Esto provoca un cambio de modo dinámico. La salida cambiará a estabilizada o a paso a través después de 16 o 2 fotogramas (dependiendo del modo de latencia) una vez cambiado el atributo.
-   El atributo [MF \_ Low \_ latencia](mf-low-latency.md) coloca la MFT de estabilización de vídeo en el modo de latencia baja o en el modo de alta calidad. La aplicación debe llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MF \_ Low \_ latencia** con un entero correspondiente a uno de los siguientes valores válidos: latencia baja = 1 alta calidad = 0
-   La canalización usa el atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) para especificar las marcas de enlace D3D11 con las que se van a crear los ejemplos de salida. Cualquier combinación de valores de la enumeración de [**\_ \_ marcadores de enlace D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) es válida.
-   La canalización utiliza el atributo **MF de \_ ejemplo de salida mínima de la \_ \_ \_ \_ cuenta** para especificar el número mínimo de muestras que este componente debe admitir en la salida.
-   El atributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) se establece en cada muestra generada por la estabilización para indicar el [ \_ \_ modo de MF VIDEODSP](mf-videodsp-mode.md) vigente que se aplica a ese ejemplo (si el ejemplo se ha estabilizado o no). En determinadas condiciones, es posible que los ejemplos no estén estabilizados (debido a una carga elevada del sistema o a las solicitudes del usuario). Este atributo tiene los mismos valores que el \_ atributo de modo MF VIDEODSP \_ (**\_ estabilización MFVideoDSPMode** y **MFVideoDSPMode \_ passthrough**). Para obtener el valor de este atributo, las aplicaciones deben llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MFSampleExtension \_ VideoDSPMode**.

## <a name="remarks"></a>Observaciones

Una instancia del DSP de estabilización de vídeo se puede crear de una de las siguientes maneras:

-   Llamando a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). El DSP de estabilización de vídeo se registra en la categoría de **\_ efecto de \_ vídeo \_ efecto de la categoría MFT** .
-   Llamando a la función de COM **CoCreateInstance** pasándole el CLSID CLSID **\_ CMSVideoDSPMFT**. Para usar este método, debe incluir wmcodecdsp. h y vincular con wmcodecdspuuid. lib.

Además, el DSP de estabilización de vídeo admite la creación de instancias mediante Windows Runtime como una extensión de Windows Media. Se define en los [**efectos Windows. Media.**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)video, y su nombre completo es "Windows. Media. videoeffects. videoestabilization".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
