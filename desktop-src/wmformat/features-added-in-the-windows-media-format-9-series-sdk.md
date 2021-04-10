---
title: Características agregadas en el SDK de Windows Media Format 9 series
description: Características agregadas en el SDK de Windows Media Format 9 series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, lectores sincrónicos
- Windows Media Format SDK, indexación basada en marcos
- SDK de Windows Media Format, códigos de tiempo SMPTE
- SDK de Windows Media Format, filtros de DirectShow
- SDK de Windows Media Format, funcionalidad de escritura de DRM
- SDK de Windows Media Format, receptores de archivo
- Windows Media Format SDK, DirectX video Acceleration (DXVA)
- SDK de Windows Media Format, audio multicanal
- Windows Media Format SDK, marca de agua
- SDK de Windows Media Format, compatibilidad con varios idiomas
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- SDK de Windows Media Format, enumeraciones de códecs
- SDK de Windows Media Format, exclusión mutua
- Windows Media Format SDK, velocidad de bits múltiple (MBR)
- SDK de Windows Media Format, transcodificación con recompresión inteligente
- SDK de Windows Media Format, recompresión inteligente
- SDK de Windows Media Format, recompresión
- SDK de Windows Media Format, metadatos
- SDK de Windows Media Format, relación de aspecto de píxeles dinámicos
- SDK de Windows Media Format, secuencias de vídeo entrelazadas
- Windows Media Format SDK, codificación de dos pasos
- Windows Media Format SDK, WMStub. lib
- lectores sincrónicos, acerca de
- indexación basada en marcos
- Códigos de tiempo SMPTE, acerca de
- Filtros de DirectShow
- receptores de archivos, mejoras
- audio multicanal, acerca de
- marcas de agua, acerca de
- códecs, enumeraciones
- exclusión mutua, acerca de
- Administración de derechos digitales (DRM), funcionalidad de escritura
- DRM (administración de derechos digitales), funcionalidad de escritura
- Aceleración de vídeo de DirectX (DXVA), acerca de
- DXVA (aceleración de vídeo de DirectX), acerca de
- Advanced Systems Format (ASF), compatibilidad con varios idiomas
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- velocidad de bits múltiple (MBR), acerca de
- MBR (velocidad de varios bits), acerca de
- transcodificación con recompresión inteligente
- recompresión inteligente
- recompresión
- metadatos, SDK de Windows Media Format
- relación de aspecto de píxeles dinámicos
- secuencias de vídeo entrelazadas
- codificación de dos pasos, acerca de
- 2-paso de codificación, acerca de
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268836"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="5c5d1-153">Características agregadas en el SDK de Windows Media Format 9 series</span><span class="sxs-lookup"><span data-stu-id="5c5d1-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="5c5d1-154">El SDK de Windows Media Format 9 series incorporó muchas mejoras y características.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="5c5d1-155">En esta sección se proporciona información general sobre estas características para la ventaja de que los usuarios migran desde una versión anterior del SDK.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="5c5d1-156">Lectura sincrónica</span><span class="sxs-lookup"><span data-stu-id="5c5d1-156">Synchronous Reading</span></span>

<span data-ttu-id="5c5d1-157">Puede leer archivos ASF con llamadas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="5c5d1-158">Al leer un archivo sincrónicamente, puede cambiar la configuración del lector mientras lee.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="5c5d1-159">Las operaciones sincrónicas de lectura del SDK no proporcionan compatibilidad para leer archivos a través de Internet, pero puede usar la interfaz COM estándar, **IStream**, para leer de orígenes personalizados.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="5c5d1-160">Indexación basada en marcos</span><span class="sxs-lookup"><span data-stu-id="5c5d1-160">Frame-based Indexing</span></span>

<span data-ttu-id="5c5d1-161">Puede indexar archivos ASF basados en fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="5c5d1-162">Tanto el lector como el lector sincrónico pueden buscar un fotograma de una secuencia de vídeo y sincronizar el resto de flujos con ese marco.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="5c5d1-163">Indexación y búsqueda con código de tiempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="5c5d1-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="5c5d1-164">El SDK de Windows Media Format permite almacenar códigos de tiempo SMPTE en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="5c5d1-165">Los archivos pueden ser indexados por código de tiempo SMPTE, y el lector asincrónico y el lector sincrónico pueden buscar entradas de índice de código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="5c5d1-166">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="5c5d1-166">DirectShow Filters</span></span>

<span data-ttu-id="5c5d1-167">El SDK de Windows Media Format incluye dos filtros de® de Microsoft DirectShow que permiten a las aplicaciones basadas en DirectShow leer y escribir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="5c5d1-168">DirectShow también permite que las aplicaciones capturen datos de dispositivos de vídeo de audio y descompriman datos de diversos formatos antes de volver a codificarlos como contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="5c5d1-169">Perfiles mejorados</span><span class="sxs-lookup"><span data-stu-id="5c5d1-169">Enhanced Profiles</span></span>

<span data-ttu-id="5c5d1-170">Los perfiles pueden contener información de uso compartido de ancho de banda e información de priorización de secuencias.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="5c5d1-171">El uso compartido de ancho de banda le permite especificar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad de ancho de banda especificada.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="5c5d1-172">El ancho de banda que comparte datos en un perfil es meramente informativo; no se aplica a ninguna lógica del SDK.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="5c5d1-173">La priorización de flujo le permite especificar un orden de prioridad para las secuencias de un perfil.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="5c5d1-174">Si no hay suficiente ancho de banda en la reproducción para transmitir el archivo correctamente, se pueden omitir los flujos de menor prioridad para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="5c5d1-175">Funcionalidad de escritura de DRM</span><span class="sxs-lookup"><span data-stu-id="5c5d1-175">DRM Writing Capability</span></span>

<span data-ttu-id="5c5d1-176">Además de la compatibilidad con la lectura de DRM existente, el SDK de Windows Media Format 9 series agregó compatibilidad para escribir archivos ASF con la protección DRM versión 1 o DRM versión 7.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="5c5d1-177">Esta nueva capacidad permite escenarios de "DRM dinámica", como la difusión por Web de pago por vista de eventos deportivos en directo o conciertos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="5c5d1-178">Receptor de archivos mejorado</span><span class="sxs-lookup"><span data-stu-id="5c5d1-178">Enhanced File Sink</span></span>

<span data-ttu-id="5c5d1-179">Se han agregado varias funcionalidades nuevas del receptor de archivos a la versión 9 de la serie del SDK.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="5c5d1-180">Puede configurar el receptor de archivos para deshabilitar la indexación automática de archivos ASF recién creados.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="5c5d1-181">También tiene la opción de configurarla para la entrada y salida no almacenadas en búfer.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="5c5d1-182">Aceleración de vídeo de DirectX</span><span class="sxs-lookup"><span data-stu-id="5c5d1-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="5c5d1-183">DirectX video Acceleration (DXVA) es una tecnología que permite la reproducción de vídeo de alta velocidad (calidad del DVD o mejor) en máquinas menos eficaces con tarjetas gráficas habilitadas para DXVA.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="5c5d1-184">Puede usar el objeto lector de este SDK para habilitar la aceleración de vídeo de DirectX, si el hardware lo admite, al reproducir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="5c5d1-185">Audio multicanal</span><span class="sxs-lookup"><span data-stu-id="5c5d1-185">Multichannel Audio</span></span>

<span data-ttu-id="5c5d1-186">Puede codificar y reproducir audio multicanal.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="5c5d1-187">El códec Windows Media Audio 9 Professional admite formatos con 6 canales y 8 canales, así como estéreo de alta definición.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="5c5d1-188">Agua</span><span class="sxs-lookup"><span data-stu-id="5c5d1-188">Watermarking</span></span>

<span data-ttu-id="5c5d1-189">Puede codificar archivos ASF con marcas de agua digitales para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="5c5d1-190">Todos los sistemas de marca de agua son diferentes en su enfoque, pero toda la identificación de inserción en el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="5c5d1-191">La marca de agua se realiza mediante el uso de objetos multimedia de DirectX® de terceros (DMOs).</span><span class="sxs-lookup"><span data-stu-id="5c5d1-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="5c5d1-192">Compatibilidad con varios idiomas en archivos ASF</span><span class="sxs-lookup"><span data-stu-id="5c5d1-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="5c5d1-193">Puede admitir varios idiomas en archivos ASF, tanto en secuencias como en metadatos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="5c5d1-194">Por ejemplo, puede crear un archivo de vídeo con secuencias de audio en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="5c5d1-195">En la reproducción, el usuario puede seleccionar el idioma que desea usar o la aplicación puede consultar la información del sistema en el equipo que se está reproduciendo y seleccionar un idioma automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="5c5d1-196">Los atributos de metadatos también se pueden especificar varias veces, con los valores en diferentes lenguajes.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="5c5d1-197">Plantillas de conformidad de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5c5d1-197">Device Conformance Templates</span></span>

<span data-ttu-id="5c5d1-198">Para ayudar a dirigir el contenido a dispositivos cliente específicos, los códecs de Windows Media ahora admiten plantillas de conformidad de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="5c5d1-199">Cada plantilla contiene un intervalo definido de opciones de configuración y códecs que deben usarse para medios destinados a una determinada categoría de plataformas.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="5c5d1-200">Los perfiles del sistema ya no son compatibles con las versiones más recientes de los códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="5c5d1-201">Todos los perfiles deben personalizarse para adaptarse a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="5c5d1-202">Puede usar plantillas de conformidad de dispositivos para ayudarle a diseñar los perfiles.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="5c5d1-203">Enumeración de códec expandida</span><span class="sxs-lookup"><span data-stu-id="5c5d1-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="5c5d1-204">El objeto de administrador de perfiles puede consultar los códecs de Windows Media Audio y vídeo para obtener los formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="5c5d1-205">Puede establecer parámetros para los formatos recuperados.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="5c5d1-206">Por ejemplo, puede recuperar todos los formatos de velocidad de bits variables basados en la calidad admitidos por el códec Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="5c5d1-207">Exclusión mutua mejorada</span><span class="sxs-lookup"><span data-stu-id="5c5d1-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="5c5d1-208">Puede crear registros con nombre que contengan varias secuencias dentro de un objeto de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="5c5d1-209">También puede asignar nombres a los objetos de exclusión mutua para que sean más fáciles de identificar.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="5c5d1-210">Esto le permite crear capas de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="5c5d1-211">Por ejemplo, un archivo puede contener flujos que se excluyen mutuamente por la velocidad de bits y por lenguaje.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="5c5d1-212">La exclusión mutua basada en el lenguaje implicaría grupos de flujos, cada uno de los cuales consta de secuencias en el mismo lenguaje pero que se excluyen mutuamente según la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="5c5d1-213">Compatibilidad ampliada con varias velocidades de bits</span><span class="sxs-lookup"><span data-stu-id="5c5d1-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="5c5d1-214">Se incluye compatibilidad con la exclusión mutua para el audio de velocidad de bits múltiple (MBR) y para vídeo con secuencias de distintos tamaños de imagen.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="5c5d1-215">Atributos para secuencias</span><span class="sxs-lookup"><span data-stu-id="5c5d1-215">Attributes for Streams</span></span>

<span data-ttu-id="5c5d1-216">Puede asignar atributos a flujos individuales en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="5c5d1-217">Todavía debe usar atributos de nivel de archivo para archivos MP3.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="5c5d1-218">Esta característica no agrega ningún método al SDK, pero los métodos existentes aceptarán ahora números de secuencia distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="5c5d1-219">Transcodificación con recompresión inteligente</span><span class="sxs-lookup"><span data-stu-id="5c5d1-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="5c5d1-220">La recompresión inteligente le permite transcodificar archivos de audio de Windows Media de una velocidad de bits alta a una velocidad de bits más baja con una calidad mejor que la que se podía conseguir.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="5c5d1-221">Compatibilidad ampliada con metadatos</span><span class="sxs-lookup"><span data-stu-id="5c5d1-221">Expanded Metadata Support</span></span>

<span data-ttu-id="5c5d1-222">El SDK de Windows Media Format proporciona las siguientes características de metadatos nuevas:</span><span class="sxs-lookup"><span data-stu-id="5c5d1-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="5c5d1-223">Etiquetas de metadatos basadas en índices, que permiten varias etiquetas con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="5c5d1-224">Capacidad de leer atributos de encabezado DRM sin un archivo WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="5c5d1-225">Atributos con más de 64 kilobytes de datos asociados.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="5c5d1-226">Atributos en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="5c5d1-227">Docenas de nuevos atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="5c5d1-228">Relación de aspecto de píxeles dinámicos</span><span class="sxs-lookup"><span data-stu-id="5c5d1-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="5c5d1-229">Las secuencias de vídeo que se componen de varios tipos de contenido se pueden acomodar mediante la identificación de la relación de aspecto de píxeles de las muestras dispares del flujo.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="5c5d1-230">Esto permite que la aplicación de reproducción proporcione una mejor reproducción de dicho contenido.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="5c5d1-231">Secuencias de vídeo entrelazadas</span><span class="sxs-lookup"><span data-stu-id="5c5d1-231">Interlaced Video Streams</span></span>

<span data-ttu-id="5c5d1-232">Las versiones anteriores del SDK de Windows Media Format proporcionan la capacidad de codificar contenido [*entrelazado*](wmformat-glossary.md) en una secuencia de vídeo de recorrido progresivo.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="5c5d1-233">A partir del SDK de Windows Media Format 9 series, puede codificar vídeo entrelazado a la vez que conserva su formato entrelazado.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="5c5d1-234">Esto puede dar lugar a una reproducción mejorada, especialmente en dispositivos entrelazados, como los conjuntos de televisión.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="5c5d1-235">Codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="5c5d1-235">Two-Pass Encoding</span></span>

<span data-ttu-id="5c5d1-236">Los nuevos códecs de Windows Media permiten la codificación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="5c5d1-237">El contenido codificado en dos pasos puede lograr una salida de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="5c5d1-238">Nuevo códec de voz</span><span class="sxs-lookup"><span data-stu-id="5c5d1-238">New Speech Codec</span></span>

<span data-ttu-id="5c5d1-239">Este SDK incluye el nuevo códec de voz de Windows Media Audio 9, que está optimizado para codificar la voz humana mientras usa una velocidad de bits baja.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="5c5d1-240">Este códec también proporciona un rendimiento superior para el contenido de voz de música mixta.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="5c5d1-241">Duración del fotograma de vídeo accesible</span><span class="sxs-lookup"><span data-stu-id="5c5d1-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="5c5d1-242">Puede hacer que el objeto escritor de este SDK proporcione la duración de los fotogramas de vídeo al lector.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="5c5d1-243">Transmisión por secuencias de HTML</span><span class="sxs-lookup"><span data-stu-id="5c5d1-243">Streaming HTML</span></span>

<span data-ttu-id="5c5d1-244">Con la versión anterior de este SDK, podía usar un comando de script para indicar a la aplicación que abrira una página web.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="5c5d1-245">A partir del SDK de Windows Media Format 9 series, puede almacenar los componentes de las páginas web en los archivos ASF para asegurarse de que no haya ningún retraso en las presentaciones.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="5c5d1-246">WMStub. lib ya no es necesario para el entorno de compilación</span><span class="sxs-lookup"><span data-stu-id="5c5d1-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="5c5d1-247">La configuración del entorno de compilación del SDK de Windows Media Format ha cambiado a partir del SDK de Windows Media Format 9 series.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="5c5d1-248">Ya no es necesario incluir WMStub. lib para las aplicaciones que usan este SDK.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="5c5d1-249">Sin embargo, las aplicaciones habilitadas para DRM todavía deben obtener y firmar un contrato de licencia independiente y obtener una biblioteca estática única de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="5c5d1-250">Póngase en contacto con wmla@microsoft.com para obtener más información sobre la biblioteca DRM y el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="5c5d1-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="5c5d1-251">Para obtener más información sobre cómo compilar proyectos con este SDK, vea [archivos de biblioteca y configuración del compilador](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5c5d1-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c5d1-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c5d1-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c5d1-253">**Acerca del SDK de Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="5c5d1-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




