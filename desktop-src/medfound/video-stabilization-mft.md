---
description: El MFT de estabilización de vídeo es Microsoft Media Foundation transformación de imágenes (MFT) que realiza la estabilización de imágenes en una secuencia de vídeo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Video Stabilization MFT (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc81f71e856b2ae1eceee41c29dd699d17663c02c0f6982d6dc6c790395df2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057582"
---
# <a name="video-stabilization-mft"></a>Video Stabilization MFT

El MFT de estabilización de vídeo es Microsoft Media Foundation transformación de imágenes (MFT) que realiza la estabilización de imágenes en una secuencia de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CMSVideoDSPMFT

## <a name="interfaces"></a>Interfaces

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Formatos de entrada

Las combinaciones de tipo de medio de entrada y subtipo aceptadas por el MFT de estabilización de vídeo para vídeo sin comprimir son:

-   **VÍDEO DE TIPO \_ MULTIMEDIA**
-   **MEDIASUBTYPE \_ NV12**
-   **MEDIASUBTYPE \_ YUY2**

## <a name="output-formats"></a>Formatos de salida

Las combinaciones de tipo de medio de salida y subtipo aceptadas por el MFT de estabilización de vídeo son:

-   **VÍDEO DE TIPO \_ MULTIMEDIA**
-   **MEDIASUBTYPE \_ NV12**

El tipo de medio de entrada debe establecerse antes que el tipo de medio de salida. En la mayoría de las situaciones, la compatibilidad con formato limitado no es un problema porque la canalización inserta automáticamente las conversiones de color necesarias.

El componente MFT de estabilización de vídeo es capaz de cambiar el formato dinámico cuando cambia la entrada. Cuando cambie el tamaño de la imagen de entrada o el subtipo, desencadenará un cambio de formato dinámico en el flujo de salida.

El MFT de estabilización de vídeo realizará la conversión de color en los casos siguientes:

-   Cuando el formato de entrada **es MEDIASUBTYPE \_ YUY2**.
-   Cuando se usa el modo de compatibilidad de Microsoft DirectX 9.0.

### <a name="attributes"></a>Atributos

El MFT de estabilización de vídeo admite los siguientes atributos a través de la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

-   El atributo [MF \_ VIDEODSP \_ MODE](mf-videodsp-mode.md) coloca el MFT de estabilización de vídeo en modo de estabilización o de paso a través. La aplicación debe llamar a [**MFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MF \_ VIDEODSP \_ TYPE** con un entero correspondiente a uno de los siguientes valores válidos: **MFVideoDSPMode \_ Stabilization** = 4, **MFVideoDSPMode \_ Passthrough** = 1. EL \_ MODO MF VIDEODSP \_ se puede cambiar en cualquier momento durante la reproducción. Esto provoca un cambio de modo dinámico. La salida cambiará a estabilizado o pasará después de 16 o 2 fotogramas (según el modo de latencia) después de cambiar el atributo.
-   El atributo [MF \_ LOW \_ LATENCY coloca](mf-low-latency.md) el MFT de estabilización de vídeo en modo de baja latencia o de alta calidad. La aplicación debe llamar a [**MFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MF LOW \_ \_ LATENCY** con un entero correspondiente a uno de los siguientes valores válidos: Latencia baja = 1 alta calidad = 0
-   La canalización usa el atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) para especificar las marcas de enlace D3D11 con las que crear los ejemplos de salida. Cualquier combinación de valores de la [**enumeración \_ BIND \_ FLAG D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) es válida.
-   La canalización usa el atributo **MF SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ \_ COUNT** para especificar el número mínimo de muestras que este componente debe admitir en la salida.
-   El atributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) se establece en todas las muestras producidas por la estabilización para indicar el modo [EFECTIVO DE MF \_ VIDEODSP \_ ](mf-videodsp-mode.md) aplicado a esa muestra (independientemente de si la muestra se ha estabilizado o no). En determinadas condiciones, es posible que las muestras no se estabilimenten (debido a una carga elevada del sistema o a solicitudes del usuario). Este atributo tiene los mismos valores que el atributo MF \_ VIDEODSP \_ MODE (**MFVideoDSPMode \_ Stabilization** y **MFVideoDSPMode \_ Passthrough**). Para obtener el valor de este atributo, las aplicaciones deben llamar [**a MFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en GUID **MFSampleExtension \_ VideoDSPMode**.

## <a name="remarks"></a>Comentarios

Una instancia del DSP de estabilización de vídeo se puede crear de una de las maneras siguientes:

-   Mediante una llamada [**a MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). El DSP de estabilización de vídeo se registra en la **categoría \_ MFT CATEGORY \_ VIDEO \_ EFFECT.**
-   Al llamar a la función COM **CoCreateInstance,** se le pasa el **CLSID \_ CLSID CMSVideoDSPMFT**. Para usar este método, debe incluir wmcodecdsp.h y un vínculo en wmcodecdspuuid.lib.

Además, el DSP de estabilización de vídeo admite la creación de instancias mediante Windows Runtime como una extensión Windows multimedia. Se define en el [**Windows. Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)y su nombre completo es "Windows. Media.VideoEffects.VideoStabilization".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Camerauicontrol.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
