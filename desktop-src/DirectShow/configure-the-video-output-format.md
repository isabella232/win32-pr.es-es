---
description: Configuración del formato de salida de vídeo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configuración del formato de salida de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe52ea72deb812fa1b3d4e131885640eb3279f1635622084b91857cadaf9bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871815"
---
# <a name="configure-the-video-output-format"></a>Configuración del formato de salida de vídeo

> [!Note]  
> La funcionalidad descrita en este tema está en desuso. Para configurar el formato de salida de un dispositivo de captura, una aplicación debe usar la estructura [**\_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) devuelta por [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el *parámetro pmt.*

 

Un dispositivo de captura puede admitir una variedad de formatos de salida. Por ejemplo, un dispositivo podría admitir RGB de 16 bits, RGB de 32 bits y YUYV. Dentro de cada uno de estos formatos, el dispositivo puede admitir una variedad de tamaños de fotograma.

En un dispositivo WDM, la [**interfaz IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) se usa para notificar qué formatos admite el dispositivo y para establecer el formato. (Para dispositivos VFW heredados, use el cuadro de diálogo FORMATO de vídeo VFW, como se describe en Mostrar cuadros de [diálogo de captura de VFW).](display-vfw-capture-dialog-boxes.md) La **interfaz IAMStreamConfig** se expone en el pin de captura del filtro de captura, el pin de vista previa o ambos. Use el [**método ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para obtener el puntero de interfaz:


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



El dispositivo tiene una lista de tipos de medios que admite. Para cada tipo de medio, el dispositivo también proporciona un conjunto de funcionalidades. Entre ellos se incluye la gama de tamaños de fotogramas disponibles para ese formato, la forma en que el dispositivo puede ampliar o reducir la imagen y el intervalo de velocidades de fotogramas.

Para obtener el número de tipos de medios, llame al [**método IAMStreamConfig::GetNumberOfCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) El método devuelve dos valores:

-   Número de tipos de medios.
-   Tamaño de la estructura que contiene la información de funcionalidades.

El valor de tamaño es necesario porque la [**interfaz IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) se usa para audio y vídeo (y se podría extender a otros tipos de medios). En el caso del vídeo, las funcionalidades se describen mediante la estructura [**\_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de configuración de VIDEO STREAM, mientras que el audio usa la estructura CAPS de [**configuración \_ \_ \_ de AUDIO STREAM.**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps)

Para enumerar los tipos de medios, llame al [**método IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) con un índice de base cero. El **método GetStreamCaps** devuelve un tipo de medio y la estructura de funcionalidad correspondiente:


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Observe cómo se asignan las estructuras para el [**método GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) El método asigna la estructura de tipo de medio, mientras que el autor de la llamada asigna la estructura de funcionalidades. Coerción de la estructura de funcionalidades a un puntero de matriz de bytes. Cuando haya terminado con el tipo de medio, elimine la estructura [**\_ AM MEDIA \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) junto con el bloque de formato del tipo de medio.

Puede configurar el dispositivo para que use un formato devuelto en el [**método GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) Simplemente llame [**a IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) con el tipo de medio:


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Si el pin no está conectado, intentará usar este formato cuando se conecte. Si el pin ya está conectado, intenta volver a conectarse con el nuevo formato. En cualquier caso, es posible que el filtro de nivel inferior rechace el formato.

También puede modificar el tipo de medio antes de pasarlo al [**método SetFormat.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) Aquí es donde entra en servicio la estructura [**\_ \_ \_ CAPS de configuración de VIDEO STREAM.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) Describe todas las formas válidas de cambiar el tipo de medio. Para usar esta información, debe comprender los detalles de ese tipo de medio determinado.

Por ejemplo, supongamos que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devuelve un formato RGB de 24 bits, con un tamaño de fotograma de 320 x 240 píxeles. Para obtener esta información, examine el tipo principal, el subtipo y el bloque de formato del tipo de medio:


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



La [**estructura \_ \_ \_ CAPS de configuración de VIDEO STREAM**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) proporciona el ancho y alto mínimo y máximo que se pueden usar para este tipo de medio. También proporciona el tamaño de "paso", que define los incrementos por los que puede ajustar el ancho o alto. Por ejemplo, el dispositivo podría devolver lo siguiente:

-   MinOutputSize: 160 x 120
-   MaxOutputSize: 320 x 240
-   OutputGranularityX: 8 píxeles (tamaño de paso horizontal)
-   OutputGranularityY: 8 píxeles (tamaño de paso vertical)

Dados estos números, podría establecer el ancho en cualquier parte del intervalo (160, 168, 176, ... 304, 312, 320) y la altura a cualquier punto del intervalo (120, 128, 136, ... 104, 112, 120). En el siguiente diagrama se muestra este proceso.

![tamaños de formato de vídeo](images/strmcap3.png)

Para establecer un nuevo tamaño de marco, modifique directamente la estructura [**\_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) devuelta en [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



A continuación, pase el tipo de medio al [**método SetFormat,**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) como se describió anteriormente.

Los **miembros MinFrameInterval** y **MaxFrameInterval** de los [**\_ \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de configuración de VIDEO STREAM son la longitud mínima y máxima de cada fotograma de vídeo, que puede traducir en velocidades de fotogramas como se muestra a continuación:

`frames per second = 10,000,000 / frame duration`

Para solicitar una velocidad de fotogramas determinada, modifique el valor de **AvgTimePerFrame** en la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) en el tipo de medio. Es posible que el dispositivo no admita todos los valores posibles entre el mínimo y el máximo, por lo que el controlador usará el valor más cercano que pueda. Para ver qué valor usó realmente el controlador, llame a [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) después de llamar a [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).

Algunos controladores pueden notificar **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) para el valor de **MaxFrameInterval**, lo que significa en efecto que no hay ninguna duración máxima. Sin embargo, es posible que quiera aplicar una velocidad de fotogramas mínima en la aplicación, como 1 fps.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los tipos de medios](about-media-types.md)
</dt> <dt>

[Configuración de un dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



