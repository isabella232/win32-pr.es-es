---
description: 'En la velocidad de bits variable (VBR) restringida, el contenido se codifica en una velocidad de bits y valores máximos especificados: una velocidad de bits máxima y una ventana de búfer máximo.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained codificación de velocidad de bits variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715513"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained codificación de velocidad de bits variable

En la velocidad de bits variable (VBR) restringida, el contenido se codifica en una velocidad de bits y *valores máximos* especificados: una velocidad de bits máxima y una ventana de búfer máximo. Estos valores máximos también se denominan los valores de los *depósitos máximos de fugas*. El archivo está codificado para ajustarse a un búfer descrito por los valores máximos, de modo que la velocidad de bits media general de la secuencia sea igual o menor que el valor de velocidad de bits promedio especificado.

Normalmente, la velocidad de bits máxima es bastante alta. El codificador garantiza que el valor de velocidad de bits promedio especificado se mantiene a lo largo de la duración de la secuencia (velocidad de bits media >= (tamaño de flujo total en bits/duración de flujo en segundos)). Considere el ejemplo siguiente: configure una secuencia con una velocidad de bits media de 16.000 bits por segundo, una velocidad de bits máxima de 48.000 bits por segundo y una ventana de búfer máximo de 3.000 (3 segundos). El tamaño del búfer usado para el flujo es de 144.000 bits (48.000 bits por segundo \* 3 segundos), según lo determinen los valores máximos. El codificador comprime los datos para que se ajusten a ese búfer. Además, la velocidad de bits media de la secuencia debe ser de 16.000 o inferior. Si el codificador debe crear ejemplos grandes para controlar un segmento complejo de contenido, puede aprovechar el tamaño de búfer grande. Sin embargo, otras partes de la secuencia deben codificarse a una velocidad de bits más baja para reducir el promedio hasta el nivel especificado. La codificación VBR máxima limitada es útil para dispositivos de reproducción con una capacidad de búfer finita y restricciones de velocidad de datos. Un ejemplo común es la codificación que se usa para DVDs cuando la descodificación se realiza mediante un chip de un dispositivo, donde hay limitaciones de hardware que deben tenerse en cuenta.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configuración del codificador para Peak-Constrained VBR

La VBR máxima restringida es como [VBR no restringida](unconstrained-variable-bit-rate--vbr--encoding.md) , ya que se limita a una velocidad de bits promedio a lo largo de la secuencia. Además, la VBR máxima restringida se ajusta a un búfer máximo. Este búfer se describe con una velocidad de bits máxima y una ventana de búfer máximo. Este modo utiliza dos fases de codificación y proporciona la flexibilidad del codificador en cómo codifica los ejemplos individuales al tiempo que se respetan las limitaciones máximas.

La configuración del codificador se establece a través de los valores de propiedad. Estas propiedades se definen en wmcodecdsp. h. Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida. Para obtener información sobre cómo establecer propiedades en el codificador, consulte [configuración del codificador](configuring-the-encoder.md). En función de los valores de propiedad especificados, puede enumerar los tipos de salida VBR admitidos y seleccionar el que se requiera en la transformación del codificador [Media Foundation](media-foundation-transforms.md) (MFT) en función de la velocidad de bits media.

Debe establecer el siguiente valor de propertiesfor en este tipo de codificación:

-   Especifique el modo de codificación VBR estableciendo la propiedad MFPKEY \_ VBRENABLED en Variant \_ true.
-   Establezca MFPKEY \_ PASSESUSED en 2 porque el modo VBR restringido de pico utiliza dos fases de codificación.
-   Establezca MFPKEY \_ RMAX para especificar la velocidad de bits máxima y establezca MFPKEY \_ Bmax para especificar la ventana de búfer máximo.
-   Durante la enumeración del tipo de medio de salida, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT \_ AVG \_**](mf-mt-avg-bitrate-attribute.md) Rate (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits promedio deseada que desea que el Para obtener más información acerca de cómo seleccionar el tipo de medio de salida, consulte [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Se recomienda establecer la velocidad de bits máxima en al menos dos veces la velocidad de bits promedio. Si se establece la tasa máxima en un valor inferior, el codificador puede codificar el contenido como CBR de dos pasos en lugar de VBR limitada.

 

Para obtener el valor de la ventana de búfer establecido por el codificador, llame a **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido en wmcodecifaces. h, wmcodecdspuuid. lib, después de la sesión de codificación. Para agregar compatibilidad con VBR no restringida para las secuencias, debe establecer este valor en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valores de cubo con fugas máximas) en el objeto de configuración de la secuencia mientras configura el perfil ASF.

En el ejemplo de código siguiente se modifica el método SetEncodingType de la clase de ejemplo CEncoder para configurar el modo VBR con restricción máxima. Para obtener información sobre esta clase, vea [código de ejemplo del codificador](encoder-example-code.md). Para obtener información sobre las macros auxiliares que se usan en este ejemplo, vea usar los ejemplos de código de Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de codificación ASF](asf-encoding-types.md)
</dt> <dt>

[El modelo de búfer de depósito con fugas](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Cómo crear una topología para Two-Pass la codificación de Windows Media](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



