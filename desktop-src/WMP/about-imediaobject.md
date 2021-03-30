---
title: Acerca de IMediaObject
description: Acerca de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IMediaObject
- complementos, interfaz IMediaObject
- Complementos de procesamiento de señal digital, interfaz IMediaObject
- Complementos DSP, interfaz IMediaObject
- Interfaz IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773584"
---
# <a name="about-imediaobject"></a><span data-ttu-id="e458d-113">Acerca de IMediaObject</span><span class="sxs-lookup"><span data-stu-id="e458d-113">About IMediaObject</span></span>

<span data-ttu-id="e458d-114">La interfaz **IMediaObject** es la interfaz necesaria para DMOs.</span><span class="sxs-lookup"><span data-stu-id="e458d-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="e458d-115">**IMediaObject** contiene los métodos que usa un complemento DSP de Windows Media Player para obtener datos de Windows Media Player, para procesar los datos y para devolver los datos procesados a Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="e458d-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="e458d-116">Para obtener la documentación completa de la interfaz **IMediaObject** , consulte la sección DirectShow de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e458d-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="e458d-117">Los métodos de **IMediaObject** se pueden categorizar de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="e458d-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="e458d-118">Métodos que controlan la negociación de formato</span><span class="sxs-lookup"><span data-stu-id="e458d-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="e458d-119">Estos son los métodos que Windows Media Player llama para obtener información sobre los formatos de datos admitidos por el complemento.</span><span class="sxs-lookup"><span data-stu-id="e458d-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="e458d-120">Esos métodos incluyen:</span><span class="sxs-lookup"><span data-stu-id="e458d-120">These methods include:</span></span>

-   <span data-ttu-id="e458d-121">**GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="e458d-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="e458d-122">**GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="e458d-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="e458d-123">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="e458d-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="e458d-124">**GetInputType**</span><span class="sxs-lookup"><span data-stu-id="e458d-124">**GetInputType**</span></span>
-   <span data-ttu-id="e458d-125">**GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="e458d-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="e458d-126">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="e458d-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="e458d-127">**GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="e458d-127">**GetOutputType**</span></span>
-   <span data-ttu-id="e458d-128">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="e458d-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="e458d-129">**SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="e458d-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="e458d-130">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="e458d-130">**SetInputType**</span></span>
-   <span data-ttu-id="e458d-131">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="e458d-131">**SetOutputType**</span></span>

<span data-ttu-id="e458d-132">Algunos de estos métodos, como **GetInputType** y **SetInputType**, usan la estructura **de \_ \_ tipo de medio DMO** para describir el formato de los datos usados por un flujo.</span><span class="sxs-lookup"><span data-stu-id="e458d-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="e458d-133">Cuando Windows Media Player llama a estos métodos, proporciona un puntero a una estructura de **\_ \_ tipo de medio DMO** .</span><span class="sxs-lookup"><span data-stu-id="e458d-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="e458d-134">Si un método como **SetInputType** especifica la información de tipo de medio, el complemento debe copiar la estructura **de \_ \_ tipo de medio DMO** en una variable miembro e inspeccionar sus miembros de datos para determinar el tipo de datos que Windows Media Player proporcionará en el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="e458d-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="e458d-135">Si un método como **GetInputType** recupera la información de tipo de archivo multimedia, el complemento debe copiar la dirección de la variable miembro que contiene la estructura de **\_ \_ tipo de medio DMO** en el puntero proporcionado por Media Player de Windows en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="e458d-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="e458d-136">Windows Media Player usa principalmente dos miembros de la estructura de **\_ \_ tipo de medio DMO** :</span><span class="sxs-lookup"><span data-stu-id="e458d-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="e458d-137">**majortype**: un identificador único global (GUID) que especifica la categoría general del medio, como audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="e458d-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="e458d-138">**SubType**: un GUID que especifica una descripción más detallada del medio, como audio PCM.</span><span class="sxs-lookup"><span data-stu-id="e458d-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="e458d-139">Estos GUID se pueden encontrar en el encabezado denominado UUID. h, que se incluye con el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e458d-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="e458d-140">Los métodos como **GetInputSizeInfo** proporcionan información a Windows Media Player sobre cuánta memoria se necesita para asignar los búferes de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e458d-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="e458d-141">Los métodos como **GetStreamCount** y **GetOutputStreamInfo** proporcionan información a Windows Media Player sobre el número y el carácter de las secuencias admitidas por el complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="e458d-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="e458d-142">**GetInputMaxLatency** y **SetInputMaxLatency** se implementan mediante DMOs en casos especiales.</span><span class="sxs-lookup"><span data-stu-id="e458d-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="e458d-143">Los complementos DSP de Windows Media Player deben devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e458d-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="e458d-144">Métodos que especifican o recuperan información de estado</span><span class="sxs-lookup"><span data-stu-id="e458d-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="e458d-145">Estos son los métodos que Windows Media Player llama para obtener o establecer valores relacionados con el estado actual del complemento.</span><span class="sxs-lookup"><span data-stu-id="e458d-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="e458d-146">Esos métodos incluyen:</span><span class="sxs-lookup"><span data-stu-id="e458d-146">These methods include:</span></span>

-   <span data-ttu-id="e458d-147">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="e458d-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="e458d-148">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="e458d-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="e458d-149">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="e458d-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="e458d-150">**GetInputCurrentType** y **GetOutputCurrentType** usan la estructura de **\_ \_ tipo de medio DMO** para devolver información a Windows Media Player acerca de los tipos de medios previamente establecidos para los flujos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="e458d-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="e458d-151">**GetInputStatus** devuelve una marca que indica a Windows Media Player si el complemento DSP puede aceptar datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e458d-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="e458d-152">Métodos que controlan los datos de procesamiento y almacenamiento en búfer</span><span class="sxs-lookup"><span data-stu-id="e458d-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="e458d-153">Estos son los métodos que Windows Media Player llama para iniciar los distintos procesos que el complemento realiza para realizar el procesamiento de la señal digital.</span><span class="sxs-lookup"><span data-stu-id="e458d-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="e458d-154">Esos métodos incluyen:</span><span class="sxs-lookup"><span data-stu-id="e458d-154">These methods include:</span></span>

-   <span data-ttu-id="e458d-155">**AllocateStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="e458d-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="e458d-156">**Discontinuidad**</span><span class="sxs-lookup"><span data-stu-id="e458d-156">**Discontinuity**</span></span>
-   <span data-ttu-id="e458d-157">**Vaciar**</span><span class="sxs-lookup"><span data-stu-id="e458d-157">**Flush**</span></span>
-   <span data-ttu-id="e458d-158">**FreeStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="e458d-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="e458d-159">**Bloquear**</span><span class="sxs-lookup"><span data-stu-id="e458d-159">**Lock**</span></span>
-   <span data-ttu-id="e458d-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="e458d-160">**ProcessInput**</span></span>
-   <span data-ttu-id="e458d-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="e458d-161">**ProcessOutput**</span></span>

<span data-ttu-id="e458d-162">Windows Media Player llama a **AllocateStreamingResources** y **FreeStreamingResources** para proporcionar al complemento DSP la oportunidad de configurar o liberar los búferes adicionales que el complemento pueda necesitar para el procesamiento interno.</span><span class="sxs-lookup"><span data-stu-id="e458d-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="e458d-163">Los complementos DSP de Windows Media Player no necesitan usar el método de **discontinuidad** de DMO.</span><span class="sxs-lookup"><span data-stu-id="e458d-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="e458d-164">Windows Media Player llama a **Flush** para dirigir el complemento DSP para vaciar todos los datos almacenados en el búfer interno.</span><span class="sxs-lookup"><span data-stu-id="e458d-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="e458d-165">El complemento debe liberar todas las referencias a las interfaces de **IMediaBuffer** , borrar cualquier valor que especifique la marca de tiempo o la longitud de muestra para el búfer multimedia, y reinicializar los Estados internos que dependen del contenido del ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="e458d-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="e458d-166">Windows Media Player llama a ProcessInput para pasar un puntero a una interfaz **IMediaBuffer** al complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="e458d-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="e458d-167">Esta interfaz proporciona acceso al búfer de entrada asignado por Windows Media Player para proporcionar datos al complemento.</span><span class="sxs-lookup"><span data-stu-id="e458d-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="e458d-168">Windows Media Player llama posteriormente a **ProcessOutput** para pasar un puntero a una interfaz **IMediaBuffer** que proporciona acceso al búfer de salida asignado por Windows Media Player para recibir los datos procesados del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="e458d-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="e458d-169">La interfaz **IMediaObject** incluye un método denominado **Lock**.</span><span class="sxs-lookup"><span data-stu-id="e458d-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="e458d-170">Este método está diseñado para adquirir o liberar un bloqueo en DMO con el fin de mantener la serialización de DMO al realizar varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="e458d-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="e458d-171">La versión de **IMediaObject:: Lock** en el código del asistente invalida la implementación ATL de **Lock**.</span><span class="sxs-lookup"><span data-stu-id="e458d-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="e458d-172">Dado que Windows Media Player serializa las llamadas realizadas a la interfaz DMO de un complemento DSP, la implementación de **Lock** simplemente devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e458d-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="e458d-173">Para obtener más información sobre cómo crear un DMO multiproceso, consulte la sección de DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e458d-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e458d-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e458d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e458d-175">**Interfaces necesarias**</span><span class="sxs-lookup"><span data-stu-id="e458d-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




