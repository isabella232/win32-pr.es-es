---
description: Crear el objeto multiplexor
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Crear el objeto multiplexor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275137"
---
# <a name="creating-the-multiplexer-object"></a>Crear el objeto multiplexor

El multiplexor de ASF es un objeto de capa WMContainer que funciona con el [objeto de datos ASF](asf-file-structure.md) y proporciona a una aplicación la capacidad de generar paquetes de datos ASF para flujos multimedia.

El objeto multiplexor expone la interfaz [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) . Para crear el multiplexor, llame a [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Esta función devuelve un puntero a un objeto vacío. Si la aplicación está escribiendo un nuevo archivo ASF, la aplicación debe inicializar el multiplexor con un objeto ContentInfo. Para ello, llame a [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). El objeto ContentInfo especificado representa el objeto de encabezado ASF del nuevo archivo. Para obtener información sobre cómo crear e inicializar el objeto ContentInfo para un nuevo archivo, consulte [inicializar el objeto ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).

El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analiza el objeto ContentInfo para recopilar información de configuración de la secuencia, como el número de flujos, el tamaño de paquete, el preajuste. Opcionalmente, el multiplexor también podría necesitar parámetros de depósito con fugas y unidades de extensión de carga. Esta información es necesaria para generar paquetes de datos que coincidan con los requisitos definidos en el objeto de encabezado ASF. El método **Initialize** configura el multiplexor según el tipo de medio y los valores de configuración de las secuencias. Por ejemplo, si una secuencia está configurada para tener extensiones de carga (consulte [creación y configuración de secuencias ASF](creating-and-configuring-asf-streams.md)) y, a continuación, el multiplexor está configurado para agregar esos valores a los paquetes de datos generados.

El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) también obtiene un identificador para el objeto de datos inicial que se creó durante la creación del objeto ContentInfo para escribir en él. Durante la generación de paquetes de datos, el multiplexor agrega paquetes al objeto de datos y los actualiza de forma adecuada. Una vez que el multiplexor genera todos los paquetes de datos, actualiza el objeto ContentInfo proporcionado para que se actualicen determinados valores, como el número de paquetes de datos.

En el ejemplo de código siguiente se muestra cómo crear un multiplexor e inicializarlo con un objeto ContentInfo.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



Para ver esta función usada en una aplicación completa, vea [Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Configuración de la inicialización del multiplexor y del depósito de fugas

El método [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura el multiplexor para determinar el flujo de datos del depósito con fugas. Para configurar estos parámetros, asegúrese de que se establecen los siguientes valores de propiedad en el objeto ContentInfo especificado. Para obtener información sobre cómo establecer estas propiedades, vea [establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).

-   [**MFPKEY \_ Propiedad de \_ \_ velocidad de bits autoajuste de ASFMEDIASINK**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) : indica si el multiplexor debe ajustar la velocidad de bits automáticamente para mantener el flujo de datos en el depósito de fugas. La aplicación puede cambiar esta configuración mediante una llamada a [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) y pasando el indicador de **\_ velocidad de \_ \_ bits autoajuste de multiplexador de MFASF** .

-   [**MFPKEY \_ Propiedad \_ \_ SENDTIME base ASFMEDIASINK**](mfpkey-asfmediasink-base-sendtime-property.md) : la hora de envío indica el momento en que se liberará la carga dentro del depósito de fugas. Las horas de envío deben ser iguales o anteriores a la hora de la presentación, ya que la carga debe tener tiempo para llegar al destino antes del tiempo de presentación.

    Este valor de propiedad es la primera hora de envío. El multiplexor usa este valor para calcular las horas de envío posteriores para asegurarse de que los datos fluyen a través del cubo. Si se ha establecido la marca de velocidad de bits **\_ \_ autoajuste \_ del multiplexor de MFASF** en el multiplexor, el multiplexor ajustará la velocidad de bits para que la carga se envíe cuando la ventana del búfer esté próxima a llenarse. Si no se establece la marca, el multiplexor no puede generar paquetes de datos debido a la saturación del ancho de banda.

El multiplexor obtiene información de configuración de secuencia del perfil ASF asociado al objeto ContentInfo especificado en el método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) . La información de configuración de la secuencia incluye parámetros de depósito con fugas. El multiplexor requiere este valor para generar paquetes de datos.

Para especificar los parámetros del depósito de fugas, establezca los valores del atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en el objeto de configuración de la secuencia que representa la secuencia del perfil. Para usar el valor de la ventana de búfer, que utiliza el codificador, llame a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). Solo se conoce el valor real de la ventana de búfer después de establecer el tipo de medio de salida del codificador. Para obtener información sobre cómo establecer el tipo de medio de salida, vea [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Los valores del depósito con fugas usados por el codificador pueden ser diferentes en el objeto ContentInfo proporcionado por el perfil ASF que se usó para crear el multiplexor.

 

El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) actualiza el objeto ContentInfo para que se reflejen los valores correctos en el objeto de encabezado ASF final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multiplexor ASF](asf-multiplexer.md)
</dt> <dt>

[Generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
