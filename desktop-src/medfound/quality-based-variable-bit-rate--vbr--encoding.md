---
description: Quality-Based codificación de velocidad de bits variable
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based codificación de velocidad de bits variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19c2cd63d5bc6f777f702827e999cd9d2ae2a272194f4b776205c1581376256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722205"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based codificación de velocidad de bits variable

A diferencia de la codificación de velocidad de bits [constante](constant-bit-rate-encoding.md) (CBR), donde el codificador se esfuerza por mantener una velocidad de bits determinada de los medios codificados, en el modo de velocidad de bits variable (VBR), el codificador se esfuerza por lograr la mejor calidad posible de los medios codificados. La diferencia principal entre CBR y VBR es el tamaño de la ventana de búfer utilizada. Las secuencias codificadas con VBR suelen tener ventanas de búfer grandes en comparación con las secuencias codificadas en CBR.

La calidad del contenido codificado viene determinada por la cantidad de datos que se pierden cuando se comprime el contenido. Muchos factores afectan a la pérdida de datos en el proceso de compresión. pero, en general, cuanto más complejos son los datos originales y mayor es la relación de compresión, más detalles se pierden en el proceso de compresión.

En el modo VBR basado en calidad, no se define una velocidad de bits ni una ventana de búfer que el codificador debe seguir. En su lugar, especifique un nivel de calidad para una secuencia multimedia digital en lugar de una velocidad de bits. El codificador comprime el contenido para que todas las muestras sean de una calidad comparable; esto garantiza que la calidad sea coherente a lo largo de la duración de reproducción, independientemente de los requisitos de búfer de la secuencia resultante.

La codificación VBR basada en calidad tiende a crear flujos comprimidos de gran tamaño. En general, este tipo de codificación es adecuado para la reproducción local o las conexiones de red de ancho de banda alto (o descargar y reproducir). Por ejemplo, puede escribir una aplicación para copiar canciones de cd a archivos ASF en un equipo. El uso de la codificación VBR basada en calidad garantizaría que todas las canciones copiadas sean de la misma calidad. En esos casos, la calidad coherente proporcionará una mejor experiencia de usuario.

La desventaja de la codificación VBR basada en calidad es que realmente no hay ninguna manera de conocer los requisitos de tamaño o ancho de banda de los medios codificados antes de la sesión de codificación, porque el codificador usa un solo paso de codificación. Esto puede hacer que los archivos codificados en VBR basados en calidad sean inadecuados en circunstancias en las que la memoria o el ancho de banda están restringidos, como la reproducción de contenido en reproductores multimedia portátiles o el streaming a través de una red de ancho de banda bajo.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Configuración del codificador para la codificación Quality-Based VBR

La configuración del codificador se establece a través de valores de propiedad. Estas propiedades se definen en wmcodecdsp.h. Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida. Para obtener información sobre cómo establecer propiedades en el codificador, vea [Configuring the Encoder](configuring-the-encoder.md).

En la lista siguiente se muestran las propiedades que debe establecer para este tipo de codificación:

-   Especifique el modo de codificación de VBR estableciendo la **propiedad MFPKEY \_ VBRENABLED** en VARIANT \_ TRUE.
-   Establezca **MFPKEY \_ PASSESUSED en** 1 porque este modo VBR usa un paso de codificación.
-   Establezca el nivel de calidad deseado (de 0 a 100) estableciendo la propiedad **MFPKEY \_ DESIRED \_ VBRQUALITY.** VBR basado en calidad no codifica el contenido en ningún parámetro de búfer predefinido. Este nivel de calidad que se mantendrá para toda la secuencia, independientemente de los requisitos de velocidad de bits resultantes.
-   En el caso de las secuencias de vídeo, establezca la velocidad de bits media en un valor distinto de cero en el atributo [**\_ MF MT AVG \_ \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio de salida del codificador. La velocidad de bits precisa se actualiza una vez completada la sesión de codificación.

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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de codificación asf](asf-encoding-types.md)
</dt> </dl>

 

 



