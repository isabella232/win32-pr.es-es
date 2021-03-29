---
description: Codificación de velocidad de bits constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codificación de velocidad de bits constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000866"
---
# <a name="constant-bit-rate-encoding"></a>Codificación de velocidad de bits constante

En la codificación de velocidad de bits constante (CBR), el codificador conoce la velocidad de bits de los ejemplos de medios de salida y la ventana de búfer (parámetros de cubo de fugas) antes de que comience la sesión de codificación. El codificador usa el mismo número de bits para codificar cada segundo de ejemplo a lo largo de la duración del archivo a fin de lograr la velocidad de bits de destino de una secuencia. Esto limita la variación en el tamaño de los ejemplos de flujo. Además, durante la sesión de codificación, la velocidad de bits no está exactamente en el valor especificado, pero permanece cerca de la velocidad de bits de destino.

La codificación CBR es útil cuando desea saber la velocidad de bits o la duración aproximada de un archivo sin tener que analizar todo el archivo. Esto es necesario en los escenarios de transmisión por secuencias en directo en los que el contenido multimedia debe transmitirse a una velocidad de bits predecible y con un uso de ancho de banda coherente.

La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante. Dado que el contenido es más difícil de comprimir, las partes de un flujo CBR serán de menor calidad que otras. Por ejemplo, una película típica tiene algunas escenas que son bastante estáticas y algunas escenas que están llenas de acción. Si codifica una película con CBR, las escenas que son estáticas y, por lo tanto, son fáciles de codificar de forma eficaz, tendrán una mayor calidad que las escenas de acción, lo que habría requerido tamaños de ejemplo más altos para mantener la misma calidad.

En general, las variaciones en la calidad de un archivo CBR son más pronunciadas a velocidades de bits inferiores. A velocidades de bits más altas, la calidad de un archivo con codificación CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario. Cuando se usa la codificación CBR, se debe establecer el ancho de banda tan alto como permita el escenario de entrega.

-   [Opciones de configuración CBR](#cbr-configuration-settings)
-   [Configuración del depósito de fugas](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Opciones de configuración CBR

Debe configurar un codificador especificando el tipo de codificación y los distintos valores específicos de la secuencia antes de la sesión de codificación.

**Para configurar el codificador para la codificación CBR**

1.  Especifique el modo de codificación CBR.

    De forma predeterminada, el codificador está configurado para usar codificación CBR. La configuración del codificador se establece a través de los valores de propiedad. Estas propiedades se definen en wmcodecdsp. h. Puede especificar explícitamente este modo estableciendo la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en Variant \_ false. Para obtener información sobre cómo establecer propiedades en los codificadores, vea [configurar el codificador](configuring-the-encoder.md).

2.  Elija la velocidad de bits de codificación.

    Para la codificación CBR, debe saber la velocidad de bits en la que desea codificar el flujo antes de que se inicie la sesión de codificación. Debe establecer la velocidad de bits durante la configuración del codificador. Para ello, mientras realiza la negociación de tipo de medio, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT AVG de \_ \_ velocidad**](mf-mt-avg-bitrate-attribute.md) de bits (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits de destino Para obtener más información, vea [negociación de tipos multimedia en el codificador](media-type-negotiation-on-the-encoder.md).

En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties. Esta función establece las propiedades de codificación de nivel de secuencia para CBR y VBR.


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a>Configuración del depósito de fugas

En el caso de la codificación CBR, el promedio y los valores máximos del depósito de fugas de la secuencia son los mismos. Para obtener más información acerca de estos parámetros, vea [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).

Para codificar secuencias de audio con CBR, debe establecer los valores del depósito con fugas después de negociar el tipo de medio de salida en el codificador. El codificador calcula la ventana del búfer internamente basándose en la velocidad de bits promedio establecida en el tipo de medio de salida.

Para establecer los valores del cubo con fugas, cree una matriz de DWORDs puede establecer los siguientes valores en la propiedad [**MFPKEY \_ ASFSTREAMSINK \_ corregida \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) en el almacén de propiedades del receptor de medios. Para obtener más información, vea [establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).

-   Velocidad de bits media: obtiene la velocidad de bits media del tipo de medio de salida que se selecciona durante la negociación del tipo de medio. Use el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .
-   Ventana de búfer: Consulte el codificador para la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) y, a continuación, llame a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).
-   Tamaño de búfer inicial: establézcalo en 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de codificación ASF](asf-encoding-types.md)
</dt> <dt>

[Tutorial: 1-pasar la codificación de Windows Media](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: escribir un archivo WMA con codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
