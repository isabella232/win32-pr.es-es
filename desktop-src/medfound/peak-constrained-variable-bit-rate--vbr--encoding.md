---
description: 'En la velocidad de bits variable con límite máximo (VBR), el contenido se codifica en una velocidad de bits y valores máximos especificados: una velocidad de bits máxima y una ventana de búfer máximo.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained codificación de velocidad de bits variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580269"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained codificación de velocidad de bits variable

En la velocidad de bits variable con límite máximo (VBR), el contenido se codifica en una velocidad de bits y valores máximos especificados: una velocidad de bits máxima y una ventana de búfer máximo. Estos valores máximos también se denominan *los valores máximos del depósito* de pérdida. El archivo se codifica para ajustarse a un búfer descrito por los valores máximos, de forma que la velocidad de bits media total de la secuencia sea igual o menor que el valor de velocidad de bits promedio especificado.

Normalmente, la velocidad de bits máxima es bastante alta. El codificador garantiza que el valor de velocidad de bits promedio especificado se mantiene durante la duración de la secuencia (promedio de velocidad de bits >= (tamaño total de la secuencia en bits/duración de la secuencia en segundos). Considere el ejemplo siguiente: configure una secuencia con una velocidad de bits media de 16 000 bits por segundo, una velocidad de bits máxima de 48 000 bits por segundo y una ventana de búfer máxima de 3000 (3 segundos). El tamaño del búfer usado para la secuencia es de 144 000 bits (48 000 bits por segundo y 3 segundos) determinado por los valores \* máximos. El codificador comprime los datos para que se ajusten a ese búfer. Además, la velocidad de bits media de la secuencia debe ser de 16 000 o menos. Si el codificador debe crear muestras grandes para controlar un segmento complejo de contenido, puede aprovechar el tamaño de búfer grande. Sin embargo, otras partes de la secuencia deben codificarse a una velocidad de bits inferior para reducir el promedio al nivel especificado. La codificación VBR con límite máximo es útil para los dispositivos de reproducción con una capacidad de búfer finita y restricciones de velocidad de datos. Un ejemplo común de esto es la codificación que se usa para los DVD cuando la codificación se realiza mediante un chip en un dispositivo, donde hay limitaciones de hardware que deben tenerse en cuenta.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configuración del codificador para Peak-Constrained VBR

VBR con restricciones máximas es como VBR sin [restricciones,](unconstrained-variable-bit-rate--vbr--encoding.md) ya que se limita a una velocidad de bits media durante la secuencia. Además, VBR con restricciones máximas se ajusta a un búfer máximo. Este búfer se describe mediante una velocidad de bits máxima y una ventana de búfer máximo. Este modo usa dos pases de codificación y proporciona al codificador flexibilidad en la forma en que codifica muestras individuales a la vez que se cumplen las limitaciones máximas.

La configuración del codificador se establece a través de valores de propiedad. Estas propiedades se definen en wmcodecdsp.h. Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida. Para obtener información sobre cómo establecer propiedades en el codificador, vea [Configuring the Encoder](configuring-the-encoder.md). En función de los valores de propiedad especificados, puede enumerar los tipos de salida de VBR admitidos y seleccionar el necesario en el codificador [Media Foundation transform](media-foundation-transforms.md) (MFT) en función de la velocidad de bits media.

Debe establecer las siguientes propiedades para este tipo de codificación:

-   Especifique el modo de codificación de VBR estableciendo la propiedad MFPKEY \_ VBRENABLED en VARIANT \_ TRUE.
-   Establezca MFPKEY PASSESUSED en 2 porque el modo VBR con restricciones \_ máximas usa dos pases de codificación.
-   Establezca MFPKEY RMAX para especificar la velocidad de bits máxima y \_ establezca MFPKEY \_ BMAX para especificar la ventana de búfer máximo.
-   Al enumerar el tipo de medio de salida, compruebe el atributo [**MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para secuencias de audio) o el atributo [**MF MT AVG \_ \_ \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits media deseada que desea que el codificador mantenga en el contenido codificado. Para obtener más información sobre cómo seleccionar el tipo de medio de salida, vea [Negociación de tipos de medios en el codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Se recomienda establecer la velocidad de bits máxima en al menos el doble de la velocidad de bits media. Si se establece la velocidad máxima en un valor inferior, el codificador puede codificar el contenido como CBR de dos pases en lugar de VBR con restricciones máximas.

 

Para obtener el valor de la ventana de búfer establecido por el codificador, llame a **IWMCodecLeakyBucket::GetBufferSizeBits**, definido en wmcodecifaces.h, wmcodecdspuuid.lib, después de la sesión de codificación. Para agregar compatibilidad con VBR sin restricciones para las secuencias, debe establecer este valor en el atributo [**\_ \_ LEAKYBUCKET2 de ASFSTREAMCONFIG**](mf-asfstreamconfig-leakybucket2-attribute.md) DE MF (valores máximos de cubo de pérdida) en el objeto de configuración de flujo al configurar el perfil de ASF.

En el ejemplo de código siguiente se modifica el método SetEncodingType de la clase de ejemplo CEncoder para configurar el modo VBR con restricciones máximas. Para obtener información sobre esta clase, vea [Código de ejemplo de codificador](encoder-example-code.md). Para obtener información sobre las macros auxiliares usadas en este ejemplo, vea Using the Media Foundation Code Examples.


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

[Tipos de codificación asf](asf-encoding-types.md)
</dt> <dt>

[El modelo de búfer de cubo filtrada](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Cómo crear una topología para la codificación Two-Pass Windows multimedia](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



