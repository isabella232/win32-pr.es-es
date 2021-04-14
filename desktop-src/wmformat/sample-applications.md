---
title: Aplicaciones de ejemplo del SDK de Windows Media Format
description: Aplicaciones de ejemplo del SDK de Windows Media Format
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- SDK de Windows Media Format, aplicaciones de ejemplo
- Administración de derechos digitales (DRM), aplicaciones de ejemplo
- DRM (administración de derechos digitales), aplicaciones de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488759"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="1f7a7-106">Aplicaciones de ejemplo del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="1f7a7-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="1f7a7-107">El código de ejemplo proporcionado con este SDK está en forma de proyectos para Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="1f7a7-108">La mayoría de los ejemplos se encuentran en C++, pero ManagedWMFSDKWrapper y ManagedMetadataEdit requieren C#.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="1f7a7-109">Estos ejemplos no funcionarán a menos que se haya instalado el SDK de Windows Media Format o el SDK de Windows Player.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="1f7a7-110">La información de uso de cada ejemplo se encuentra en un archivo readme.txt en cada directorio de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f7a7-111">Samle</span><span class="sxs-lookup"><span data-stu-id="1f7a7-111">Samle</span></span></th>
<th><span data-ttu-id="1f7a7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f7a7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f7a7-113">AudioPlayer</span><span class="sxs-lookup"><span data-stu-id="1f7a7-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="1f7a7-114">Reproduce archivos de Windows Media, incluidos los archivos protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="1f7a7-115">Se controla a través de una GUI y los comandos incluyen reproducir, pausar, buscar y detener.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="1f7a7-116">Puede reproducir archivos o archivos locales leídos de Internet (incluidos los resultados en Internet mediante el ejemplo WMVNetWrite).</span><span class="sxs-lookup"><span data-stu-id="1f7a7-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f7a7-117">Las partes DRM de este ejemplo no se admiten en las versiones basadas en x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-118">DRMHeader</span><span class="sxs-lookup"><span data-stu-id="1f7a7-118">DRMHeader</span></span></td>
<td><span data-ttu-id="1f7a7-119">DRMHeader es una aplicación de consola que usa la interfaz <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> del editor de metadatos para leer atributos DRM de archivos sin vincular a la biblioteca estática de DRM.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f7a7-120">Este ejemplo no se admite en las versiones basadas en x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-121">DRMShow</span><span class="sxs-lookup"><span data-stu-id="1f7a7-121">DRMShow</span></span></td>
<td><span data-ttu-id="1f7a7-122">DRMShow es una aplicación de consola que muestra cómo leer las propiedades <a href="wmformat-glossary.md"><em>DRM</em></a> de un archivo de Windows Media mediante el método <strong>IWMDRMReader:: GetDRMProperty</strong> . En este ejemplo se muestra el uso del método <strong>IWMDRMReader:: GetDRMProperty</strong> y las propiedades que se pueden recuperar del lector DRM.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="1f7a7-123">No muestra cómo adquirir una licencia para contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="1f7a7-124">Este ejemplo requiere la compilación de la biblioteca de rutas de DRM WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f7a7-125">Este ejemplo no se admite en las versiones basadas en x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="1f7a7-126">Al adquirir WMStubDRM. lib de Microsoft, se asigna a la biblioteca un nivel de seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="1f7a7-127">Si el nivel de seguridad de la biblioteca que recibe no es suficiente para reproducir un archivo protegido, este ejemplo mostrará un error.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-128">DirectShowInterop/DSCopy</span><span class="sxs-lookup"><span data-stu-id="1f7a7-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="1f7a7-129">Transcodificar uno o más archivos en un archivo ASF mediante el filtro de escritor ASF de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="1f7a7-130">El archivo de entrada puede ser cualquier formato comprimido o sin comprimir compatible con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-131">DirectShowInterop/DSPlay</span><span class="sxs-lookup"><span data-stu-id="1f7a7-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="1f7a7-132">Este ejemplo es un reproductor de archivos multimedia de audio/vídeo interactivo con compatibilidad con <a href="wmformat-glossary.md"><em>DRM</em></a> .</span><span class="sxs-lookup"><span data-stu-id="1f7a7-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="1f7a7-133">Usa el filtro de lector ASF de WM de DirectShow para reproducir archivos de Windows Media (ASF, WMA, WMV) sin protección DRM y archivos que usan DRM en un nivel de 100 o inferior.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="1f7a7-134">Consulte readme.txt en el directorio del ejemplo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-135">DirectShowInterop/DSSeekFm</span><span class="sxs-lookup"><span data-stu-id="1f7a7-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="1f7a7-136">En este ejemplo se muestra cómo usar el filtro de lector ASF de DirectShow para reproducir el contenido ASF en un gráfico de filtros de DirectShow y también cómo usar la compatibilidad para buscar fotogramas en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-137">Administrados/WMFSDKWrapper</span><span class="sxs-lookup"><span data-stu-id="1f7a7-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="1f7a7-138">Este ensamblado administrado actúa como un contenedor que usan los ejemplos de código administrado para tener acceso a algunas interfaces de metadatos de este SDK.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-139">Administrados/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="1f7a7-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="1f7a7-140">Esta aplicación de C# se puede usar para ver y editar metadatos de archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="1f7a7-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="1f7a7-142">Se trata de una versión de C++ de la aplicación MetadataEdit administrada.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-143">ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="1f7a7-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="1f7a7-144">Este ejemplo de aplicación de consola muestra cómo leer datos de <strong>IStream</strong> con WMReader.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="1f7a7-145">El origen de <strong>IStream</strong> se ha implementado para usar un archivo en el formato de Windows Media (WMA/WMV/ASF).</span><span class="sxs-lookup"><span data-stu-id="1f7a7-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f7a7-146">En este ejemplo no se muestra cómo procesar los ejemplos de medios que salen de WMReader.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="1f7a7-147">Para obtener ejemplos sobre cómo procesar audio y vídeo u otros tipos de muestras multimedia, consulte otros ejemplos, por ejemplo, AudioPlayer, que se incluyen con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-148">UncompAVIToWMV</span><span class="sxs-lookup"><span data-stu-id="1f7a7-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="1f7a7-149">Este ejemplo de aplicación de consola muestra el código necesario para comprimir un archivo AVI en un archivo WMV.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="1f7a7-150">Muestra cómo fusionar mediante combinación ejemplos de secuencias de audio y vídeo de varios archivos AVI y combinarlos en secuencias similares o crear una nueva secuencia basada en el perfil de flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="1f7a7-151">También se muestra cómo crear un flujo arbitrario, realizar una codificación Multipass, agregar código de tiempo SMPTE y aplicar la protección DRM versión 1.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-152">WMGenProfile/exe</span><span class="sxs-lookup"><span data-stu-id="1f7a7-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="1f7a7-153">Este ejemplo se ha actualizado a partir de la versión 7,1.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="1f7a7-154">Ahora es una aplicación de diálogo de MFC.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="1f7a7-155">En el ejemplo WMGenProfile se muestra el uso de la biblioteca estática WMGenProfile.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="1f7a7-156">También sirve como herramienta para la creación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="1f7a7-157">Esta herramienta está diseñada para los desarrolladores familiarizados con el formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="1f7a7-158">La interfaz de usuario no se ha probado para la experiencia del usuario y no está pensada como recomendación sobre cómo presentar esta información a un usuario.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-159">WMGenProfile/lib</span><span class="sxs-lookup"><span data-stu-id="1f7a7-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="1f7a7-160">El ejemplo de biblioteca GenProfile muestra la creación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="1f7a7-161">Muestra cómo crear tipos de medios y secuencias para varios tipos de secuencias (audio, vídeo, script, imagen, transferencia de archivos y Web).</span><span class="sxs-lookup"><span data-stu-id="1f7a7-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="1f7a7-162">No se muestra cómo trabajar con perfiles del sistema o cómo convertir perfiles del sistema en perfiles que especifican los códecs de la serie de Windows Media Audio y vídeo 9.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-163">WMProp</span><span class="sxs-lookup"><span data-stu-id="1f7a7-163">WMProp</span></span></td>
<td><span data-ttu-id="1f7a7-164">Esta aplicación de consola muestra cómo recuperar atributos mediante el objeto de editor de metadatos y la información de perfil del lector.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-165">WMStats</span><span class="sxs-lookup"><span data-stu-id="1f7a7-165">WMStats</span></span></td>
<td><span data-ttu-id="1f7a7-166">Esta aplicación de consola muestra las estadísticas de lector y escritor.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="1f7a7-167">También se pueden usar varias instancias de WMStats simultáneamente en un equipo.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="1f7a7-168">Inicie una instancia como servidor para enviar la secuencia a la red y, a continuación, ejecute una segunda instancia como cliente para comprobar que el servidor se está transmitiendo correctamente.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-169">WMSyncReader</span><span class="sxs-lookup"><span data-stu-id="1f7a7-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="1f7a7-170">Este ejemplo de aplicación de consola muestra cómo leer un archivo multimedia mediante <strong>IWMSyncReader</strong> sin crear ningún subproceso adicional ni usar devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="1f7a7-171">Se han implementado las siguientes características: leer ejemplos comprimidos o descomprimidos</span><span class="sxs-lookup"><span data-stu-id="1f7a7-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="1f7a7-172">Búsqueda basada en el tiempo</span><span class="sxs-lookup"><span data-stu-id="1f7a7-172">Time-based seeking</span></span><br/> <span data-ttu-id="1f7a7-173">Búsqueda basada en marcos</span><span class="sxs-lookup"><span data-stu-id="1f7a7-173">Frame-based seeking</span></span><br/> <span data-ttu-id="1f7a7-174">Origen derivado de <strong>IStream</strong></span><span class="sxs-lookup"><span data-stu-id="1f7a7-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-175">WMVAppend</span><span class="sxs-lookup"><span data-stu-id="1f7a7-175">WMVAppend</span></span></td>
<td><span data-ttu-id="1f7a7-176">Esta aplicación de consola toma dos archivos de Windows Media para la entrada e intenta crear un archivo de salida con el contenido de la primera seguido del segundo.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="1f7a7-177">En el ejemplo se comparan los perfiles de los dos archivos de entrada para asegurarse de que son lo suficientemente similares para ser anexados.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="1f7a7-178">Si no es así, aparece un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="1f7a7-179">Por ejemplo, un mensaje de error se produce cuando un archivo es de solo audio y el segundo es un archivo de audio o vídeo, o cuando dos archivos de audio tienen velocidades de bits diferentes. El ejemplo acepta orígenes de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="1f7a7-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="1f7a7-180">Sin embargo, cuando se comparan los perfiles de los dos orígenes de VBR, el ejemplo omite la diferencia de velocidad de bits media porque dos flujos VBR tendrán velocidades de bits medias diferentes aunque se hayan creado con el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="1f7a7-181">WMVAppend no puede comparar la velocidad de bits máxima de las secuencias VBR basadas en la tasa de bits sin restricciones o el nivel de calidad de las secuencias VBR basadas en la calidad, ya que esta información no existe en los archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="1f7a7-182">Por lo tanto, es responsabilidad del usuario asegurarse de que se crean dos archivos de origen con el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="1f7a7-183">De lo contrario, se puede crear contenido no válido.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-184">WMVCopy</span><span class="sxs-lookup"><span data-stu-id="1f7a7-184">WMVCopy</span></span></td>
<td><span data-ttu-id="1f7a7-185">En este ejemplo se muestra el código necesario para copiar un archivo WMV.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="1f7a7-186">Muestra cómo leer y escribir ejemplos comprimidos, leer atributos y scripts de encabezado y modificar atributos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f7a7-187">WMVNetWrite</span><span class="sxs-lookup"><span data-stu-id="1f7a7-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="1f7a7-188">Esta aplicación de consola muestra cómo se transmite un archivo de Windows Media a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="1f7a7-189">El ejemplo requiere que se especifique un puerto y, a continuación, se puede reproducir el archivo mediante un reproductor.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f7a7-190">WMVRecompress</span><span class="sxs-lookup"><span data-stu-id="1f7a7-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="1f7a7-191">Esta aplicación de consola muestra cómo volver a comprimir un archivo WMV.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="1f7a7-192">Muestra cómo leer ejemplos sin comprimir, escribir ejemplos sin comprimir y realizar la codificación de múltiples pasadas, la salida de varios canales y la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="1f7a7-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1f7a7-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f7a7-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f7a7-194">**Acerca del SDK de Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="1f7a7-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="1f7a7-195">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="1f7a7-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





