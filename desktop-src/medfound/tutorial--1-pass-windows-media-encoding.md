---
description: La codificación hace referencia al proceso de convertir archivos multimedia digitales de un formato a otro. Por ejemplo, la conversión de audio MP3 en formato Windows Media Audio tal y como se define en la especificación Advanced Systems Format (ASF).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: 1-pasar la codificación de Windows Media'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820303"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="6071d-104">Tutorial: 1-pasar la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6071d-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="6071d-105">La codificación hace referencia al proceso de convertir archivos multimedia digitales de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="6071d-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="6071d-106">Por ejemplo, la conversión de audio MP3 en formato Windows Media Audio tal y como se define en la especificación Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="6071d-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="6071d-107">**Nota:**  La especificación ASF define un tipo de contenedor para el archivo de salida (. WMA o. wmv) que puede contener datos multimedia en cualquier formato, comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="6071d-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="6071d-108">Por ejemplo, un contenedor ASF, como un archivo. WMA, puede contener datos multimedia en formato MP3.</span><span class="sxs-lookup"><span data-stu-id="6071d-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="6071d-109">El proceso de codificación convierte el formato real de los datos contenidos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="6071d-110">En este tutorial se muestra cómo codificar el origen de entrada sin cifrar contenido (no protegido por DRM) en el contenido de Windows Media y escribir los datos en un nuevo archivo ASF (. WM \* ) mediante los componentes ASF de capa de canalización.</span><span class="sxs-lookup"><span data-stu-id="6071d-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="6071d-111">Estos componentes se usarán para crear una topología de codificación parcial, que será controlada por una instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="6071d-112">En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida y el modo de codificación como argumentos.</span><span class="sxs-lookup"><span data-stu-id="6071d-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="6071d-113">El archivo de entrada puede tener un formato de medios comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="6071d-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="6071d-114">Los modos de codificación válidos son "CBR" (velocidad de bits constante) o "VBR" (velocidad de bits variable).</span><span class="sxs-lookup"><span data-stu-id="6071d-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="6071d-115">La aplicación crea un origen de medios para representar el origen especificado por el nombre de archivo de entrada y el receptor de archivos ASF para archivar el contenido codificado del archivo de origen en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="6071d-116">Para que el escenario sea sencillo de implementar, el archivo de salida tendrá solo una secuencia de audio y otra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="6071d-117">La aplicación inserta el códec Windows Media Audio 9,1 Professional para la conversión de formato de secuencia de audio y el códec de Windows Media Video 9 para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="6071d-118">En el caso de la codificación de velocidad de bits constante, antes de que se inicie la sesión de codificación, el codificador debe conocer la velocidad de bits de destino que debe lograr.</span><span class="sxs-lookup"><span data-stu-id="6071d-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="6071d-119">En este tutorial, para el modo "CBR", la aplicación usa la velocidad de bits disponible con el primer tipo de medio de salida que se recupera del codificador durante la negociación del tipo de medio como la velocidad de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="6071d-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="6071d-120">En el caso de la codificación de velocidad de bits variable, en este tutorial se muestra la codificación con velocidad de bits variable mediante el establecimiento de un nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="6071d-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="6071d-121">Los flujos de audio se codifican en el nivel de calidad de 98 y las secuencias de vídeo en el nivel de calidad de 95.</span><span class="sxs-lookup"><span data-stu-id="6071d-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="6071d-122">En el procedimiento siguiente se resumen los pasos para codificar el contenido de Windows Media en un contenedor ASF mediante el modo de codificación de 1 paso.</span><span class="sxs-lookup"><span data-stu-id="6071d-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="6071d-123">Cree un origen de medios para el especificado mediante el solucionador de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="6071d-124">Enumerar las secuencias en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="6071d-125">Cree el receptor de medios ASF y agregue receptores de secuencia en función de las secuencias del origen de medios que deban codificarse.</span><span class="sxs-lookup"><span data-stu-id="6071d-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="6071d-126">Configure el receptor de medios con las propiedades de codificación necesarias.</span><span class="sxs-lookup"><span data-stu-id="6071d-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="6071d-127">Cree los codificadores de Windows Media para las secuencias en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6071d-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="6071d-128">Configure los codificadores con las propiedades que se establecen en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="6071d-129">Cree una topología de codificación parcial.</span><span class="sxs-lookup"><span data-stu-id="6071d-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="6071d-130">Cree una instancia de la sesión multimedia y establezca la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="6071d-131">Inicie la sesión de codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="6071d-132">Para la codificación VBR, obtenga los valores de propiedad de codificación del codificador y establézcalo en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="6071d-133">Cierre y cierre la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="6071d-134">Este tutorial contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="6071d-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="6071d-135">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6071d-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="6071d-136">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="6071d-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="6071d-137">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6071d-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="6071d-138">Crear el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="6071d-139">Crear el objeto de perfil ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="6071d-140">Crear un tipo de medio de audio comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="6071d-141">Crear un tipo de medio de vídeo comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="6071d-142">Crear el objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="6071d-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="6071d-143">Crear el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="6071d-144">Compilar la topología de codificación parcial</span><span class="sxs-lookup"><span data-stu-id="6071d-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="6071d-145">Crear el nodo de la topología de origen para el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6071d-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="6071d-146">Crear instancias de los codificadores necesarios y crear los nodos de transformación</span><span class="sxs-lookup"><span data-stu-id="6071d-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="6071d-147">Crear los nodos de topología de salida para el receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="6071d-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="6071d-148">Conexión de los nodos de origen, transformación y receptor</span><span class="sxs-lookup"><span data-stu-id="6071d-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="6071d-149">Controlar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="6071d-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="6071d-150">Actualizar las propiedades de codificación en el receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="6071d-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="6071d-151">Implementar Main</span><span class="sxs-lookup"><span data-stu-id="6071d-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="6071d-152">Probar el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="6071d-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="6071d-153">Códigos de error comunes y sugerencias de depuración</span><span class="sxs-lookup"><span data-stu-id="6071d-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="6071d-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6071d-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="6071d-155">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6071d-155">Prerequisites</span></span>

<span data-ttu-id="6071d-156">En este tutorial se da por hecho lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6071d-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="6071d-157">Está familiarizado con la [estructura de archivos ASF](asf-file-structure.md), los [componentes ASF de la capa de canalización](pipeline-layer-asf-components.md) proporcionados por Media Foundation para trabajar con objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="6071d-158">Estos componentes incluyen los siguientes objetos:</span><span class="sxs-lookup"><span data-stu-id="6071d-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="6071d-159">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="6071d-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="6071d-160">**Nota:**  Si está realizando una transclasificación (convirtiendo un archivo de velocidad de bits superior en un archivo de velocidad de bits inferior sin cambiar los formatos), usará el [origen de medios ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="6071d-161">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6071d-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="6071d-162">Receptores de medios ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="6071d-163">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="6071d-164">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="6071d-165">Está familiarizado con los codificadores de Windows Media y con los distintos tipos de codificación, especialmente la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md) y la [codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="6071d-166">Está familiarizado con las operaciones de MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="6071d-167">En concreto, crear una instancia del codificador y establecer los tipos de entrada y salida en el codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="6071d-168">Está familiarizado con los objetos de topología y con cómo crear una topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="6071d-169">Para obtener más información sobre las topologías y los nodos de topología, consulte [crear topologías](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="6071d-170">Está familiarizado con el modelo de eventos de la [sesión multimedia](media-session.md)y las operaciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="6071d-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="6071d-171">Para obtener más información, consulte [eventos de sesión de medios](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="6071d-172">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="6071d-172">Set up the Project</span></span>

1.  <span data-ttu-id="6071d-173">Incluya los siguientes encabezados en el archivo de código fuente:</span><span class="sxs-lookup"><span data-stu-id="6071d-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="6071d-174">Vínculo a los siguientes archivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="6071d-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="6071d-175">Declare la función [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="6071d-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="6071d-176">Declare la \_ enumeración del modo de codificación para definir los tipos de codificación CBR y VBR.</span><span class="sxs-lookup"><span data-stu-id="6071d-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="6071d-177">Defina una constante para la ventana de búfer de un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="6071d-178">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6071d-178">Create the Media Source</span></span>

<span data-ttu-id="6071d-179">Cree un origen de medios para el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="6071d-179">Create a media source for the input source.</span></span> <span data-ttu-id="6071d-180">Media Foundation proporciona orígenes de medios integrados para varios formatos de medios: MP3, MP4/3GP, AVI/WAVE.</span><span class="sxs-lookup"><span data-stu-id="6071d-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="6071d-181">Para obtener información acerca de los formatos admitidos por Media Foundation, consulte [formatos multimedia compatibles en Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="6071d-182">Para crear el origen multimedia, use la [resolución de origen](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="6071d-183">Este objeto analiza la dirección URL que se especificó para el archivo de código fuente y crea el origen de medios adecuado.</span><span class="sxs-lookup"><span data-stu-id="6071d-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="6071d-184">Realice las siguientes llamadas:</span><span class="sxs-lookup"><span data-stu-id="6071d-184">Make the following calls:</span></span>

-   [<span data-ttu-id="6071d-185">**MFCreateSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="6071d-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="6071d-186">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="6071d-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="6071d-187">Para obtener más información acerca de estas llamadas, vea [usar el solucionador de origen](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="6071d-188">Si el archivo de entrada está en formato ASF y desea convertirlo en un archivo de velocidad de bits diferente sin cambiar los formatos, el Solver de origen crea una instancia del [origen de medios ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="6071d-189">En el ejemplo de código siguiente se muestra una función CreateMediaSource que crea un origen de medios para el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6071d-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="6071d-190">Crear el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-190">Create the ASF File Sink</span></span>

<span data-ttu-id="6071d-191">Cree una instancia del receptor de archivos ASF que archivará los datos multimedia codificados en un archivo ASF al final de la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="6071d-192">En este tutorial, creará un objeto de activación para el receptor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="6071d-193">El receptor de archivos necesita la siguiente información para crear los receptores de secuencias necesarios.</span><span class="sxs-lookup"><span data-stu-id="6071d-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="6071d-194">Secuencias que se van a codificar y escribir en el archivo final.</span><span class="sxs-lookup"><span data-stu-id="6071d-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="6071d-195">Propiedades de codificación que se usan para codificar el contenido multimedia, como, el tipo de codificación, el número de pasos de codificación y las propiedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6071d-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="6071d-196">Las propiedades globales del archivo que indican al receptor de medios si deben ajustar los parámetros del depósito de fugas (velocidad de bits y tamaño de búfer) automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6071d-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="6071d-197">La información de la secuencia se configura en el objeto de perfil ASF y la codificación y las propiedades globales se establecen en un almacén de propiedades administrado por el objeto ContentInfo ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="6071d-198">Para obtener información general sobre el receptor de archivos ASF, consulte [ASF media Sink](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="6071d-199">Crear el objeto de perfil ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="6071d-200">Para que el receptor de archivos ASF escriba datos multimedia codificados en un archivo ASF, el receptor debe conocer el número de flujos y el tipo de secuencias para las que se van a crear receptores de secuencias.</span><span class="sxs-lookup"><span data-stu-id="6071d-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="6071d-201">En este tutorial, extraerá esa información del origen de medios y creará los flujos de salida correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6071d-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="6071d-202">Restrinja los flujos de salida a una secuencia de audio y una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="6071d-203">Para cada flujo seleccionado en el origen, cree una secuencia de destino y agréguela al perfil.</span><span class="sxs-lookup"><span data-stu-id="6071d-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="6071d-204">Para implementar este paso, necesita los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="6071d-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="6071d-205">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="6071d-206">Descriptor de presentación para el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6071d-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="6071d-207">Descriptores de secuencia para las secuencias seleccionadas en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="6071d-208">Tipos de medios de las secuencias seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="6071d-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="6071d-209">En los pasos siguientes se describe el proceso de creación del perfil ASF y las secuencias de destino.</span><span class="sxs-lookup"><span data-stu-id="6071d-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="6071d-210">**Para crear el perfil ASF**</span><span class="sxs-lookup"><span data-stu-id="6071d-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="6071d-211">Llame a [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para crear un objeto de perfil vacío.</span><span class="sxs-lookup"><span data-stu-id="6071d-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="6071d-212">Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para crear el descriptor de presentación para el origen de medios creado en el paso descrito en la sección "crear el origen multimedia" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="6071d-213">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obtener el número de flujos en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="6071d-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="6071d-214">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para cada flujo en el origen multimedia y obtenga el descriptor de flujo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="6071d-215">Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguido de [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) y obtenga el primer tipo de medio para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="6071d-216">**Nota:**   Para evitar llamadas complejas, supongamos que solo existe un tipo de medio por secuencia y selecciona el primer tipo de medio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="6071d-217">En el caso de las secuencias complejas, debe enumerar cada tipo de medio desde el controlador de tipo de medio y elegir el tipo de medio que desea codificar.</span><span class="sxs-lookup"><span data-stu-id="6071d-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="6071d-218">Llame a I [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) para obtener el tipo principal de la secuencia con el fin de determinar si la secuencia contiene audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="6071d-219">En función del tipo principal de la secuencia, cree tipos de medios de destino.</span><span class="sxs-lookup"><span data-stu-id="6071d-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="6071d-220">Estos tipos de medios contendrán la información de formato que el codificador usará durante la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="6071d-221">En las siguientes secciones de este tutorial se describe el proceso de creación de los tipos de medios de destino.</span><span class="sxs-lookup"><span data-stu-id="6071d-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="6071d-222">Crear un tipo de medio de audio comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="6071d-223">Crear un tipo de medio de vídeo comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="6071d-224">Cree una secuencia basada en el tipo de medio de destino, configure la secuencia según los requisitos de la aplicación y agregue la secuencia al perfil.</span><span class="sxs-lookup"><span data-stu-id="6071d-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="6071d-225">Para obtener más información, consulte [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="6071d-226">Llame a [**IMFASFProfile:: CreateStream (**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) y pase el tipo de medio de destino para crear el flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="6071d-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="6071d-227">El método recupera la interfaz IMFASFStreamConfig del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="6071d-228">Configure el flujo.</span><span class="sxs-lookup"><span data-stu-id="6071d-228">Configure the stream.</span></span>
        -   <span data-ttu-id="6071d-229">Llame a [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para asignar un número a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="6071d-230">Esta configuración es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="6071d-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="6071d-231">Opcionalmente, puede configurar los parámetros de depósito de fugas, la extensión de carga, la exclusión mutua en cada flujo llamando a métodos de [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) y atributos de configuración de secuencia pertinentes.</span><span class="sxs-lookup"><span data-stu-id="6071d-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="6071d-232">Agregue las propiedades de codificación de nivel de secuencia mediante el objeto ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="6071d-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="6071d-233">Para obtener más información acerca de este paso, consulte la sección "crear el objeto ASF ContentInfo" en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="6071d-234">Llame a [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar la secuencia al perfil.</span><span class="sxs-lookup"><span data-stu-id="6071d-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="6071d-235">En el ejemplo de código siguiente se crea una secuencia de audio de salida.</span><span class="sxs-lookup"><span data-stu-id="6071d-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="6071d-236">En el ejemplo de código siguiente se crea una secuencia de vídeo de salida.</span><span class="sxs-lookup"><span data-stu-id="6071d-236">The following code example creates an output video stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

<span data-ttu-id="6071d-237">En el ejemplo de código siguiente se crean flujos de salida en función de las secuencias del origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="6071d-238">Crear un tipo de medio de audio comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="6071d-239">Si desea incluir una secuencia de audio en el archivo de salida, cree un tipo de audio especificando las características del tipo codificado mediante el establecimiento de los atributos necesarios.</span><span class="sxs-lookup"><span data-stu-id="6071d-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="6071d-240">Para asegurarse de que el tipo de audio es compatible con el codificador de audio de Windows Media, cree una instancia de la MFT del codificador, establezca las propiedades de codificación y obtenga un tipo de medio mediante una llamada a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="6071d-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="6071d-241">Obtenga el tipo de salida necesario recorriendo en bucle todos los tipos disponibles, obteniendo los atributos de cada tipo de medio y seleccionando el tipo más próximo a sus requisitos.</span><span class="sxs-lookup"><span data-stu-id="6071d-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="6071d-242">En este tutorial, obtenga el primer tipo disponible de la lista de tipos de medios de salida admitidos por el codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="6071d-243">**Nota:**  En Windows 7, Media Foundation proporciona una nueva función, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) que recupera una lista de los tipos de audio compatibles.</span><span class="sxs-lookup"><span data-stu-id="6071d-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="6071d-244">Esta función solo obtiene los tipos de medios para la codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="6071d-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="6071d-245">Un tipo de audio completo debe tener establecidos los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="6071d-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="6071d-246">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="6071d-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="6071d-247">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="6071d-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="6071d-248">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6071d-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="6071d-249">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="6071d-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="6071d-250">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6071d-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="6071d-251">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="6071d-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="6071d-252">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="6071d-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="6071d-253">En el ejemplo de código siguiente se crea un tipo de audio comprimido obteniendo un tipo compatible del codificador Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="6071d-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="6071d-254">La implementación de SetEncodingProperties se muestra en la sección "crear el objeto ContentInfo de ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="6071d-255">Crear un tipo de medio de vídeo comprimido</span><span class="sxs-lookup"><span data-stu-id="6071d-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="6071d-256">Si desea incluir una secuencia de vídeo en el archivo de salida, cree un tipo de vídeo codificado completo.</span><span class="sxs-lookup"><span data-stu-id="6071d-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="6071d-257">El tipo de medio completo debe incluir la velocidad de bits deseada y los datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="6071d-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="6071d-258">Hay dos maneras de crear un tipo de medio de vídeo completo.</span><span class="sxs-lookup"><span data-stu-id="6071d-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="6071d-259">Cree un tipo de medio vacío y copie los atributos de tipo de medio del tipo de vídeo de origen y sobrescriba el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) con la constante GUID MFVideoFormat \_ WMV3.</span><span class="sxs-lookup"><span data-stu-id="6071d-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="6071d-260">Un tipo de vídeo completo debe tener establecidos los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="6071d-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="6071d-261">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="6071d-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="6071d-262">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="6071d-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="6071d-263">\_velocidad de \_ fotogramas MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6071d-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="6071d-264">\_tamaño de \_ marco MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6071d-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="6071d-265">\_ \_ modo entrelazado MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6071d-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="6071d-266">\_relación de \_ aspecto de píxeles MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6071d-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="6071d-267">\_velocidad de \_ bits media MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6071d-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="6071d-268">datos de usuario de MF \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6071d-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="6071d-269">En el ejemplo de código siguiente se crea un tipo de vídeo comprimido a partir del tipo de vídeo del origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="6071d-270">Para obtener un tipo de medio compatible desde el codificador de vídeo de Windows Media, establezca las propiedades de codificación y, a continuación, llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="6071d-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="6071d-271">Este método devuelve el tipo parcial.</span><span class="sxs-lookup"><span data-stu-id="6071d-271">This method returns the partial type.</span></span> <span data-ttu-id="6071d-272">Asegúrese de convertir el tipo parcial en un tipo completo agregando la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="6071d-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="6071d-273">Establezca la velocidad de bits de vídeo en el atributo [**MF \_ MT \_ AVG de \_ velocidad**](mf-mt-avg-bitrate-attribute.md) de bits.</span><span class="sxs-lookup"><span data-stu-id="6071d-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="6071d-274">Agregue los datos privados del códec mediante el establecimiento del atributo de [**\_ datos del \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6071d-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="6071d-275">Para obtener instrucciones detalladas, vea "datos de códecs privados" en [configuración de un codificador WMV](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="6071d-276">Dado que [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) comprueba la velocidad de bits antes de devolver los datos privados del códec, asegúrese de establecer la velocidad de bits antes de obtener los datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="6071d-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="6071d-277">En el ejemplo de código siguiente se crea un tipo de vídeo comprimido obteniendo un tipo compatible del codificador Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="6071d-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="6071d-278">También crea un tipo de vídeo sin comprimir y lo establece como la entrada del codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="6071d-279">Esto se implementa en la función auxiliar CreateUncompressedVideoType.</span><span class="sxs-lookup"><span data-stu-id="6071d-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="6071d-280">GetOutputTypeFromWMVEncoder convierte el tipo parcial devuelto en un tipo completo agregando datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="6071d-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="6071d-281">La implementación de SetEncodingProperties se muestra en la sección "crear el objeto ContentInfo de ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="6071d-282">En el ejemplo de código siguiente se crea un tipo de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="6071d-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="6071d-283">En el ejemplo de código siguiente se agregan datos privados del códec al tipo de medio de vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="6071d-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="6071d-284">Crear el objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="6071d-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="6071d-285">El objeto ASF ContentInfo es un componente de nivel de WMContainer que está diseñado principalmente para almacenar información del objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="6071d-286">El receptor de archivos ASF, implementa el objeto ContentInfo para almacenar información (en un almacén de propiedades) que se utilizará para escribir el objeto de encabezado ASF del archivo codificado.</span><span class="sxs-lookup"><span data-stu-id="6071d-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="6071d-287">Para ello, debe crear y configurar el siguiente conjunto de información en el objeto ContentInfo antes de iniciar la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="6071d-288">Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="6071d-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="6071d-289">En el ejemplo de código siguiente se crea un objeto ContentInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="6071d-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="6071d-290">Llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener el almacén de propiedades de nivel de flujo del receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="6071d-291">En esta llamada, debe pasar el número de secuencia que asignó para la secuencia al crear el perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="6071d-292">Establezca las [propiedades de codificación](configuring-the-encoder.md) de nivel de secuencia en el almacén de propiedades de flujo del receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="6071d-293">Para obtener más información, vea "propiedades de codificación de secuencias" en [configuración de las propiedades del receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="6071d-294">En el ejemplo de código siguiente se establecen las propiedades de nivel de flujo en el almacén de propiedades del receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="6071d-295">En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="6071d-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="6071d-296">Esta función establece las propiedades de codificación de nivel de secuencia para CBR y VBR.</span><span class="sxs-lookup"><span data-stu-id="6071d-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

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

    

4.  <span data-ttu-id="6071d-297">Llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener el almacén de propiedades global del receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="6071d-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="6071d-298">En esta llamada, debe pasar 0 en el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="6071d-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="6071d-299">Para obtener más información, vea "propiedades del receptor de archivos globales" en [configuración de las propiedades del receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="6071d-300">Establezca la [**\_ velocidad de \_ \_ bits de autoajuste de MFPKEY ASFMEDIASINK**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) en Variant \_ true para asegurarse de que los valores del cubo con fugas del multiplexor ASF se ajustan correctamente.</span><span class="sxs-lookup"><span data-stu-id="6071d-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="6071d-301">Para obtener información sobre esta propiedad, vea "configuración de la inicialización del multiplexor y del cubo de fugas" en [crear el objeto multiplexor](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="6071d-302">En el ejemplo de código siguiente se establecen las propiedades de nivel de flujo en el almacén de propiedades del receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="6071d-303">Hay otras propiedades que puede establecer en el nivel global del receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="6071d-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="6071d-304">Para obtener más información, vea "configurar el objeto ContentInfo con la configuración del codificador" en [establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="6071d-305">Usará el ContentInfo ASF configurado para crear un objeto de activación para el receptor de archivos ASF (descrito en la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="6071d-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="6071d-306">Si va a crear un receptor de archivos fuera de proceso ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), es decir, mediante el uso de un objeto de activación, puede usar el objeto ContentInfo configurado para crear una instancia del receptor de medios ASF (descrito en la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="6071d-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="6071d-307">Si va a crear un receptor de archivos en proceso ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), en lugar de crear el objeto ContentInfo vacío como se describe en el paso 1, obtenga una referencia a la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) llamando a **IMFMediaSink:: QueryInterface** en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="6071d-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="6071d-308">A continuación, debe configurar el objeto ContentInfo como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6071d-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="6071d-309">Crear el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="6071d-309">Create the ASF File Sink</span></span>

<span data-ttu-id="6071d-310">En este paso del tutorial, usará el ContentInfo ASF configurado, que creó en el paso anterior, para crear un objeto de activación para el receptor de archivos ASF mediante una llamada a la función [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="6071d-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="6071d-311">Para obtener más información, vea [crear el receptor de archivos ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="6071d-312">En el ejemplo de código siguiente se crea el objeto de activación para el receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="6071d-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="6071d-313">Compilar la topología de codificación parcial</span><span class="sxs-lookup"><span data-stu-id="6071d-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="6071d-314">A continuación, creará una topología de codificación parcial creando nodos de topología para el origen de medios, los codificadores de Windows Media necesarios y el receptor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="6071d-315">Después de agregar los nodos de topología, se conectarán los nodos de origen, transformación y receptor.</span><span class="sxs-lookup"><span data-stu-id="6071d-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="6071d-316">Antes de agregar nodos de topología, debe crear un objeto de topología vacío mediante una llamada a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="6071d-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="6071d-317">Crear el nodo de la topología de origen para el origen de medios</span><span class="sxs-lookup"><span data-stu-id="6071d-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="6071d-318">En este paso, creará el nodo de la topología de origen para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="6071d-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="6071d-319">Para crear este nodo necesita las siguientes referencias:</span><span class="sxs-lookup"><span data-stu-id="6071d-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="6071d-320">Un puntero al origen multimedia que creó en el paso descrito en la sección "crear el origen multimedia" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="6071d-321">Puntero al descriptor de presentación para el origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="6071d-322">Puede obtener una referencia a la interfaz IMFPresentationDescriptor del origen multimedia llamando a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="6071d-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="6071d-323">Un puntero al descriptor de flujo para cada flujo en el origen multimedia para el que se ha creado una secuencia de destino en el paso descrito en la sección "crear el objeto de perfil ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="6071d-324">Para obtener más información sobre cómo crear nodos de origen y ejemplos de código, vea [crear nodos de origen](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="6071d-325">En el ejemplo de código siguiente se crea una topología parcial agregando el nodo de origen y los nodos de transformación necesarios.</span><span class="sxs-lookup"><span data-stu-id="6071d-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="6071d-326">Este código llama a las funciones auxiliares AddSourceNode y AddTransformOutputNodes.</span><span class="sxs-lookup"><span data-stu-id="6071d-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="6071d-327">Estas funciones se incluyen más adelante en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="6071d-328">En el ejemplo de código siguiente se crea y agrega el nodo de la topología de origen a la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="6071d-329">Toma punteros a un objeto de topología anterior, el origen de medios para enumerar los flujos de origen, el descriptor de presentación del origen multimedia y el descriptor de flujo del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="6071d-330">El autor de la llamada recibe un puntero al nodo de la topología de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="6071d-331">Crear instancias de los codificadores necesarios y crear los nodos de transformación</span><span class="sxs-lookup"><span data-stu-id="6071d-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="6071d-332">La canalización de Media Foundation no inserta automáticamente los codificadores de Windows Media necesarios para las secuencias que debe codificar.</span><span class="sxs-lookup"><span data-stu-id="6071d-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="6071d-333">La aplicación debe agregar los codificadores manualmente.</span><span class="sxs-lookup"><span data-stu-id="6071d-333">The application must add the encoders manually.</span></span> <span data-ttu-id="6071d-334">Para ello, enumere las secuencias del perfil ASF que creó en el paso descrito en la sección "crear el objeto de perfil ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="6071d-335">Para cada flujo en el origen y el flujo correspondiente en el perfil, cree instancias de los codificadores necesarios.</span><span class="sxs-lookup"><span data-stu-id="6071d-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="6071d-336">En este paso, necesitará un puntero al objeto de activación para el receptor de archivos que creó en el paso descrito en la sección "crear el receptor de archivos ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="6071d-337">Para obtener información general sobre cómo crear codificadores a través de objetos de activación, consulte [uso de los objetos de activación de un codificador](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="6071d-338">En el procedimiento siguiente se describen los pasos necesarios para crear una instancia de los codificadores necesarios.</span><span class="sxs-lookup"><span data-stu-id="6071d-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="6071d-339">Obtenga una referencia al objeto ContentInfo del receptor llamando a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el receptor de archivo activar y, a continuación, consultando el [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del receptor de archivos llamando a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6071d-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="6071d-340">Obtiene el perfil ASF asociado al objeto ContentInfo llamando a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="6071d-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="6071d-341">Enumerar las secuencias del perfil.</span><span class="sxs-lookup"><span data-stu-id="6071d-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="6071d-342">Para ello, necesitará el recuento de flujos y una referencia a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="6071d-343">Llame a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6071d-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="6071d-344">**IMFASFProfile::GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="6071d-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="6071d-345">**IMFASFProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="6071d-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="6071d-346">Para cada flujo, obtenga el tipo principal y las propiedades de codificación de la secuencia del objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="6071d-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="6071d-347">Llame a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6071d-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="6071d-348">**IMFASFStreamConfig::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="6071d-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="6071d-349">**IMFMediaType::GetMajorType**</span><span class="sxs-lookup"><span data-stu-id="6071d-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="6071d-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="6071d-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="6071d-351">Para esta llamada, necesita el número de secuencia recuperado por la llamada a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .</span><span class="sxs-lookup"><span data-stu-id="6071d-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="6071d-352">Dependiendo del tipo de secuencia, audio o vídeo, cree una instancia del objeto de activación para el codificador mediante una llamada a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span><span class="sxs-lookup"><span data-stu-id="6071d-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="6071d-353">Para llamar a estas funciones, necesita las siguientes referencias:</span><span class="sxs-lookup"><span data-stu-id="6071d-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="6071d-354">Un puntero al tipo de archivo multimedia de la secuencia recuperado por [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="6071d-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="6071d-355">Un puntero al almacén de propiedades de codificación de la secuencia recuperado por [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span><span class="sxs-lookup"><span data-stu-id="6071d-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="6071d-356">Al pasar un puntero al almacén de propiedades, las propiedades de secuencia establecidas en el receptor de archivos se copian en la MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="6071d-357">Actualice el parámetro de depósito de fugas para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="6071d-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="6071d-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) establece el tipo de salida en la MFT del codificador subyacente para el códec de audio de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6071d-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="6071d-359">Una vez que se establece el tipo de medio de salida, el codificador obtiene la velocidad de bits media del tipo de medio de salida, calcula la velocidad de bits de la ventana de búfer y establece los valores del cubo con fugas que se usarán durante la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="6071d-360">Puede actualizar estos valores en el receptor de archivos; para ello, consulte al codificador o establezca los valores personalizados.</span><span class="sxs-lookup"><span data-stu-id="6071d-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="6071d-361">Para actualizar los valores necesita el siguiente conjunto de información:</span><span class="sxs-lookup"><span data-stu-id="6071d-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="6071d-362">Velocidad de bits media: obtiene la velocidad de bits media del atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) establecido en el tipo de medio de salida que se selecciona durante la negociación del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6071d-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="6071d-363">Ventana de búfer: puede recuperarla llamando a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="6071d-364">Tamaño de búfer inicial: establézcalo en 0.</span><span class="sxs-lookup"><span data-stu-id="6071d-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="6071d-365">Cree una matriz de valores DWORD y establezca el valor en la propiedad [**MFPKEY \_ ASFSTREAMSINK \_ corregida \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del receptor de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="6071d-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="6071d-366">Si no proporciona los valores actualizados, la sesión multimedia los establece de manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="6071d-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="6071d-367">Para obtener más información, consulte [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="6071d-368">Los objetos de activación creados en el paso 5 se deben agregar a la topología como nodos de topología de transformación.</span><span class="sxs-lookup"><span data-stu-id="6071d-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="6071d-369">Para obtener más información y ejemplos de código, vea "crear un nodo de transformación desde un objeto de activación" en [crear nodos de transformación](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="6071d-370">En el ejemplo de código siguiente se crea y se agrega la activación del codificador necesaria.</span><span class="sxs-lookup"><span data-stu-id="6071d-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="6071d-371">Toma punteros a un objeto de topología creado previamente, el objeto de activación del receptor de archivos y el tipo de medio del flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="6071d-372">También llama a AddOutputNode (vea el siguiente ejemplo de código) que crea y agrega el nodo de receptor a la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="6071d-373">El autor de la llamada recibe un puntero al nodo de la topología de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="6071d-374">Crear los nodos de topología de salida para el receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="6071d-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="6071d-375">En este paso, creará el nodo de la topología de salida para el receptor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="6071d-376">Para crear este nodo necesita las siguientes referencias:</span><span class="sxs-lookup"><span data-stu-id="6071d-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="6071d-377">Un puntero al objeto de activación que creó en el paso descrito en la sección "crear el receptor de archivos ASF" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="6071d-378">Los números de secuencia para identificar los receptores de flujo agregados al receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="6071d-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="6071d-379">Los números de flujo coinciden con la identificación de la secuencia que se estableció durante la creación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="6071d-380">Para obtener más información sobre cómo crear nodos de salida y ejemplos de código, vea "crear un nodo de salida a partir de un objeto de activación" en [crear nodos de salida](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="6071d-381">Si no usa el objeto de activación para el receptor de archivos, debe enumerar los receptores de flujo en el receptor de archivos ASF y establecer cada receptor de flujo como el nodo de salida en la topología.</span><span class="sxs-lookup"><span data-stu-id="6071d-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="6071d-382">Para obtener información acerca de la enumeración del receptor de secuencias, vea "enumeración de receptores de secuencias" en [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="6071d-383">En el ejemplo de código siguiente se crea y agrega el nodo de receptor a la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="6071d-384">Toma punteros a un objeto de topología creado previamente, el objeto de activación del receptor de archivos y el número de identificación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="6071d-385">El autor de la llamada recibe un puntero al nodo de la topología de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="6071d-386">En el ejemplo de código siguiente se enumeran los receptores de flujo para un receptor multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="6071d-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="6071d-387">Conexión de los nodos de origen, transformación y receptor</span><span class="sxs-lookup"><span data-stu-id="6071d-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="6071d-388">En este paso, conectará el nodo de origen al nodo de transformación que hace referencia a las activaciones de codificación que creó en el paso descrito en la sección "crear instancias de los codificadores necesarios y crear los nodos de transformación" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="6071d-389">El nodo de transformación se conectará al nodo de salida que contiene el objeto de activación del receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="6071d-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="6071d-390">Controlar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="6071d-390">Handling the Encoding Session</span></span>

<span data-ttu-id="6071d-391">En el paso, realizará los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6071d-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="6071d-392">Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear una sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="6071d-393">Llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología de codificación en la sesión.</span><span class="sxs-lookup"><span data-stu-id="6071d-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="6071d-394">Si la llamada se completa, la sesión multimedia evalúa los nodos de la topología e inserta objetos de transformación adicionales, como un descodificador que convierte el origen comprimido especificado en muestras sin comprimir para que se proporcionen como entrada para el codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="6071d-395">Llame a [**IMFMediaSession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) para solicitar los eventos generados por la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="6071d-396">En el bucle de eventos, iniciará y cerrará la sesión de codificación en función de los eventos generados por la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="6071d-397">La llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) genera una sesión multimedia que genera el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con \_ el \_ conjunto de marcas listo TOPOSTATUS Ready.</span><span class="sxs-lookup"><span data-stu-id="6071d-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="6071d-398">Todos los eventos se generan de forma asincrónica y una aplicación puede recuperar estos eventos de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6071d-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="6071d-399">Dado que la aplicación de este tutorial es una aplicación de consola y el bloqueo de subprocesos de interfaz de usuario no es un problema, se obtendrán los eventos de la sesión de medios sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="6071d-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="6071d-400">Para obtener los eventos de forma asincrónica, la aplicación debe implementar la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="6071d-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="6071d-401">Para obtener más información y un ejemplo de implementación de esta interfaz, vea el tema sobre el control de eventos de sesión en [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="6071d-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="6071d-402">En el bucle de eventos para obtener eventos de sesión multimedia, espere a que se produzca el evento [MESessionTopologyStatus](mesessiontopologystatus.md) que se genera cuando se completa [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) y se resuelve la topología.</span><span class="sxs-lookup"><span data-stu-id="6071d-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="6071d-403">Tras obtener el evento MESessionTopologyStatus, inicie la sesión de codificación llamando a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="6071d-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="6071d-404">La sesión multimedia genera el evento [MEEndOfPresentation](meendofpresentation.md) cuando se completan todas las operaciones de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="6071d-405">Este evento debe controlarse para la codificación VBR y se describe en la sección siguiente "actualizar las propiedades de codificación del receptor de archivos para la codificación VBR" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="6071d-406">La sesión multimedia genera el objeto de encabezado ASF y finaliza el archivo cuando se completa la sesión de codificación y, a continuación, genera el evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="6071d-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="6071d-407">Este evento debe controlarse mediante la realización de operaciones de cierre adecuadas en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="6071d-408">Para iniciar las operaciones de apagado, llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="6071d-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="6071d-409">Una vez cerrada la sesión de codificación, no se puede establecer otra topología para la codificación en la misma instancia de sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="6071d-410">Para codificar otro archivo, la sesión multimedia actual debe cerrarse y liberarse y la nueva topología debe establecerse en una sesión multimedia recién creada.</span><span class="sxs-lookup"><span data-stu-id="6071d-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="6071d-411">En el ejemplo de código siguiente se crea la sesión multimedia, se establece la topología de codificación y se controlan los eventos de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="6071d-412">En el ejemplo de código siguiente se crea la sesión multimedia, se establece la topología de codificación y se controla la sesión de codificación controlando los eventos de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6071d-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="6071d-413">Actualizar las propiedades de codificación en el receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="6071d-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="6071d-414">Ciertas propiedades de codificación, como la velocidad de bits de codificación y los valores de depósito de fugas precisos, no se conocen hasta que se completa la codificación, especialmente en el caso de la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="6071d-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="6071d-415">Para obtener los valores correctos, la aplicación debe esperar al evento [MEEndOfPresentation](meendofpresentation.md) que indica que se ha completado la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="6071d-416">Los valores del depósito con fugas se deben actualizar en el receptor para que el objeto de encabezado ASF pueda reflejar los valores precisos.</span><span class="sxs-lookup"><span data-stu-id="6071d-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="6071d-417">En el procedimiento siguiente se describen los pasos necesarios para atravesar los nodos de la topología de codificación para obtener el nodo receptor de archivos y establecer las propiedades de depósito de fugas necesarias.</span><span class="sxs-lookup"><span data-stu-id="6071d-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="6071d-418">**Para actualizar los valores de la propiedad de codificación posterior en el receptor de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="6071d-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="6071d-419">Llame a [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obtener la colección de nodos de salida de la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="6071d-420">Para cada nodo, obtenga un puntero al receptor de la secuencia en el nodo mediante una llamada a [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span><span class="sxs-lookup"><span data-stu-id="6071d-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="6071d-421">Consulte la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) en el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) devuelto por **IMFTopologyNode:: GetObject**.</span><span class="sxs-lookup"><span data-stu-id="6071d-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="6071d-422">Para cada receptor de flujo, obtenga el nodo de nivel inferior (codificador) mediante una llamada a [**IMFTopologyNode:: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span><span class="sxs-lookup"><span data-stu-id="6071d-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="6071d-423">Consulte el nodo para obtener el puntero [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) desde el nodo Encoder.</span><span class="sxs-lookup"><span data-stu-id="6071d-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="6071d-424">Consulte al codificador el puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener el almacén de propiedades de codificación del codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="6071d-425">Consulte el receptor de la secuencia para que el puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) obtenga el almacén de propiedades del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6071d-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="6071d-426">Llame a [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener los valores de propiedad necesarios del almacén de propiedades del codificador y copiarlos en el almacén de propiedades del receptor de flujo llamando a **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="6071d-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="6071d-427">En la tabla siguiente se muestran los valores de propiedad de la codificación post que se deben establecer en el receptor de flujo para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6071d-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="6071d-428">Tipo de codificación</span><span class="sxs-lookup"><span data-stu-id="6071d-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="6071d-429">Nombre de propiedad (GetValue)</span><span class="sxs-lookup"><span data-stu-id="6071d-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="6071d-430">Nombre de propiedad (SetValue)</span><span class="sxs-lookup"><span data-stu-id="6071d-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6071d-431">Codificación de velocidad de bits constante</span><span class="sxs-lookup"><span data-stu-id="6071d-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="6071d-432">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="6071d-433">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="6071d-434">MFPKEY \_ STAT \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="6071d-435">MFPKEY \_ STAT \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="6071d-436">Codificación de velocidad de bits variable basada en la calidad</span><span class="sxs-lookup"><span data-stu-id="6071d-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="6071d-437">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="6071d-438">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="6071d-439">MFPKEY \_ Bmax</span><span class="sxs-lookup"><span data-stu-id="6071d-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="6071d-440">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="6071d-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="6071d-441">MFPKEY \_ STAT \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="6071d-442">MFPKEY \_ STAT \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="6071d-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="6071d-443">MFPKEY \_ STAT \_ Bmax</span><span class="sxs-lookup"><span data-stu-id="6071d-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="6071d-444">MFPKEY \_ STAT \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="6071d-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="6071d-445">En el ejemplo de código siguiente se establecen los valores de las propiedades posteriores a la codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="6071d-446">Implementar Main</span><span class="sxs-lookup"><span data-stu-id="6071d-446">Implement Main</span></span>

<span data-ttu-id="6071d-447">En el ejemplo de código siguiente se muestra la función principal de la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="6071d-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="6071d-448">Probar el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="6071d-448">Test the Output File</span></span>

<span data-ttu-id="6071d-449">En la lista siguiente se describe una lista de comprobación para probar el archivo codificado.</span><span class="sxs-lookup"><span data-stu-id="6071d-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="6071d-450">Estos valores se pueden comprobar en el cuadro de diálogo Propiedades del archivo que puede mostrar haciendo clic con el botón secundario en el archivo codificado y seleccionando **propiedades** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="6071d-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="6071d-451">La ruta de acceso del archivo codificado es precisa.</span><span class="sxs-lookup"><span data-stu-id="6071d-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="6071d-452">El tamaño del archivo es superior a cero KB y la duración de la reproducción coincide con la duración del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="6071d-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="6071d-453">En el flujo de vídeo, compruebe el ancho y el alto del marco, velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6071d-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="6071d-454">Estos valores deben coincidir con los valores especificados en el perfil ASF que creó en el paso descrito en la sección "crear el objeto de perfil ASF".</span><span class="sxs-lookup"><span data-stu-id="6071d-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="6071d-455">En el flujo de audio, la velocidad de bits debe estar cerca del valor especificado en el tipo de medio de destino.</span><span class="sxs-lookup"><span data-stu-id="6071d-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="6071d-456">Abra el archivo en Windows Media Player y Compruebe la calidad de la codificación.</span><span class="sxs-lookup"><span data-stu-id="6071d-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="6071d-457">Abra el archivo ASF en ASFViewer para ver la estructura de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6071d-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="6071d-458">Esta herramienta se puede descargar en este [sitio web de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="6071d-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="6071d-459">Códigos de error comunes y sugerencias de depuración</span><span class="sxs-lookup"><span data-stu-id="6071d-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="6071d-460">En la lista siguiente se describen los códigos de error comunes que puede recibir y las sugerencias de depuración.</span><span class="sxs-lookup"><span data-stu-id="6071d-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="6071d-461">La llamada a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) detiene la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6071d-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="6071d-462">Asegúrese de que ha inicializado la plataforma Media Foundation llamando a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="6071d-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="6071d-463">Esta función configura la plataforma asincrónica que usan todos los métodos que inician operaciones asincrónicas, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internamente.</span><span class="sxs-lookup"><span data-stu-id="6071d-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="6071d-464">[**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) devuelve HRESULT 0X80070002 "el sistema no encuentra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6071d-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="6071d-465">Asegúrese de que el nombre del archivo de entrada especificado por el usuario en el primer argumento existe.</span><span class="sxs-lookup"><span data-stu-id="6071d-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="6071d-466">HRESULT 0x80070020 "el proceso no puede obtener acceso al archivo porque otro proceso lo está usando.</span><span class="sxs-lookup"><span data-stu-id="6071d-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="6071d-467">"</span><span class="sxs-lookup"><span data-stu-id="6071d-467">"</span></span>

    <span data-ttu-id="6071d-468">Asegúrese de que los archivos de entrada y salida no estén siendo utilizados por otro recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="6071d-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="6071d-469">Las llamadas a métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devuelven MF \_ E \_ INVALIDMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="6071d-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="6071d-470">Asegúrese de que se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6071d-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="6071d-471">El tipo de entrada o el tipo de salida que especificó es compatible con los tipos de medios que admite el codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="6071d-472">Los tipos de medios que especificó están completos.</span><span class="sxs-lookup"><span data-stu-id="6071d-472">The media types that you specified are complete.</span></span> <span data-ttu-id="6071d-473">Para completar los tipos de medios, consulte los atributos necesarios en las secciones "crear un tipo de medio de audio comprimido" y "crear un tipo de medio de vídeo comprimido" de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6071d-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="6071d-474">Asegúrese de que ha establecido la velocidad de bits de destino en el tipo de medio parcial al que va a agregar los datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="6071d-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="6071d-475">La sesión multimedia devuelve \_ \_ el tipo D3D no compatible con MF E \_ \_ en el estado del evento.</span><span class="sxs-lookup"><span data-stu-id="6071d-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="6071d-476">Este error se devuelve cuando el tipo de medio del origen indica un modo de entrelazado mixto que no es compatible con el codificador de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="6071d-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="6071d-477">Si el tipo de medio de vídeo comprimido está configurado para usar el modo progresivo, la canalización debe usar una transformación de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="6071d-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="6071d-478">Dado que la canalización no puede encontrar una coincidencia (indicada por este código de error), debe insertar manualmente un descodificador (procesador de vídeo de Transcode) entre los nodos descodificador y codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="6071d-479">La sesión multimedia devuelve E \_ INVALIDARG en el estado del evento.</span><span class="sxs-lookup"><span data-stu-id="6071d-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="6071d-480">Este error se devuelve cuando los atributos de tipo de medio de origen no son compatibles con los atributos del tipo de medio de salida establecido en el codificador de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6071d-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="6071d-481">[**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) devuelve HRESULT 0x80040203 "error de sintaxis al intentar evaluar una cadena de consulta"</span><span class="sxs-lookup"><span data-stu-id="6071d-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="6071d-482">Asegúrese de que el tipo de entrada está establecido en la MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="6071d-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6071d-483">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6071d-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6071d-484">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="6071d-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
