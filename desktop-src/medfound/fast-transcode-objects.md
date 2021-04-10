---
description: En este tema se describe cómo usar la API de Transcode para codificar un archivo multimedia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso de la API de Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153631"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="a3640-103">Uso de la API de Transcode</span><span class="sxs-lookup"><span data-stu-id="a3640-103">Using the Transcode API</span></span>

<span data-ttu-id="a3640-104">En este tema se describe cómo usar la API de Transcode para codificar un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3640-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="a3640-105">Información general</span><span class="sxs-lookup"><span data-stu-id="a3640-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="a3640-106">Crear un origen de medios</span><span class="sxs-lookup"><span data-stu-id="a3640-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="a3640-107">Creación de un perfil de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a3640-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="a3640-108">Atributos de audio</span><span class="sxs-lookup"><span data-stu-id="a3640-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="a3640-109">Atributos de vídeo</span><span class="sxs-lookup"><span data-stu-id="a3640-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="a3640-110">Atributos de contenedor</span><span class="sxs-lookup"><span data-stu-id="a3640-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="a3640-111">Creación de una topología de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a3640-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="a3640-112">Ejecutar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="a3640-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="a3640-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3640-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="a3640-114">Información general</span><span class="sxs-lookup"><span data-stu-id="a3640-114">Overview</span></span>

<span data-ttu-id="a3640-115">Antes de usar la API de Transcode, la aplicación debe tener los siguientes datos:</span><span class="sxs-lookup"><span data-stu-id="a3640-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="a3640-116">La ruta de acceso o la dirección URL de un archivo multimedia existente que se volverá a codificar.</span><span class="sxs-lookup"><span data-stu-id="a3640-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="a3640-117">Nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a3640-117">The name of the output file.</span></span>
-   <span data-ttu-id="a3640-118">El tipo de contenedor para el archivo de salida, como MP4 o el formato de streaming avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="a3640-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="a3640-119">Formato de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-119">The encoding format.</span></span> <span data-ttu-id="a3640-120">Esta información incluye los tipos de medios que describen las secuencias de audio y vídeo codificadas.</span><span class="sxs-lookup"><span data-stu-id="a3640-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="a3640-121">Para usar la API de Transcode, una aplicación realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a3640-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="a3640-122">Cree un origen de medios para leer el archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="a3640-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="a3640-123">Cree un perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-123">Create a transcode profile.</span></span> <span data-ttu-id="a3640-124">Agregue atributos que describan la secuencia de audio, el flujo de vídeo y el contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="a3640-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="a3640-125">Use el perfil de transcodificación para crear una topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="a3640-126">(Para obtener más información acerca de las topologías, consulte [acerca de las topologías](about-topologies.md)).</span><span class="sxs-lookup"><span data-stu-id="a3640-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="a3640-127">Establezca la topología en la [sesión de medios](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="a3640-128">Inicie la sesión de medios y espere hasta el evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="a3640-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="a3640-129">En el resto de este tema se describen estos pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="a3640-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="a3640-130">Crear un origen de medios</span><span class="sxs-lookup"><span data-stu-id="a3640-130">Creating a Media Source</span></span>

<span data-ttu-id="a3640-131">Un origen multimedia es un objeto que lee y analiza el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a3640-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="a3640-132">Para crear un origen multimedia, use la [resolución de origen](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="a3640-133">Puede encontrar código de ejemplo en el tema [uso de la resolución de origen](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="a3640-134">Creación de un perfil de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a3640-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="a3640-135">Un *Perfil de transcodificación* describe el formato y la configuración que se usan para codificar el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a3640-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="a3640-136">El perfil de transcodificación contiene tres conjuntos de atributos:</span><span class="sxs-lookup"><span data-stu-id="a3640-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="a3640-137">Atributos de audio: describa el formato de audio de destino y la configuración del codificador de audio.</span><span class="sxs-lookup"><span data-stu-id="a3640-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="a3640-138">Atributos de vídeo: describe el formato de vídeo de destino y la configuración del codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3640-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="a3640-139">Atributos de contenedor: defina el tipo de contenedor de archivos, así como algunos valores de codificación globales.</span><span class="sxs-lookup"><span data-stu-id="a3640-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="a3640-140">Para crear un perfil de transcodificación, llame a la función [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="a3640-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="a3640-141">Esta función devuelve un puntero a la interfaz [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="a3640-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="a3640-142">El objeto de perfil inicial está vacío; no contiene ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="a3640-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="a3640-143">El siguiente paso consiste en agregar los atributos que definen el perfil.</span><span class="sxs-lookup"><span data-stu-id="a3640-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="a3640-144">Atributos de audio</span><span class="sxs-lookup"><span data-stu-id="a3640-144">Audio Attributes</span></span>

<span data-ttu-id="a3640-145">Para agregar atributos para la secuencia de audio, llame a [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="a3640-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="a3640-146">Estos atributos especifican cómo se codifica la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="a3640-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="a3640-147">Si el archivo de salida no va a contener una secuencia de audio, omita estos atributos.</span><span class="sxs-lookup"><span data-stu-id="a3640-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="a3640-148">Los atributos de audio se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="a3640-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="a3640-149">Atributos que especifican el formato de la secuencia codificada</span><span class="sxs-lookup"><span data-stu-id="a3640-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="a3640-150">Atributos que especifican otros parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="a3640-151">Los atributos de formato son simplemente atributos de tipo de medio, como se describe en la sección [tipos de medios de audio](audio-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="a3640-152">El conjunto exacto de atributos de formato depende del codificador.</span><span class="sxs-lookup"><span data-stu-id="a3640-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="a3640-153">(Consulte [formatos de medios compatibles en Media Foundation](supported-media-formats-in-media-foundation.md)). Esta es una lista de los atributos de formato de audio típicos:</span><span class="sxs-lookup"><span data-stu-id="a3640-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="a3640-154">Atributo de formato</span><span class="sxs-lookup"><span data-stu-id="a3640-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="a3640-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3640-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a3640-156">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="a3640-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="a3640-157">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="a3640-157">The subtype.</span></span> <span data-ttu-id="a3640-158">Vea [GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="a3640-159">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a3640-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="a3640-160">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="a3640-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="a3640-161">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="a3640-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="a3640-162">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="a3640-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="a3640-163">\_alineación del \_ bloque de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a3640-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="a3640-164">La alineación del bloque.</span><span class="sxs-lookup"><span data-stu-id="a3640-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="a3640-165">\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="a3640-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="a3640-166">Número promedio de bytes por segundo (velocidad de bits codificada).</span><span class="sxs-lookup"><span data-stu-id="a3640-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="a3640-167">Se definen los siguientes parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="a3640-168">Parámetro Encoding</span><span class="sxs-lookup"><span data-stu-id="a3640-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="a3640-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3640-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a3640-170">MF \_ Transcode \_ donot \_ Insertar \_ codificador</span><span class="sxs-lookup"><span data-stu-id="a3640-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="a3640-171">Impide que la API de Transcode Inserte un codificador para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="a3640-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="a3640-172">\_ENCODINGPROFILE de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="a3640-173">Especifica la plantilla de conformidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3640-173">Specifies the device conformance template.</span></span> <span data-ttu-id="a3640-174">(Sólo se aplica a archivos ASF).</span><span class="sxs-lookup"><span data-stu-id="a3640-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="a3640-175">\_QUALITYVSSPEED de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="a3640-176">Especifica el equilibrio entre la calidad y la velocidad de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="a3640-177">Debe establecer los atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="a3640-177">You must set the format attributes.</span></span> <span data-ttu-id="a3640-178">Los parámetros de codificación son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a3640-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="a3640-179">Una manera de buscar un formato que sea compatible con el codificador es llamar a la función [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="a3640-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="a3640-180">El codificador deseado se especifica mediante el subtipo.</span><span class="sxs-lookup"><span data-stu-id="a3640-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="a3640-181">La función devuelve una colección de tipos de medios para ese codificador.</span><span class="sxs-lookup"><span data-stu-id="a3640-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="a3640-182">Puede seleccionar un tipo de la lista y copiar los atributos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a3640-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="a3640-183">Para ver un ejemplo de código que usa este enfoque, vea [Tutorial: codificar un archivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="a3640-184">Atributos de vídeo</span><span class="sxs-lookup"><span data-stu-id="a3640-184">Video Attributes</span></span>

<span data-ttu-id="a3640-185">Para agregar atributos para la secuencia de vídeo, llame a [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="a3640-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="a3640-186">Estos atributos especifican cómo se codifica el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3640-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="a3640-187">Si el archivo de salida no va a contener una secuencia de vídeo, omita estos atributos.</span><span class="sxs-lookup"><span data-stu-id="a3640-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="a3640-188">Al igual que con los atributos de audio, los atributos de vídeo se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="a3640-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="a3640-189">Atributos que especifican el formato de la secuencia codificada</span><span class="sxs-lookup"><span data-stu-id="a3640-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="a3640-190">Atributos que especifican otros parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="a3640-191">Los atributos de formato son atributos de tipo de medio, como se describe en la sección [tipos de medios de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="a3640-192">Esta es una lista de los atributos de formato de vídeo típicos:</span><span class="sxs-lookup"><span data-stu-id="a3640-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="a3640-193">Atributo de formato</span><span class="sxs-lookup"><span data-stu-id="a3640-193">Format Attribute</span></span>                                                       | <span data-ttu-id="a3640-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3640-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a3640-195">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="a3640-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="a3640-196">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="a3640-196">The subtype.</span></span> <span data-ttu-id="a3640-197">Vea [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="a3640-198">\_velocidad de \_ fotogramas MF MT \_</span><span class="sxs-lookup"><span data-stu-id="a3640-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="a3640-199">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a3640-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="a3640-200">\_tamaño de \_ marco MF MT \_</span><span class="sxs-lookup"><span data-stu-id="a3640-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="a3640-201">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="a3640-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="a3640-202">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a3640-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="a3640-203">Velocidad de bits media.</span><span class="sxs-lookup"><span data-stu-id="a3640-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="a3640-204">\_relación de \_ aspecto de píxeles MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a3640-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="a3640-205">La relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a3640-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="a3640-206">Se definen los siguientes parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="a3640-207">Parámetro Encoding</span><span class="sxs-lookup"><span data-stu-id="a3640-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="a3640-208">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3640-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a3640-209">MF \_ Transcode \_ donot \_ Insertar \_ codificador</span><span class="sxs-lookup"><span data-stu-id="a3640-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="a3640-210">Impide que la API de Transcode Inserte un codificador para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3640-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="a3640-211">\_ENCODINGPROFILE de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="a3640-212">Especifica la plantilla de conformidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3640-212">Specifies the device conformance template.</span></span> <span data-ttu-id="a3640-213">(Sólo se aplica a archivos ASF).</span><span class="sxs-lookup"><span data-stu-id="a3640-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="a3640-214">\_QUALITYVSSPEED de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="a3640-215">Especifica el equilibrio entre la calidad y la velocidad de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="a3640-216">Debe establecer los atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="a3640-216">You must set the format attributes.</span></span> <span data-ttu-id="a3640-217">Los parámetros de codificación son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a3640-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="a3640-218">Atributos de contenedor</span><span class="sxs-lookup"><span data-stu-id="a3640-218">Container Attributes</span></span>

<span data-ttu-id="a3640-219">Los atributos de contenedor definen las características de nivel de archivo del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a3640-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="a3640-220">Para establecer atributos de contenedor, llame a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="a3640-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="a3640-221">Se definen los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="a3640-221">The following attributes are defined.</span></span>



| <span data-ttu-id="a3640-222">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3640-222">Attribute</span></span>                                                                          | <span data-ttu-id="a3640-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3640-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3640-224">\_Perfil de ajuste de TRANScodificación de MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="a3640-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="a3640-225">Define la configuración de la secuencia que se va a utilizar para la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="a3640-226">Puede establecer las marcas para usar la configuración de origen de entrada o usar atributos de secuencia personalizados.</span><span class="sxs-lookup"><span data-stu-id="a3640-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="a3640-227">\_CONTAINERTYPE de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="a3640-228">Especifica el formato de archivo del archivo de salida, como MP4 o ASF.</span><span class="sxs-lookup"><span data-stu-id="a3640-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="a3640-229">En función de este valor, se agrega el receptor de medios adecuado a la topología.</span><span class="sxs-lookup"><span data-stu-id="a3640-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="a3640-230">\_REcodificar \_ omitir \_ transferencia de metadatos \_</span><span class="sxs-lookup"><span data-stu-id="a3640-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="a3640-231">Especifica si los metadatos del origen se copian en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a3640-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="a3640-232">\_TOPOLOGYMODE de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="a3640-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="a3640-233">Especifica si los códecs basados en hardware se pueden usar durante la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="a3640-234">\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_</span><span class="sxs-lookup"><span data-stu-id="a3640-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="a3640-235">Desbloquea un códec que tiene restricciones de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="a3640-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="a3640-236">Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a3640-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="a3640-237">El atributo [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3640-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="a3640-238">Los demás atributos de contenedor son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a3640-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="a3640-239">Creación de una topología de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a3640-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="a3640-240">La topología de transcodificación es una topología parcial que contiene el origen de medios, los códecs adecuados y el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="a3640-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="a3640-241">Para crear la topología de transcodificación, llame a la función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) .</span><span class="sxs-lookup"><span data-stu-id="a3640-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="a3640-242">Esta función toma los siguientes parámetros como entrada:</span><span class="sxs-lookup"><span data-stu-id="a3640-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="a3640-243">Puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3640-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="a3640-244">Nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a3640-244">The name of the output file.</span></span>
-   <span data-ttu-id="a3640-245">Puntero a la interfaz [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="a3640-246">La función devuelve un puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .</span><span class="sxs-lookup"><span data-stu-id="a3640-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="a3640-247">Ejecutar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="a3640-247">Running the Encoding Session</span></span>

<span data-ttu-id="a3640-248">Después de crear la topología, está listo para codificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="a3640-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="a3640-249">Puede descartar el perfil en este momento.</span><span class="sxs-lookup"><span data-stu-id="a3640-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="a3640-250">Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3640-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="a3640-251">Llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3640-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="a3640-252">Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="a3640-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="a3640-253">Espere el evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="a3640-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="a3640-254">Llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3640-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="a3640-255">Espere el evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="a3640-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="a3640-256">Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="a3640-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="a3640-257">Llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="a3640-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="a3640-258">La mayor parte del tiempo empleado en la codificación se produce entre los pasos 3 y 4.</span><span class="sxs-lookup"><span data-stu-id="a3640-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3640-259">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3640-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3640-260">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a3640-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="a3640-261">Acerca de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="a3640-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



