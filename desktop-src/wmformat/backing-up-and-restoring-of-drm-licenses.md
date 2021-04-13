---
title: Copia de seguridad y restauración de licencias de DRM
description: Copia de seguridad y restauración de licencias de DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- SDK de Windows Media Format, copia de seguridad de licencias de DRM
- SDK de Windows Media Format, restaurar licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, característica de restauración de copia de seguridad
- SDK de Windows Media Format, servicio de administración de licencias
- SDK de Windows Media Format, detección de fraudes
- Administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- Administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), característica de restauración de copia de seguridad
- DRM (administración de derechos digitales), característica de restauración de copia de seguridad
- Administración de derechos digitales (DRM), servicio de administración de licencias
- DRM (administración de derechos digitales), servicio de administración de licencias
- Administración de derechos digitales (DRM), detección de fraudes
- DRM (administración de derechos digitales), detección de fraudes
- copia de seguridad de licencias de DRM
- restauración de licencias de DRM
- licencias, DRM
- licencias, copia de seguridad de DRM
- licencias, restaurar DRM
- Característica de restauración de copia de seguridad
- Servicio de administración de licencias
- detección de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104359479"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="d6e2d-130">Copia de seguridad y restauración de licencias de DRM</span><span class="sxs-lookup"><span data-stu-id="d6e2d-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="d6e2d-131">Con la característica de restauración de copia de seguridad, los usuarios pueden realizar copias de seguridad y restaurar [*licencias*](wmformat-glossary.md) en el mismo equipo o en otros equipos.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="d6e2d-132">Esta característica permite a los usuarios transferir licencias a un nuevo equipo o al mismo equipo (por ejemplo, después de volver a formatear el disco duro).</span><span class="sxs-lookup"><span data-stu-id="d6e2d-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="d6e2d-133">Además, los usuarios pueden reproducir archivos ASF protegidos en más de un equipo.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="d6e2d-134">Para fomentar el uso legítimo de una licencia, una directiva de detección de fraudes restringe el número de veces que se puede restaurar una licencia.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="d6e2d-135">Microsoft proporciona un servicio que realiza un seguimiento del número de equipos en los que se ha restaurado una licencia; Si se alcanza un límite, el usuario no podrá restaurar la licencia.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="d6e2d-136">Permitir o denegar el derecho a realizar copias de seguridad y restauraciones</span><span class="sxs-lookup"><span data-stu-id="d6e2d-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="d6e2d-137">La característica de restauración de copia de seguridad solo funciona con licencias para las que se proporciona la opción de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="d6e2d-138">Si los propietarios de contenido o los emisores de licencias no desean esta característica, o si emiten licencias que contienen un estado seguro (como operaciones contables o tiempo limitado), pueden no permitir este derecho.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="d6e2d-139">Cuando no se puede restaurar una licencia porque un usuario no tiene el derecho, se pasa un [*identificador de clave*](wmformat-glossary.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="d6e2d-140">Como mínimo, se debe notificar al usuario que no se pudo realizar una copia de seguridad de algunas licencias, aunque el usuario no sabe a qué licencias hace referencia este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="d6e2d-141">Si conoce el identificador de clave para los archivos protegidos disponibles, puede desarrollar una solución más sólida para informar al usuario.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="d6e2d-142">Por ejemplo, un reproductor podría desarrollarse para una etiqueta de registro que proporcione canciones protegidas en Internet.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="d6e2d-143">Se puede realizar un seguimiento de estas canciones y de sus identificadores de clave en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="d6e2d-144">Si no se pudo realizar una copia de seguridad de algunas licencias, la aplicación del reproductor podría usar el identificador de clave para consultar el nombre de las canciones en la base de datos y, a continuación, informar al usuario sobre las canciones de las que no se pueden realizar copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="d6e2d-145">O bien, se podría crear una biblioteca de música para cada usuario localmente, y el identificador de clave podría usarse para recuperar más información acerca de las licencias de las que no se pudo realizar una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="d6e2d-146">El servicio de administración de licencias</span><span class="sxs-lookup"><span data-stu-id="d6e2d-146">The License Management Service</span></span>

<span data-ttu-id="d6e2d-147">Cuando se implementa la característica de restauración de copia de seguridad, un servicio de administración de licencias hospedado por Microsoft administra la restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="d6e2d-148">En primer lugar, los usuarios copian las licencias en la aplicación, por ejemplo, eligiendo una opción de menú.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="d6e2d-149">Se realiza una copia de seguridad de todas las licencias del equipo en una ubicación especificada, como un disquete.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="d6e2d-150">Después, los usuarios restauran las licencias mediante la aplicación, por ejemplo, eligiendo una opción de menú y especificando su ubicación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="d6e2d-151">En este momento, el usuario debe estar conectado a Internet. una solicitud de la aplicación se envía al servicio de administración de licencias.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="d6e2d-152">Si el equipo desde el que se realizó la copia de seguridad de la licencia es diferente del equipo original (o se ha cambiado el formato del equipo original), el servicio de administración de licencias emite una nueva licencia al nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="d6e2d-153">De lo contrario, se reenvía la licencia que se emitió previamente a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="d6e2d-154">Dado que el servicio de administración de licencias recupera información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el [sitio web de Microsoft](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="d6e2d-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="d6e2d-155">Cuando un usuario final restaura una licencia en otro equipo y la licencia requiere la individualización, el usuario final debe autorizar la actualización de los componentes de DRM.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="d6e2d-156">Debe implementar un proceso en la aplicación de reproducción para admitir esta característica.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="d6e2d-157">Detección de fraudes</span><span class="sxs-lookup"><span data-stu-id="d6e2d-157">Detecting Fraud</span></span>

<span data-ttu-id="d6e2d-158">El usuario puede restaurar una licencia un número limitado de veces.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="d6e2d-159">Cada vez que se restaura una licencia, el servicio de administración de licencias realiza su seguimiento e incrementa el recuento de esa licencia en uno.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="d6e2d-160">Al restaurar una licencia a un equipo en el que se ha restaurado anteriormente la licencia (por ejemplo, el equipo desde el que se realizó la copia de seguridad de la licencia), el recuento no se incrementa.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="d6e2d-161">Un equipo se considera diferente si tiene un nuevo sistema operativo o si se ha vuelto a instalar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="d6e2d-162">De acuerdo con la Directiva de detección de fraudes de Microsoft, cuando una licencia se ha restaurado un número determinado de veces, la aplicación recibe una dirección URL de los componentes de DRM y es responsable de abrir un explorador y mostrar la página web, lo que indica que es posible que se haya infringido el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="d6e2d-163">El usuario debe ponerse en contacto con el distribuidor de licencias, que debe determinar si la solicitud es válida.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="d6e2d-164">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="d6e2d-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d6e2d-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6e2d-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e2d-166">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="d6e2d-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="d6e2d-167">**Copia de seguridad y restauración de licencias**</span><span class="sxs-lookup"><span data-stu-id="d6e2d-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




