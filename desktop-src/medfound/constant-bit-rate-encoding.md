---
description: Codificación de velocidad de bits constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codificación de velocidad de bits constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318cbf6d1a0b9c635fcd8313589581839fe74c7402411d59a1b5dfbdb55739d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974834"
---
# <a name="constant-bit-rate-encoding"></a>Codificación de velocidad de bits constante

En la codificación de velocidad de bits constante (CBR), el codificador conoce la velocidad de bits de los ejemplos de medios de salida y la ventana de búfer (parámetros de cubo de pérdida) antes de que comience la sesión de codificación. El codificador usa el mismo número de bits para codificar cada segundo de la muestra a lo largo de la duración del archivo para lograr la velocidad de bits de destino de una secuencia. Esto limita la variación en el tamaño de los ejemplos de secuencia. Además, durante la sesión de codificación, la velocidad de bits no está exactamente en el valor especificado, pero permanece cerca de la velocidad de bits de destino.

La codificación CBR es útil cuando desea saber la velocidad de bits o la duración aproximada de un archivo sin tener que analizar todo el archivo. Esto es necesario en los escenarios de transmisión por secuencias en directo en los que el contenido multimedia debe transmitirse a una velocidad de bits predecible y con un uso de ancho de banda coherente.

La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante. Dado que algunos contenidos son más difíciles de comprimir, las partes de una secuencia CBR serán de menor calidad que otras. Por ejemplo, una película típica tiene algunas escenas bastante estáticas y otras que están llenas de acción. Si codifica una película mediante CBR, las escenas estáticas y, por tanto, fáciles de codificar de forma eficaz, serán de mayor calidad que las escenas de acción, lo que habría requerido tamaños de muestra más altos para mantener la misma calidad.

En general, las variaciones en la calidad de un archivo CBR se pronuncian más a velocidades de bits más bajas. A velocidades de bits más altas, la calidad de un archivo codificado con CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario. Al usar la codificación CBR, debe establecer el ancho de banda tan alto como lo permita el escenario de entrega.

-   [Configuración de CBR Configuración](#cbr-configuration-settings)
-   [Pérdida de cubos Configuración](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Configuración de CBR Configuración

Debe configurar un codificador especificando el tipo de codificación y los distintos valores específicos de la secuencia antes de la sesión de codificación.

**Para configurar el codificador para la codificación CBR**

1.  Especifique el modo de codificación CBR.

    De forma predeterminada, el codificador está configurado para usar la codificación CBR. La configuración del codificador se establece a través de valores de propiedad. Estas propiedades se definen en wmcodecdsp.h. Puede especificar explícitamente este modo estableciendo la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en VARIANT \_ FALSE. Para obtener información sobre cómo establecer propiedades en codificadores, vea [Configuring the Encoder](configuring-the-encoder.md).

2.  Elija la velocidad de bits de codificación.

    Para la codificación CBR, debe conocer la velocidad de bits a la que desea codificar la secuencia antes de que comience la sesión de codificación. Debe establecer la velocidad de bits durante la configuración del codificador. Para ello, mientras realiza la negociación de tipos de medios, compruebe el atributo AVG BYTES PER [**\_ \_ \_ \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) de MF MT AUDIO (para secuencias de audio) o el atributo [**AVG \_ \_ \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) de MF MT (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits objetivo que desea lograr. Para obtener más información, vea [Negociación de tipos de medios en el codificador](media-type-negotiation-on-the-encoder.md).

En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties. Esta función establece las propiedades de codificación de nivel de flujo para CBR y VBR.


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



### <a name="leaky-bucket-settings"></a>Pérdida de cubos Configuración

Para la codificación CBR, los valores promedio y máximo del cubo de pérdidas para la secuencia son los mismos. Para obtener más información sobre estos parámetros, vea [El modelo de búfer de cubos con pérdidas.](the-leaky-bucket-buffer-model.md)

Para codificar secuencias de audio con CBR, debe establecer los valores del cubo de fugas después de negociar el tipo de medio de salida en el codificador. El codificador calcula la ventana de búfer internamente en función de la velocidad de bits media establecida en el tipo de medio de salida.

Para establecer valores de cubo con fugas, cree una matriz de DWORDs puede establecer los siguientes valores en la propiedad [**\_ MFPKEY ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) en el almacén de propiedades del receptor de medios. Para obtener más información, vea [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).

-   Velocidad de bits media: obtenga la velocidad de bits media del tipo de medio de salida seleccionado durante la negociación del tipo de medio. Use el [**atributo MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND.**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   Ventana búfer: consulte el codificador para la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) y, a continuación, llame a [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).
-   Tamaño inicial del búfer: se establece en 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de codificación asf](asf-encoding-types.md)
</dt> <dt>

[Tutorial: Codificación de medios Windows paso 1](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: Escritura de un archivo WMA mediante la codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
