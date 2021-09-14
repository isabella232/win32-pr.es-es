---
description: Crear el objeto multiplexor
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Crear el objeto multiplexor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263399"
---
# <a name="creating-the-multiplexer-object"></a>Crear el objeto multiplexor

El multiplexor de ASF es un objeto de capa WMContainer que funciona con el objeto de datos [de ASF](asf-file-structure.md) y ofrece a una aplicación la capacidad de generar paquetes de datos de ASF para secuencias multimedia.

El objeto multiplexor expone la [**interfaz DEMAFMultiplexer.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) Para crear el multiplexor, llame [**a MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Esta función devuelve un puntero a un objeto vacío. Si la aplicación está escribiendo un nuevo archivo ASF, la aplicación debe inicializar el multiplexor con un objeto ContentInfo. Para ello, llame a [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). El objeto ContentInfo especificado representa el objeto de encabezado ASF del nuevo archivo. Para obtener información sobre cómo crear e inicializar el objeto ContentInfo para un nuevo archivo, vea Inicializar el objeto [ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).

El [**método Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analiza el objeto ContentInfo para recopilar información de configuración de secuencias, como el número de secuencias, el tamaño del paquete y la inscripción previa. Opcionalmente, el multiplexador también podría necesitar parámetros de cubo con pérdidas y las unidades de extensión de carga. Esta información es necesaria para generar paquetes de datos que coincidan con los requisitos definidos en el objeto de encabezado asf. El **método Initialize** configura el multiplexor en función del tipo de medio y los valores de configuración de las secuencias. Por ejemplo, si una secuencia está configurada para tener extensiones de carga (consulte Creación y configuración de [ASF Secuencias)](creating-and-configuring-asf-streams.md)y, a continuación, el multiplexador se configura para agregar esos valores a los paquetes de datos generados.

El [**método Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) también obtiene un identificador para el objeto de datos inicial que se creó durante la creación del objeto ContentInfo para su escritura. Durante la generación de paquetes de datos, el multiplexor agrega paquetes al objeto de datos y los actualiza correctamente. Una vez que el multiplexor genera todos los paquetes de datos, actualiza el objeto ContentInfo proporcionado para que se actualicen determinados valores, como el número de paquetes de datos.

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



Para ver esta función usada en una aplicación completa, vea Tutorial: Copia de [ASF Secuencias de un archivo a otro.](tutorial--copying-asf-streams-from-one-file-to-another.md)

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Inicialización de multiplexador y depósito de pérdidas Configuración

El [**método IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura el multiplexor para determinar el flujo de datos del cubo con fugas. Para configurar estos parámetros, asegúrese de que los siguientes valores de propiedad están establecidos en el objeto ContentInfo especificado. Para obtener información sobre cómo establecer estas propiedades, vea [Establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).

-   [**MFPKEY \_ Propiedad \_ AUTOADJUST \_ BITRATE de ASFMEDIASINK:**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) indica si el multiplexor debe ajustar automáticamente la velocidad de bits para mantener el flujo de datos en el cubo de pérdidas. Esta configuración se puede cambiar mediante la aplicación llamando a [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) y pasando la marca **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE.**

-   [**MFPKEY \_ Propiedad ASFMEDIASINK \_ BASE \_ SENDTIME:**](mfpkey-asfmediasink-base-sendtime-property.md) el tiempo de envío indica cuándo se liberará la carga dentro del depósito de pérdidas. Los tiempos de envío deben ser iguales o anteriores al tiempo de presentación, ya que la carga debe tener tiempo para llegar al destino antes del tiempo de presentación.

    Este valor de propiedad es la primera vez que se envía. El multiplexor usa este valor para calcular los tiempos de envío subsiguientes para asegurarse de que los datos fluyen a través del cubo de forma constante. Si se ha establecido la marca **\_ \_ MFASF MULTIPLEXER AUTOADJUST \_ BITRATE** en el multiplexor, el multiplexor ajustará la velocidad de bits para que la carga se envíe cuando la ventana del búfer esté a punto de estar llena. Si no se establece la marca, el multiplexor no puede generar paquetes de datos debido a la saturación del ancho de banda.

El multiplexor obtiene información de configuración de secuencias del perfil de ASF asociado al objeto ContentInfo especificado en el [**método Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) La información de configuración del flujo incluye parámetros de cubo con fugas. El multiplexor requiere este valor para generar paquetes de datos.

Para especificar los parámetros del cubo de fugas, establezca los valores del atributo [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en el objeto de configuración de flujo que representa la secuencia en el perfil. Para usar el valor de la ventana de búfer, que usa el codificador, llame a [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). El valor real de la ventana de búfer solo se conoce después de establecer el tipo de medio de salida del codificador. Para obtener información sobre cómo establecer el tipo de medio de salida, vea [Negociación de tipos de medios en el codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Los valores del cubo de pérdida usados por el codificador pueden ser diferentes en el objeto ContentInfo proporcionado por el perfil de ASF que se usó para crear el multiplexor.

 

El [**método Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) actualiza el objeto ContentInfo para que los valores correctos se reflejen en el objeto de encabezado ASF final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multiplexor de ASF](asf-multiplexer.md)
</dt> <dt>

[Generación de nuevos paquetes de datos de ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
