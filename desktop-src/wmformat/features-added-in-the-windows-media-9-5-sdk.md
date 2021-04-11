---
title: Características agregadas en el SDK de Windows Media 9,5
description: Características agregadas en el SDK de Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, interfaz para el procesamiento específico de la aplicación
- Windows Media Format SDK, DirectX video Acceleration (DXVA)
- SDK de Windows Media Format, interfaz IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versiones basadas en x64 de Windows
- Windows Media Format SDK, códec de imagen de Windows Media Video
- Windows Media Format SDK, códecs de audio
- Windows Media Format SDK, DRM 10 para dispositivos de red
- SDK de Windows Media Format, licencias de DRM
- Windows Media Format SDK, códec de perfil avanzado
- Windows Media Format SDK, formato de interconexión digital de Sony/Philips (S/PDIF)
- SDK de Windows Media Format, formatos de retraso bajo
- SDK de Windows Media Format, modo de búsqueda aproximado
- SDK de Windows Media Format, grabación de listas de reproducción
- SDK de Windows Media Format, compatibilidad con varios idiomas
- Windows Media Format SDK, Windows Media Administrador de dispositivos SDK
- SDK de Windows Media Format, interfaces de códec
- códecs, imagen de Windows Media Video
- Administración de derechos digitales (DRM), protocolo de transferencia segura de dispositivos de red
- DRM (administración de derechos digitales), protocolo de transferencia segura de dispositivos de red
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- códecs, códec de perfil avanzado
- Formato de interconexión digital de Sony/Philips (S/PDIF), transferencia o transmisión con
- S/PDIF (formato Sony/Philips digital Interconnect), transferencia o transmisión con
- modo de búsqueda aproximado
- metadatos, compatibilidad con varios idiomas
- SDK de Administrador de dispositivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149104"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="e6eea-133">Características agregadas en el SDK de Windows Media 9,5</span><span class="sxs-lookup"><span data-stu-id="e6eea-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="e6eea-134">El SDK de Windows Media Format 9,5 presentó nuevas características para proporcionar una mayor seguridad y flexibilidad en el contenido.</span><span class="sxs-lookup"><span data-stu-id="e6eea-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="e6eea-135">Se realizaron los siguientes cambios en el SDK desde la versión 9 series.</span><span class="sxs-lookup"><span data-stu-id="e6eea-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="e6eea-136">Nueva interfaz para el procesamiento específico de la aplicación durante la aceleración de vídeo de DirectX</span><span class="sxs-lookup"><span data-stu-id="e6eea-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="e6eea-137">Las aplicaciones de reproductor compatibles con la aceleración de vídeo de DirectX ahora pueden implementar la interfaz [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para realizar el procesamiento específico de la aplicación durante la descodificación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="e6eea-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="e6eea-138">El lector llama al método de devolución de llamada [**IWMPLayerHook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de pasar muestras de vídeo comprimidos al procesador de vídeo para la descodificación.</span><span class="sxs-lookup"><span data-stu-id="e6eea-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="e6eea-139">Para usar la interfaz **IWMPlayerHook** y la interfaz [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) asociada, debe tener instalado el número de actualización 888656 en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e6eea-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="e6eea-140">Puede descargar la actualización desde el [sitio web de Microsoft](https://support.microsoft.com/?id=888656).</span><span class="sxs-lookup"><span data-stu-id="e6eea-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="e6eea-141">Versión del SDK de Windows Media Format para versiones basadas en x64 de Windows</span><span class="sxs-lookup"><span data-stu-id="e6eea-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="e6eea-142">Hay disponible una versión basada en x64 del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e6eea-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="e6eea-143">Esta documentación se aplica tanto a las versiones de 32 bits como a la versión basada en x64 del SDK.</span><span class="sxs-lookup"><span data-stu-id="e6eea-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="e6eea-144">Sin embargo, no se admite la administración de derechos digitales (DRM) en el SDK de Windows Media Format basado en x64.</span><span class="sxs-lookup"><span data-stu-id="e6eea-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="e6eea-145">Nueva versión del códec de imagen de Windows Media Video</span><span class="sxs-lookup"><span data-stu-id="e6eea-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="e6eea-146">El códec Windows Media Video 9 Image V2 simplifica los cálculos de geometría de ejemplo para la panorámica y el zoom.</span><span class="sxs-lookup"><span data-stu-id="e6eea-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="e6eea-147">El nuevo códec también admite varias transiciones complejas entre imágenes.</span><span class="sxs-lookup"><span data-stu-id="e6eea-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="e6eea-148">Nueva versión de los códecs de Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="e6eea-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="e6eea-149">El SDK de Windows Media Format 9,5 incluye los siguientes códecs de audio actualizados:</span><span class="sxs-lookup"><span data-stu-id="e6eea-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="e6eea-150">Windows Media Audio 9,1</span><span class="sxs-lookup"><span data-stu-id="e6eea-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="e6eea-151">Windows Media Audio 9,1 Professional</span><span class="sxs-lookup"><span data-stu-id="e6eea-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="e6eea-152">Windows Media Audio 9,1 Lossless</span><span class="sxs-lookup"><span data-stu-id="e6eea-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="e6eea-153">Compatibilidad del Protocolo de Windows Media DRM 10 con dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="e6eea-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="e6eea-154">El SDK de Windows Media Format 9,5 admite el nuevo protocolo de transferencia segura de Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="e6eea-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="e6eea-155">Este protocolo se puede usar para transmitir contenido cifrado a través de una red local a un dispositivo de reproducción, como un receptor de vídeo de un conjunto.</span><span class="sxs-lookup"><span data-stu-id="e6eea-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="e6eea-156">La mayoría de los procedimientos que se usan para implementar la compatibilidad con Windows Media DRM 10 para dispositivos de red deben ser realizados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6eea-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="e6eea-157">Sin embargo, puede usar los métodos del SDK de Windows Media Format para proporcionar la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="e6eea-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="e6eea-158">Mantener una base de datos de dispositivos, incluidos los que están habilitados para Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="e6eea-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="e6eea-159">Valide los dispositivos para asegurarse de que estén lo suficientemente cerca del cliente en la red para la transmisión por secuencias segura.</span><span class="sxs-lookup"><span data-stu-id="e6eea-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="e6eea-160">Convertir archivos protegidos con DRM en Windows Media DRM 10 para transmisiones de dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="e6eea-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="e6eea-161">Escribir archivos con datos cifrados previamente.</span><span class="sxs-lookup"><span data-stu-id="e6eea-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="e6eea-162">Compatibilidad con nuevas licencias de DRM</span><span class="sxs-lookup"><span data-stu-id="e6eea-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="e6eea-163">Las nuevas licencias creadas con el SDK de Windows Media Rights Manager usan niveles de protección de salida (OPLs) para especificar derechos y restricciones para reproducir y copiar contenido.</span><span class="sxs-lookup"><span data-stu-id="e6eea-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="e6eea-164">El SDK de Windows Media Format proporciona compatibilidad para leer el OPLs de una licencia.</span><span class="sxs-lookup"><span data-stu-id="e6eea-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="e6eea-165">Nuevo códec de vídeo</span><span class="sxs-lookup"><span data-stu-id="e6eea-165">New Video Codec</span></span>

<span data-ttu-id="e6eea-166">El códec de perfil avanzado de Windows Media Video 9 se basa en la alta calidad del códec de Windows Media Video 9 al agregar compatibilidad con la codificación entrelazada.</span><span class="sxs-lookup"><span data-stu-id="e6eea-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="e6eea-167">Salida S/PDIF</span><span class="sxs-lookup"><span data-stu-id="e6eea-167">S/PDIF Output</span></span>

<span data-ttu-id="e6eea-168">El contenido codificado con uno de los códecs profesionales de Windows Media Audio se puede transferir o transmitir mediante el formato de interconexión digital de Sony/Philips (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="e6eea-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="e6eea-169">Low-Delay audio</span><span class="sxs-lookup"><span data-stu-id="e6eea-169">Low-Delay Audio</span></span>

<span data-ttu-id="e6eea-170">Los códecs Professional Windows Media Audio 9,1 y Windows Media Audio 9,1 ahora admiten varios formatos de retraso bajo.</span><span class="sxs-lookup"><span data-stu-id="e6eea-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="e6eea-171">Estos formatos producen secuencias de audio que se pueden iniciar más rápidamente, lo que reduce la latencia en escenarios de cambio de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e6eea-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="e6eea-172">La latencia general de las difusiones en vivo también se ha mejorado mediante el uso de formatos de retraso reducido.</span><span class="sxs-lookup"><span data-stu-id="e6eea-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="e6eea-173">Modo de búsqueda aproximado</span><span class="sxs-lookup"><span data-stu-id="e6eea-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="e6eea-174">Ahora puede buscar una hora aproximada en un archivo ASF con el lector.</span><span class="sxs-lookup"><span data-stu-id="e6eea-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="e6eea-175">Este modo mejora el rendimiento al realizar una búsqueda imprecisa, como cuando un usuario hace clic en la barra de búsqueda de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e6eea-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="e6eea-176">La búsqueda aproximada devuelve el ejemplo multimedia para el cleanpoint anterior en lugar de reconstruir el ejemplo para el tiempo que se busca.</span><span class="sxs-lookup"><span data-stu-id="e6eea-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="e6eea-177">Grabación de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="e6eea-177">Playlist Burning</span></span>

<span data-ttu-id="e6eea-178">Windows Media DRM 10 admite derechos para copiar archivos de audio en el CD de libro rojo como parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e6eea-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="e6eea-179">El SDK de Windows Media Format proporciona métodos para comprobar si se pueden copiar los archivos de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e6eea-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="e6eea-180">Compatibilidad mejorada con Multiple-Language para metadatos</span><span class="sxs-lookup"><span data-stu-id="e6eea-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="e6eea-181">En el SDK de Windows Media Format 9 series, todos los metadatos agregados a un archivo se asignaron a una lista de idiomas que tenía el identificador de idioma del idioma predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e6eea-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="e6eea-182">Esto causaba problemas cuando los distribuidores de contenido de diferentes configuraciones regionales agregaban algunos metadatos, ya que los usuarios de la configuración regional del distribuidor solo ven los pocos atributos agregados para su idioma.</span><span class="sxs-lookup"><span data-stu-id="e6eea-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="e6eea-183">El SDK de Windows Media Format 9,5 soluciona este problema al no crear una lista de idiomas hasta que haya atributos de dos idiomas presentes en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e6eea-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="e6eea-184">En ese momento, todos los metadatos se asocian a la configuración regional del segundo idioma, que luego se convierte en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e6eea-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="e6eea-185">De esta manera, un distribuidor de contenido puede mantener intactos todos los metadatos originales de un archivo, como el título y el autor, al agregar algunos atributos relacionados con su configuración regional.</span><span class="sxs-lookup"><span data-stu-id="e6eea-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="e6eea-186">SDK de Windows Media Administrador de dispositivos incluido en la instalación</span><span class="sxs-lookup"><span data-stu-id="e6eea-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="e6eea-187">El paquete de instalación del SDK de Windows Media Format 9,5 instala el SDK de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e6eea-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="e6eea-188">La documentación del SDK de Windows Media Administrador de dispositivos se puede encontrar en la carpeta C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (la carpeta será diferente si no instala el SDK de Windows Media Format en la carpeta predeterminada).</span><span class="sxs-lookup"><span data-stu-id="e6eea-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="e6eea-189">Documentación de la interfaz de códec</span><span class="sxs-lookup"><span data-stu-id="e6eea-189">Codec Interface Documentation</span></span>

<span data-ttu-id="e6eea-190">En esta documentación se incluye información acerca del uso de los códecs de Windows Media Audio y vídeo fuera del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e6eea-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="e6eea-191">Esta documentación se publicó originalmente como parte de una descarga de Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="e6eea-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="e6eea-192">Las aplicaciones de ejemplo que muestran el uso del códec DMOs directamente se incluyen en la instalación del SDK de Windows Media Format junto con los encabezados.</span><span class="sxs-lookup"><span data-stu-id="e6eea-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6eea-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6eea-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6eea-194">**Acerca del SDK de Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="e6eea-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




