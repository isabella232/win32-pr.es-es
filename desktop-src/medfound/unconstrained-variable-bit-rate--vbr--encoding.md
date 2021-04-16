---
description: Codificación de velocidad de bits variable sin restricciones
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codificación de velocidad de bits variable sin restricciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696866"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a>Codificación de velocidad de bits variable sin restricciones

En el modo de codificación de velocidad de bits variable (VBR) sin restricciones, el contenido se codifica con la máxima calidad posible manteniendo una velocidad de bits especificada.

La codificación VBR sin restricciones utiliza dos fases de codificación. Cuando se usa la codificación VBR sin restricciones, se especifica una velocidad de bits para la secuencia, tal y como se haría con la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md). Sin embargo, el codificador usa este valor solo como la velocidad de bits promedio para el flujo y codificaciones para que la calidad sea lo más alta posible mientras se mantiene el promedio. Los ejemplos individuales generados por el codificador varían en tamaño sin ningún límite explícito de búfer. Sin embargo, la velocidad de bits media durante la sesión de codificación y la duración de la secuencia no debe ser superior al valor especificado por el usuario. La velocidad de bits real en cualquier punto de la secuencia codificada puede variar considerablemente respecto al valor medio. No se establece una ventana de búfer para la codificación VBR sin restricciones. En su lugar, el codificador calcula el tamaño de la ventana de búfer necesaria en función de los requisitos de los ejemplos codificados. Esto significa que no hay ningún límite en el tamaño de los ejemplos individuales de la secuencia, siempre que la velocidad de bits media sea menor o igual que el valor establecido.

La ventaja de la codificación VBR no restringida es que el flujo comprimido tiene la máxima calidad posible y permanece dentro de un ancho de banda medio predecible. Úselo si necesita especificar un ancho de banda, pero se aceptan las fluctuaciones en torno al ancho de banda especificado. por ejemplo, para archivos locales o solo descarga.

El inconveniente de este modo de codificación es que el codificador puede establecer la ventana del búfer en el valor que sea necesario después de la codificación, lo que no le permite controlar el tamaño del búfer. En la mayoría de los casos, si no le preocupa el tamaño del búfer o la coherencia del uso de ancho de banda, debe usar la [codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md) .

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Configuración del codificador para VBR sin restricciones

La configuración del codificador se establece a través de los valores de propiedad. Estas propiedades se definen en wmcodecdsp. h. Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida. Para obtener información sobre cómo establecer propiedades en el codificador, consulte [configuración del codificador](configuring-the-encoder.md). En función de los valores de propiedad especificados, puede enumerar los tipos de salida VBR admitidos y seleccionar el que se requiera en la transformación del codificador [Media Foundation](media-foundation-transforms.md) (MFT) en función de la velocidad de bits media.

En la lista siguiente se muestran las propiedades que se deben establecer para este tipo de codificación:

-   Especifique el modo de codificación VBR estableciendo la propiedad MFPKEY \_ VBRENABLED en Variant \_ true.
-   Establezca MFPKEY \_ PASSESUSED en 2 porque el modo VBR sin restricciones utiliza dos fases de codificación.
-   Mientras enumera el tipo de medio de salida, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT \_ AVG de velocidad de \_ bits**](mf-mt-avg-bitrate-attribute.md) (para secuencias de vídeo) de los tipos de medios de salida disponibles. Elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits promedio deseada que desea que el codificador mantenga en el contenido codificado. Para obtener más información acerca de cómo seleccionar el tipo de medio de salida, consulte [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).

Para obtener el valor de la ventana de búfer establecido por el codificador, llame a **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido en wmcodecifaces. h y wmcodecdspuuid. lib, después de la sesión de codificación. Para agregar compatibilidad con VBR no restringida para las secuencias, debe establecer este valor en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores de depósito de pérdida promedio) en el objeto de configuración de la secuencia mientras configura el perfil ASF.

A continuación se modifica el método SetEncodingType de la clase de ejemplo CEncoder para configurar el modo VBR sin restricciones. Para obtener información sobre esta clase, vea [código de ejemplo del codificador](encoder-example-code.md). Para obtener información sobre las macros auxiliares que se usan en este ejemplo, vea usar los ejemplos de código de Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
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

 

 



