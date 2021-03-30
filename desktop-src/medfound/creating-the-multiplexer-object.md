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
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="71ff1-103">Crear el objeto multiplexor</span><span class="sxs-lookup"><span data-stu-id="71ff1-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="71ff1-104">El multiplexor de ASF es un objeto de capa WMContainer que funciona con el [objeto de datos ASF](asf-file-structure.md) y proporciona a una aplicación la capacidad de generar paquetes de datos ASF para flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="71ff1-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="71ff1-105">El objeto multiplexor expone la interfaz [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) .</span><span class="sxs-lookup"><span data-stu-id="71ff1-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="71ff1-106">Para crear el multiplexor, llame a [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span><span class="sxs-lookup"><span data-stu-id="71ff1-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="71ff1-107">Esta función devuelve un puntero a un objeto vacío.</span><span class="sxs-lookup"><span data-stu-id="71ff1-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="71ff1-108">Si la aplicación está escribiendo un nuevo archivo ASF, la aplicación debe inicializar el multiplexor con un objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="71ff1-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="71ff1-109">Para ello, llame a [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="71ff1-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="71ff1-110">El objeto ContentInfo especificado representa el objeto de encabezado ASF del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="71ff1-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="71ff1-111">Para obtener información sobre cómo crear e inicializar el objeto ContentInfo para un nuevo archivo, consulte [inicializar el objeto ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="71ff1-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="71ff1-112">El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analiza el objeto ContentInfo para recopilar información de configuración de la secuencia, como el número de flujos, el tamaño de paquete, el preajuste.</span><span class="sxs-lookup"><span data-stu-id="71ff1-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="71ff1-113">Opcionalmente, el multiplexor también podría necesitar parámetros de depósito con fugas y unidades de extensión de carga.</span><span class="sxs-lookup"><span data-stu-id="71ff1-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="71ff1-114">Esta información es necesaria para generar paquetes de datos que coincidan con los requisitos definidos en el objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="71ff1-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="71ff1-115">El método **Initialize** configura el multiplexor según el tipo de medio y los valores de configuración de las secuencias.</span><span class="sxs-lookup"><span data-stu-id="71ff1-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="71ff1-116">Por ejemplo, si una secuencia está configurada para tener extensiones de carga (consulte [creación y configuración de secuencias ASF](creating-and-configuring-asf-streams.md)) y, a continuación, el multiplexor está configurado para agregar esos valores a los paquetes de datos generados.</span><span class="sxs-lookup"><span data-stu-id="71ff1-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="71ff1-117">El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) también obtiene un identificador para el objeto de datos inicial que se creó durante la creación del objeto ContentInfo para escribir en él.</span><span class="sxs-lookup"><span data-stu-id="71ff1-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="71ff1-118">Durante la generación de paquetes de datos, el multiplexor agrega paquetes al objeto de datos y los actualiza de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="71ff1-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="71ff1-119">Una vez que el multiplexor genera todos los paquetes de datos, actualiza el objeto ContentInfo proporcionado para que se actualicen determinados valores, como el número de paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="71ff1-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="71ff1-120">En el ejemplo de código siguiente se muestra cómo crear un multiplexor e inicializarlo con un objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="71ff1-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


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



<span data-ttu-id="71ff1-121">Para ver esta función usada en una aplicación completa, vea [Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="71ff1-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="71ff1-122">Configuración de la inicialización del multiplexor y del depósito de fugas</span><span class="sxs-lookup"><span data-stu-id="71ff1-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="71ff1-123">El método [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura el multiplexor para determinar el flujo de datos del depósito con fugas.</span><span class="sxs-lookup"><span data-stu-id="71ff1-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="71ff1-124">Para configurar estos parámetros, asegúrese de que se establecen los siguientes valores de propiedad en el objeto ContentInfo especificado.</span><span class="sxs-lookup"><span data-stu-id="71ff1-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="71ff1-125">Para obtener información sobre cómo establecer estas propiedades, vea [establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="71ff1-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="71ff1-126">[**MFPKEY \_ Propiedad de \_ \_ velocidad de bits autoajuste de ASFMEDIASINK**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) : indica si el multiplexor debe ajustar la velocidad de bits automáticamente para mantener el flujo de datos en el depósito de fugas.</span><span class="sxs-lookup"><span data-stu-id="71ff1-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="71ff1-127">La aplicación puede cambiar esta configuración mediante una llamada a [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) y pasando el indicador de **\_ velocidad de \_ \_ bits autoajuste de multiplexador de MFASF** .</span><span class="sxs-lookup"><span data-stu-id="71ff1-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="71ff1-128">[**MFPKEY \_ Propiedad \_ \_ SENDTIME base ASFMEDIASINK**](mfpkey-asfmediasink-base-sendtime-property.md) : la hora de envío indica el momento en que se liberará la carga dentro del depósito de fugas.</span><span class="sxs-lookup"><span data-stu-id="71ff1-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="71ff1-129">Las horas de envío deben ser iguales o anteriores a la hora de la presentación, ya que la carga debe tener tiempo para llegar al destino antes del tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="71ff1-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="71ff1-130">Este valor de propiedad es la primera hora de envío.</span><span class="sxs-lookup"><span data-stu-id="71ff1-130">This property value is the first send time.</span></span> <span data-ttu-id="71ff1-131">El multiplexor usa este valor para calcular las horas de envío posteriores para asegurarse de que los datos fluyen a través del cubo.</span><span class="sxs-lookup"><span data-stu-id="71ff1-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="71ff1-132">Si se ha establecido la marca de velocidad de bits **\_ \_ autoajuste \_ del multiplexor de MFASF** en el multiplexor, el multiplexor ajustará la velocidad de bits para que la carga se envíe cuando la ventana del búfer esté próxima a llenarse.</span><span class="sxs-lookup"><span data-stu-id="71ff1-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="71ff1-133">Si no se establece la marca, el multiplexor no puede generar paquetes de datos debido a la saturación del ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="71ff1-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="71ff1-134">El multiplexor obtiene información de configuración de secuencia del perfil ASF asociado al objeto ContentInfo especificado en el método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) .</span><span class="sxs-lookup"><span data-stu-id="71ff1-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="71ff1-135">La información de configuración de la secuencia incluye parámetros de depósito con fugas.</span><span class="sxs-lookup"><span data-stu-id="71ff1-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="71ff1-136">El multiplexor requiere este valor para generar paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="71ff1-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="71ff1-137">Para especificar los parámetros del depósito de fugas, establezca los valores del atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en el objeto de configuración de la secuencia que representa la secuencia del perfil.</span><span class="sxs-lookup"><span data-stu-id="71ff1-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="71ff1-138">Para usar el valor de la ventana de búfer, que utiliza el codificador, llame a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="71ff1-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="71ff1-139">Solo se conoce el valor real de la ventana de búfer después de establecer el tipo de medio de salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="71ff1-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="71ff1-140">Para obtener información sobre cómo establecer el tipo de medio de salida, vea [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="71ff1-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="71ff1-141">Los valores del depósito con fugas usados por el codificador pueden ser diferentes en el objeto ContentInfo proporcionado por el perfil ASF que se usó para crear el multiplexor.</span><span class="sxs-lookup"><span data-stu-id="71ff1-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="71ff1-142">El método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) actualiza el objeto ContentInfo para que se reflejen los valores correctos en el objeto de encabezado ASF final.</span><span class="sxs-lookup"><span data-stu-id="71ff1-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71ff1-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71ff1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ff1-144">Multiplexor ASF</span><span class="sxs-lookup"><span data-stu-id="71ff1-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="71ff1-145">Generación de nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="71ff1-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
