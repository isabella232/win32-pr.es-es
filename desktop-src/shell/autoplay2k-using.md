---
description: Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión activa, se determina el contenido del dispositivo o el medio. La reproducción automática, según la configuración actual, realiza una de las acciones siguientes.
title: Uso y configuración de la reproducción automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808876"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="807e2-104">Uso y configuración de la reproducción automática</span><span class="sxs-lookup"><span data-stu-id="807e2-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="807e2-105">Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión activa, se determina el contenido del dispositivo o el medio.</span><span class="sxs-lookup"><span data-stu-id="807e2-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="807e2-106">La reproducción automática, según la configuración actual, realiza una de las acciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="807e2-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="807e2-107">Reproduce el contenido automáticamente.</span><span class="sxs-lookup"><span data-stu-id="807e2-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="807e2-108">Muestra un cuadro de diálogo que pide al usuario que elija un controlador predeterminado para un solo tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="807e2-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="807e2-109">Presenta, en el caso de contenido mixto, una lista de las aplicaciones de controlador disponibles que se van a iniciar.</span><span class="sxs-lookup"><span data-stu-id="807e2-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="807e2-110">El controlador elegido reproduce automáticamente su tipo de contenido asociado.</span><span class="sxs-lookup"><span data-stu-id="807e2-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="807e2-111">Muestra una vista de carpeta estándar de los archivos.</span><span class="sxs-lookup"><span data-stu-id="807e2-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="807e2-112">No hace nada si, antes, el usuario decidió **no realizar ninguna acción** para ese tipo de contenido, sino que **siempre realiza la acción seleccionada**.</span><span class="sxs-lookup"><span data-stu-id="807e2-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="807e2-113">Si el contenido no cumple los criterios de reproducción automática, el evento se pasa a la adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="807e2-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="807e2-114">En los temas siguientes se describe la instalación y el uso de la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="807e2-115">Preparación del hardware y el software para su uso con reproducción automática</span><span class="sxs-lookup"><span data-stu-id="807e2-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="807e2-116">Cómo busca la reproducción automática multimedia</span><span class="sxs-lookup"><span data-stu-id="807e2-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="807e2-117">Definir tipos de contenido único y mixto</span><span class="sxs-lookup"><span data-stu-id="807e2-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="807e2-118">Escenarios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="807e2-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="807e2-119">Reproducción automática de dispositivos de almacenamiento con medios de imagen</span><span class="sxs-lookup"><span data-stu-id="807e2-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="807e2-120">Reproducción automática de dispositivos de reproducción de archivos de música y dispositivos de almacenamiento que contienen medios de música</span><span class="sxs-lookup"><span data-stu-id="807e2-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="807e2-121">Reproducción automática para reproducción de vídeo en la primera presentación</span><span class="sxs-lookup"><span data-stu-id="807e2-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="807e2-122">Asignar aplicaciones de controlador predeterminadas</span><span class="sxs-lookup"><span data-stu-id="807e2-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="807e2-123">Controlar medios que contienen tipos de contenido mixtos</span><span class="sxs-lookup"><span data-stu-id="807e2-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="807e2-124">Interfaces de usuario de reproducción automática</span><span class="sxs-lookup"><span data-stu-id="807e2-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="807e2-125">Cuadro de diálogo de tipo de contenido único</span><span class="sxs-lookup"><span data-stu-id="807e2-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="807e2-126">Cuadro de diálogo medios mixtos</span><span class="sxs-lookup"><span data-stu-id="807e2-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="807e2-127">Página de propiedades</span><span class="sxs-lookup"><span data-stu-id="807e2-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="807e2-128">Preparación del hardware y el software para su uso con reproducción automática</span><span class="sxs-lookup"><span data-stu-id="807e2-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="807e2-129">Es necesario que aparezcan varios fragmentos de información en el registro para que funcione la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="807e2-130">Estos fragmentos de información interactúan y hacen referencia entre sí para formar el entorno completo de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="807e2-131">En este documento se presenta la configuración de cada uno de estos fragmentos de información como un procedimiento independiente individual.</span><span class="sxs-lookup"><span data-stu-id="807e2-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="807e2-132">Vea los temas siguientes para obtener instrucciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="807e2-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="807e2-133">Asignación de un controlador de dispositivo a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="807e2-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="807e2-134">Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos</span><span class="sxs-lookup"><span data-stu-id="807e2-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="807e2-135">Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante una clase de dispositivo</span><span class="sxs-lookup"><span data-stu-id="807e2-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="807e2-136">Cómo evitar la reproducción automática de un componente</span><span class="sxs-lookup"><span data-stu-id="807e2-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="807e2-137">Cómo registrar un controlador para un evento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="807e2-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="807e2-138">Cómo usar eventos de reproducción automática en aplicaciones en ejecución</span><span class="sxs-lookup"><span data-stu-id="807e2-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="807e2-139">Cómo registrar un controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="807e2-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="807e2-140">Cómo busca la reproducción automática multimedia</span><span class="sxs-lookup"><span data-stu-id="807e2-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="807e2-141">La reproducción automática busca los elementos multimedia de cuatro niveles de directorio por debajo del directorio raíz para buscar tipos de archivo conocidos.</span><span class="sxs-lookup"><span data-stu-id="807e2-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="807e2-142">Usa el valor PerceivedType asociado a una extensión de nombre de archivo en el registro para determinar la categoría del archivo, si se trata de una imagen, un archivo de audio o un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="807e2-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="807e2-143">Con esta información, la reproducción automática inicia el controlador adecuado para ese dispositivo y tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="807e2-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="807e2-144">Para obtener más información, vea [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="807e2-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="807e2-145">Definir tipos de contenido único y mixto</span><span class="sxs-lookup"><span data-stu-id="807e2-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="807e2-146">La reproducción automática define tres categorías de contenido principales.</span><span class="sxs-lookup"><span data-stu-id="807e2-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="807e2-147">Imágenes</span><span class="sxs-lookup"><span data-stu-id="807e2-147">Pictures</span></span>
-   <span data-ttu-id="807e2-148">Música</span><span class="sxs-lookup"><span data-stu-id="807e2-148">Music</span></span>
-   <span data-ttu-id="807e2-149">Vídeo</span><span class="sxs-lookup"><span data-stu-id="807e2-149">Video</span></span>

<span data-ttu-id="807e2-150">Se considera que un medio contiene un solo tipo de contenido si todos los archivos del medio se encuentran en una sola de estas tres categorías.</span><span class="sxs-lookup"><span data-stu-id="807e2-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="807e2-151">Tenga en cuenta que esto no significa que los archivos deben tener el mismo tipo de *archivo* ;. jpg,. gif y. bmp son tipos de archivo diferentes, pero un tipo de contenido (imágenes).</span><span class="sxs-lookup"><span data-stu-id="807e2-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="807e2-152">Si los tipos de contenido admitidos están presentes en el medio, pero ningún tipo de contenido único puede tener en cuenta el 100 por ciento del total, se considera que el medio contiene un tipo de contenido mixto y se administra en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="807e2-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="807e2-153">Para obtener más información, vea [controlar medios que contienen tipos de contenido mixto](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="807e2-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="807e2-154">Escenarios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="807e2-154">Sample Scenarios</span></span>

<span data-ttu-id="807e2-155">Los escenarios siguientes proporcionan una descripción básica de lo que se debe esperar de la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="807e2-156">Reproducción automática de dispositivos de almacenamiento con medios de imagen</span><span class="sxs-lookup"><span data-stu-id="807e2-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="807e2-157">El usuario conecta un dispositivo de lector CompactFlash USB SanDisk que ya tiene un medio insertado con un tipo de contenido de imagen del 100 por ciento en forma de archivos. jpg.</span><span class="sxs-lookup"><span data-stu-id="807e2-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="807e2-158">La notificación muestra **el nuevo hardware-SanDisk ImageMate**.</span><span class="sxs-lookup"><span data-stu-id="807e2-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="807e2-159">Reproducción automática inicia la aplicación de imagen adecuada.</span><span class="sxs-lookup"><span data-stu-id="807e2-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="807e2-160">Del mismo modo, cuando el usuario inserta el mismo medio de CompactFlash en el lector cuando el lector ya está conectado al sistema, el evento de inserción de medios también hace que la reproducción automática inicie la aplicación de presentación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="807e2-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="807e2-161">El usuario tiene la opción de ir a la página de propiedades del dispositivo multimedia SanDisk para cambiar el valor predeterminado a otra aplicación de reproducción automática registrada, como el Asistente para escáneres y cámaras o Picture It!.</span><span class="sxs-lookup"><span data-stu-id="807e2-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="807e2-162">Reproducción automática de dispositivos de reproducción de archivos de música y dispositivos de almacenamiento que contienen medios de música</span><span class="sxs-lookup"><span data-stu-id="807e2-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="807e2-163">El usuario conecta un reproductor MP3 de Diamond Rio USB.</span><span class="sxs-lookup"><span data-stu-id="807e2-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="807e2-164">La notificación muestra **el nuevo hardware, el reproductor mp3 de Diamond Rio**.</span><span class="sxs-lookup"><span data-stu-id="807e2-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="807e2-165">La reproducción automática reproduce los archivos con el controlador predeterminado registrado, por ejemplo, Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="807e2-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="807e2-166">Del mismo modo, si el usuario inserta cualquier medio que contenga archivos. mp3 (por ejemplo, CompactFlash, SmartMedia, Memory Stick o un CD-ROM) que representen el 100 por ciento del contenido total admitido en un dispositivo de almacenamiento, el evento de inserción de medios también haría que la reproducción automática reproducira los archivos con la Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="807e2-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="807e2-167">El usuario puede tener acceso a la hoja de propiedades del dispositivo de almacenamiento y cambiar la acción predeterminada a otra aplicación de reproducción automática registrada, como WinAmp o Real Player.</span><span class="sxs-lookup"><span data-stu-id="807e2-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="807e2-168">Reproducción automática para reproducción de vídeo en la primera presentación</span><span class="sxs-lookup"><span data-stu-id="807e2-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="807e2-169">El usuario se conecta a una cámara de vídeo digital 1394 por primera vez.</span><span class="sxs-lookup"><span data-stu-id="807e2-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="807e2-170">Al usuario se le presenta un cuadro de diálogo simple que pregunta qué aplicación se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="807e2-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="807e2-171">Las opciones son ejecutar una de las aplicaciones de reproducción automática registradas o abrir una carpeta para ver los archivos.</span><span class="sxs-lookup"><span data-stu-id="807e2-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="807e2-172">El usuario puede establecer el comportamiento seleccionado para que se guarde como la acción predeterminada para los eventos de conexión en caliente de la cámara de vídeo digital posterior.</span><span class="sxs-lookup"><span data-stu-id="807e2-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="807e2-173">Asignar aplicaciones de controlador predeterminadas</span><span class="sxs-lookup"><span data-stu-id="807e2-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="807e2-174">Una instalación nueva de Windows busca la reproducción automática con un conjunto de aplicaciones de controlador registradas.</span><span class="sxs-lookup"><span data-stu-id="807e2-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="807e2-175">Las aplicaciones registradas de forma predeterminada durante una instalación de Windows son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="807e2-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="807e2-176">Tipo de soporte</span><span class="sxs-lookup"><span data-stu-id="807e2-176">Media Type</span></span></th>
<th><span data-ttu-id="807e2-177">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="807e2-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="807e2-178">Imágenes</span><span class="sxs-lookup"><span data-stu-id="807e2-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="807e2-179">Presentación (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="807e2-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="807e2-180">Asistente para cámara y escáner</span><span class="sxs-lookup"><span data-stu-id="807e2-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="807e2-181">Asistente para impresión</span><span class="sxs-lookup"><span data-stu-id="807e2-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="807e2-182">Abrir carpeta</span><span class="sxs-lookup"><span data-stu-id="807e2-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="807e2-183">Música</span><span class="sxs-lookup"><span data-stu-id="807e2-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="807e2-184">Media Player de Windows (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="807e2-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="807e2-185">Abrir carpeta</span><span class="sxs-lookup"><span data-stu-id="807e2-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="807e2-186">Vídeo</span><span class="sxs-lookup"><span data-stu-id="807e2-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="807e2-187">Media Player de Windows (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="807e2-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="807e2-188">Abrir carpeta</span><span class="sxs-lookup"><span data-stu-id="807e2-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="807e2-189">En el caso de los tipos no compatibles, se pide a los usuarios que asignen la configuración predeterminada para la acción de reproducción automática asociada con cada dispositivo de almacenamiento en su primera introducción al sistema.</span><span class="sxs-lookup"><span data-stu-id="807e2-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="807e2-190">En ese momento, se solicita al usuario que elija una acción de una lista proporcionada de aplicaciones registradas o que muestre una vista de carpeta que enumera el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="807e2-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="807e2-191">El usuario también tiene la opción de elegir que se le solicite cada vez que se detecta el tipo de medio en lugar de guardar una aplicación concreta como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="807e2-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="807e2-192">Los fabricantes de dispositivos tienen la opción de registrar y asignar las aplicaciones predeterminadas que se usarán con sus productos particulares.</span><span class="sxs-lookup"><span data-stu-id="807e2-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="807e2-193">En estos casos, no se muestra el cuadro de diálogo que ofrece la opción de elegir al usuario.</span><span class="sxs-lookup"><span data-stu-id="807e2-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="807e2-194">Para que la reproducción automática se ofrezca como una opción de controlador, las aplicaciones recién instaladas deben registrarse en el registro.</span><span class="sxs-lookup"><span data-stu-id="807e2-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="807e2-195">Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="807e2-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="807e2-196">Los usuarios siempre pueden cambiar el controlador de reproducción automática predeterminado para cualquier dispositivo de almacenamiento o tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="807e2-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="807e2-197">La página de propiedades de reproducción automática es accesible para su cambio en la hoja de propiedades del dispositivo de almacenamiento en **mi PC**.</span><span class="sxs-lookup"><span data-stu-id="807e2-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="807e2-198">Para obtener ejemplos de mensajes de usuario y páginas de propiedades, consulte las [interfaces de usuario de reproducción automática](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="807e2-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="807e2-199">Controlar medios que contienen tipos de contenido mixtos</span><span class="sxs-lookup"><span data-stu-id="807e2-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="807e2-200">Cuando se presenta la reproducción automática con un medio de contenido mixto, se requiere la intervención del usuario antes de que pueda actuar.</span><span class="sxs-lookup"><span data-stu-id="807e2-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="807e2-201">En este caso, se presenta al usuario un cuadro de diálogo que contiene una lista filtrada de todas las aplicaciones registradas adecuadas disponibles para los tipos de contenido presentes en el medio.</span><span class="sxs-lookup"><span data-stu-id="807e2-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="807e2-202">El usuario puede elegir una de estas aplicaciones para la reproducción automática de un tipo de contenido determinado, mientras que el resto permanece intacto.</span><span class="sxs-lookup"><span data-stu-id="807e2-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="807e2-203">Dado que la composición de los medios de contenido mixto varía con cada disco individual, no hay ninguna opción para guardar esta opción como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="807e2-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="807e2-204">Para obtener ejemplos de mensajes de usuario, consulte las [interfaces de usuario de reproducción automática](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="807e2-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="807e2-205">Interfaces de usuario de reproducción automática</span><span class="sxs-lookup"><span data-stu-id="807e2-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="807e2-206">Hay tres interfaces de usuario posibles.</span><span class="sxs-lookup"><span data-stu-id="807e2-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="807e2-207">Cuadro de diálogo que pide al usuario que escriba una acción para un único tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="807e2-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="807e2-208">Cuadro de diálogo que pide al usuario que escriba una acción para los tipos de contenido mixto</span><span class="sxs-lookup"><span data-stu-id="807e2-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="807e2-209">Una página de propiedades</span><span class="sxs-lookup"><span data-stu-id="807e2-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="807e2-210">Cuadro de diálogo de tipo de contenido único</span><span class="sxs-lookup"><span data-stu-id="807e2-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="807e2-211">Se muestra un cuadro de diálogo similar al siguiente cuando todavía no se ha asignado a ningún medio compatible una acción de reproducción automática predeterminada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="807e2-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![captura de pantalla del cuadro de diálogo tipo de contenido único](images/pix.png)

<span data-ttu-id="807e2-213">Los usuarios pueden realizar una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="807e2-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="807e2-214">Elija una acción de la lista de aplicaciones registradas.</span><span class="sxs-lookup"><span data-stu-id="807e2-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="807e2-215">Enumere los archivos del medio en una vista de carpeta normal.</span><span class="sxs-lookup"><span data-stu-id="807e2-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="807e2-216">No realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="807e2-216">Take no action.</span></span>

<span data-ttu-id="807e2-217">Un usuario también puede guardar una opción como acción predeterminada para este medio haciendo clic en el cuadro **realizar siempre la acción seleccionada** .</span><span class="sxs-lookup"><span data-stu-id="807e2-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="807e2-218">Una vez realizada esta opción, el cuadro de diálogo no se muestra de nuevo.</span><span class="sxs-lookup"><span data-stu-id="807e2-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="807e2-219">Sin embargo, en el Service Pack 1 (SP1) de Windows XP, si se agrega al equipo una nueva aplicación que puede controlar un tipo de medio determinado, el cuadro de diálogo se muestra de nuevo al usuario, lo que les permite seleccionar la nueva aplicación como la acción de reproducción automática predeterminada.</span><span class="sxs-lookup"><span data-stu-id="807e2-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="807e2-220">Las aplicaciones también se pueden establecer como la selección predeterminada cuando se instalan.</span><span class="sxs-lookup"><span data-stu-id="807e2-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="807e2-221">Windows XP SP1 también agrega una característica que conserva la elección de la acción de reproducción automática del usuario si no hace clic en el cuadro **realizar siempre la acción seleccionada** .</span><span class="sxs-lookup"><span data-stu-id="807e2-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="807e2-222">Si un usuario elige una acción de reproducción automática para una única instancia, la siguiente vez que se presenta el cuadro de diálogo para ese tipo de medio, la misma acción es la selección predeterminada.</span><span class="sxs-lookup"><span data-stu-id="807e2-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="807e2-223">Para que una aplicación se incluya en la lista de acciones posibles, debe estar registrada con la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="807e2-224">Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="807e2-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="807e2-225">Cuadro de diálogo medios mixtos</span><span class="sxs-lookup"><span data-stu-id="807e2-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="807e2-226">El siguiente cuadro de diálogo se muestra cuando se presenta al sistema cualquier medio que contenga una combinación de tipos de archivo admitidos.</span><span class="sxs-lookup"><span data-stu-id="807e2-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="807e2-227">Esto es esencialmente el mismo que el cuadro de diálogo de medio de contenido único, pero con dos diferencias importantes.</span><span class="sxs-lookup"><span data-stu-id="807e2-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="807e2-228">En primer lugar, las opciones de acción disponibles constan de una lista filtrada de las aplicaciones relevantes para todos los tipos de contenido presentes en el medio.</span><span class="sxs-lookup"><span data-stu-id="807e2-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="807e2-229">En segundo lugar, no hay ninguna opción para elegir una acción predeterminada permanente, ya que los tipos de contenido y los porcentajes de los medios de contenido mixto son demasiado impredecibles.</span><span class="sxs-lookup"><span data-stu-id="807e2-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![captura de pantalla del cuadro de diálogo medios mixtos](images/mix.png)

<span data-ttu-id="807e2-231">Para que una aplicación se incluya en la lista de acciones posibles, debe estar registrada con la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="807e2-232">Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="807e2-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="807e2-233">Página de propiedades</span><span class="sxs-lookup"><span data-stu-id="807e2-233">Property Page</span></span>

<span data-ttu-id="807e2-234">A continuación se muestra una página de propiedades de reproducción automática de ejemplo para un dispositivo de DVD o CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="807e2-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![captura de pantalla de la página de propiedades](images/apdlg.png)

<span data-ttu-id="807e2-236">Cada tipo de dispositivo ofrece un subconjunto adecuado de tipos de contenido para la configuración de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="807e2-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="807e2-237">A su vez, cada tipo de contenido, cuando se selecciona, ofrece una lista adecuada de opciones de acción en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="807e2-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="807e2-238">Se puede elegir una acción diferente para cada tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="807e2-238">A different action can be chosen for each content type.</span></span>

 

 



