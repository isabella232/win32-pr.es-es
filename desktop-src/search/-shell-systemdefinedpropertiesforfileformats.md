---
description: Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined propiedades de los formatos de archivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153946"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="1710a-103">System-Defined propiedades de los formatos de archivo personalizados</span><span class="sxs-lookup"><span data-stu-id="1710a-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="1710a-104">Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="1710a-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="1710a-105">Si va a crear un formato de archivo personalizado, debe admitir tantas propiedades definidas por el sistema como pueda.</span><span class="sxs-lookup"><span data-stu-id="1710a-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="1710a-106">Antes de crear un controlador de propiedades personalizado, debe revisar los controladores proporcionados por el sistema para ver si puede usar uno en lugar de escribir el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="1710a-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="1710a-107">En la tabla siguiente se clasifican los formatos de archivo y, a continuación, se enumeran las propiedades del sistema más importantes que debe admitir el formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="1710a-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="1710a-108">Para proporcionar una experiencia de usuario adecuada, debe admitir todas las propiedades de prioridad 1 y 2 para su categoría de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="1710a-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="1710a-109">Comunicaciones</span><span class="sxs-lookup"><span data-stu-id="1710a-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="1710a-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="1710a-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="1710a-111">Documentos</span><span class="sxs-lookup"><span data-stu-id="1710a-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="1710a-112">Genérico</span><span class="sxs-lookup"><span data-stu-id="1710a-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="1710a-113">Canción</span><span class="sxs-lookup"><span data-stu-id="1710a-113">Music</span></span>](#music)
-   [<span data-ttu-id="1710a-114">Imágenes</span><span class="sxs-lookup"><span data-stu-id="1710a-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="1710a-115">Vídeos</span><span class="sxs-lookup"><span data-stu-id="1710a-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="1710a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1710a-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="1710a-117">Comunicaciones</span><span class="sxs-lookup"><span data-stu-id="1710a-117">Communications</span></span>



| <span data-ttu-id="1710a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-118">Name</span></span>            | <span data-ttu-id="1710a-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-119">Property</span></span>                               | <span data-ttu-id="1710a-120">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="1710a-121">Fecha de recepción</span><span class="sxs-lookup"><span data-stu-id="1710a-121">Date received</span></span>   | <span data-ttu-id="1710a-122">System. Message. DateReceived</span><span class="sxs-lookup"><span data-stu-id="1710a-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="1710a-123">1</span><span class="sxs-lookup"><span data-stu-id="1710a-123">1</span></span>        |
| <span data-ttu-id="1710a-124">Desde nombres</span><span class="sxs-lookup"><span data-stu-id="1710a-124">From names</span></span>      | <span data-ttu-id="1710a-125">System. Message. FromName</span><span class="sxs-lookup"><span data-stu-id="1710a-125">System.Message.FromName</span></span>                | <span data-ttu-id="1710a-126">1</span><span class="sxs-lookup"><span data-stu-id="1710a-126">1</span></span>        |
| <span data-ttu-id="1710a-127">Tiene datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="1710a-127">Has attachments</span></span> | <span data-ttu-id="1710a-128">System. Message. HasAttachments</span><span class="sxs-lookup"><span data-stu-id="1710a-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="1710a-129">1</span><span class="sxs-lookup"><span data-stu-id="1710a-129">1</span></span>        |
| <span data-ttu-id="1710a-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="1710a-130">Mailbox</span></span>         | <span data-ttu-id="1710a-131">System. Communication. storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="1710a-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="1710a-132">1</span><span class="sxs-lookup"><span data-stu-id="1710a-132">1</span></span>        |
| <span data-ttu-id="1710a-133">NOMBRE</span><span class="sxs-lookup"><span data-stu-id="1710a-133">Name</span></span>            | <span data-ttu-id="1710a-134">System. FileName</span><span class="sxs-lookup"><span data-stu-id="1710a-134">System.FileName</span></span>                        | <span data-ttu-id="1710a-135">1</span><span class="sxs-lookup"><span data-stu-id="1710a-135">1</span></span>        |
| <span data-ttu-id="1710a-136">Asunto</span><span class="sxs-lookup"><span data-stu-id="1710a-136">Subject</span></span>         | <span data-ttu-id="1710a-137">System. Subject</span><span class="sxs-lookup"><span data-stu-id="1710a-137">System.Subject</span></span>                         | <span data-ttu-id="1710a-138">1</span><span class="sxs-lookup"><span data-stu-id="1710a-138">1</span></span>        |
| <span data-ttu-id="1710a-139">A nombres</span><span class="sxs-lookup"><span data-stu-id="1710a-139">To names</span></span>        | <span data-ttu-id="1710a-140">System. Message. ToName</span><span class="sxs-lookup"><span data-stu-id="1710a-140">System.Message.ToName</span></span>                  | <span data-ttu-id="1710a-141">1</span><span class="sxs-lookup"><span data-stu-id="1710a-141">1</span></span>        |
| <span data-ttu-id="1710a-142">Category</span><span class="sxs-lookup"><span data-stu-id="1710a-142">Category</span></span>        | <span data-ttu-id="1710a-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="1710a-143">System.Category</span></span>                        | <span data-ttu-id="1710a-144">2</span><span class="sxs-lookup"><span data-stu-id="1710a-144">2</span></span>        |
| <span data-ttu-id="1710a-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="1710a-145">Type</span></span>            | <span data-ttu-id="1710a-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1710a-146">System.PerceivedType</span></span>                   | <span data-ttu-id="1710a-147">2</span><span class="sxs-lookup"><span data-stu-id="1710a-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="1710a-148">Contactos</span><span class="sxs-lookup"><span data-stu-id="1710a-148">Contacts</span></span>



| <span data-ttu-id="1710a-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-149">Name</span></span>             | <span data-ttu-id="1710a-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-150">Property</span></span>                           | <span data-ttu-id="1710a-151">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="1710a-152">Nombre de cuenta</span><span class="sxs-lookup"><span data-stu-id="1710a-152">Account Name</span></span>     | <span data-ttu-id="1710a-153">System. Communication. AccountName</span><span class="sxs-lookup"><span data-stu-id="1710a-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="1710a-154">1</span><span class="sxs-lookup"><span data-stu-id="1710a-154">1</span></span>        |
| <span data-ttu-id="1710a-155">Teléfono del trabajo</span><span class="sxs-lookup"><span data-stu-id="1710a-155">Business Phone</span></span>   | <span data-ttu-id="1710a-156">System. contact. BusinessTelephone</span><span class="sxs-lookup"><span data-stu-id="1710a-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="1710a-157">1</span><span class="sxs-lookup"><span data-stu-id="1710a-157">1</span></span>        |
| <span data-ttu-id="1710a-158">Compañía</span><span class="sxs-lookup"><span data-stu-id="1710a-158">Company</span></span>          | <span data-ttu-id="1710a-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="1710a-159">System.Company</span></span>                     | <span data-ttu-id="1710a-160">1</span><span class="sxs-lookup"><span data-stu-id="1710a-160">1</span></span>        |
| <span data-ttu-id="1710a-161">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1710a-161">Email Address</span></span>    | <span data-ttu-id="1710a-162">System. contact. PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1710a-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="1710a-163">1</span><span class="sxs-lookup"><span data-stu-id="1710a-163">1</span></span>        |
| <span data-ttu-id="1710a-164">Importancia</span><span class="sxs-lookup"><span data-stu-id="1710a-164">Importance</span></span>       | <span data-ttu-id="1710a-165">System. ImportanceText</span><span class="sxs-lookup"><span data-stu-id="1710a-165">System.ImportanceText</span></span>              | <span data-ttu-id="1710a-166">1</span><span class="sxs-lookup"><span data-stu-id="1710a-166">1</span></span>        |
| <span data-ttu-id="1710a-167">Teléfono móvil</span><span class="sxs-lookup"><span data-stu-id="1710a-167">Mobile Phone</span></span>     | <span data-ttu-id="1710a-168">System. contact. MobileTelephone</span><span class="sxs-lookup"><span data-stu-id="1710a-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="1710a-169">1</span><span class="sxs-lookup"><span data-stu-id="1710a-169">1</span></span>        |
| <span data-ttu-id="1710a-170">Dirección de la empresa</span><span class="sxs-lookup"><span data-stu-id="1710a-170">Business address</span></span> | <span data-ttu-id="1710a-171">System. contact. BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="1710a-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="1710a-172">2</span><span class="sxs-lookup"><span data-stu-id="1710a-172">2</span></span>        |
| <span data-ttu-id="1710a-173">Fax del trabajo</span><span class="sxs-lookup"><span data-stu-id="1710a-173">Business fax</span></span>     | <span data-ttu-id="1710a-174">System. contact. BusinessFaxNumber</span><span class="sxs-lookup"><span data-stu-id="1710a-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="1710a-175">2</span><span class="sxs-lookup"><span data-stu-id="1710a-175">2</span></span>        |
| <span data-ttu-id="1710a-176">Category</span><span class="sxs-lookup"><span data-stu-id="1710a-176">Category</span></span>         | <span data-ttu-id="1710a-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="1710a-177">System.Category</span></span>                    | <span data-ttu-id="1710a-178">2</span><span class="sxs-lookup"><span data-stu-id="1710a-178">2</span></span>        |
| <span data-ttu-id="1710a-179">Dirección particular</span><span class="sxs-lookup"><span data-stu-id="1710a-179">Home address</span></span>     | <span data-ttu-id="1710a-180">System. contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="1710a-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="1710a-181">2</span><span class="sxs-lookup"><span data-stu-id="1710a-181">2</span></span>        |
| <span data-ttu-id="1710a-182">Teléfono particular</span><span class="sxs-lookup"><span data-stu-id="1710a-182">Home phone</span></span>       | <span data-ttu-id="1710a-183">System. contact. HomeTelephone</span><span class="sxs-lookup"><span data-stu-id="1710a-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="1710a-184">2</span><span class="sxs-lookup"><span data-stu-id="1710a-184">2</span></span>        |
| <span data-ttu-id="1710a-185">Título</span><span class="sxs-lookup"><span data-stu-id="1710a-185">Title</span></span>            | <span data-ttu-id="1710a-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="1710a-186">System.Title</span></span>                       | <span data-ttu-id="1710a-187">2</span><span class="sxs-lookup"><span data-stu-id="1710a-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="1710a-188">Documentos</span><span class="sxs-lookup"><span data-stu-id="1710a-188">Documents</span></span>



| <span data-ttu-id="1710a-189">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-189">Name</span></span>      | <span data-ttu-id="1710a-190">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-190">Property</span></span>             | <span data-ttu-id="1710a-191">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="1710a-192">Authors</span><span class="sxs-lookup"><span data-stu-id="1710a-192">Authors</span></span>   | <span data-ttu-id="1710a-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="1710a-193">System.Author</span></span>        | <span data-ttu-id="1710a-194">1</span><span class="sxs-lookup"><span data-stu-id="1710a-194">1</span></span>        |
| <span data-ttu-id="1710a-195">Texto completo</span><span class="sxs-lookup"><span data-stu-id="1710a-195">Full Text</span></span> | <span data-ttu-id="1710a-196">System. FullText</span><span class="sxs-lookup"><span data-stu-id="1710a-196">System.FullText</span></span>      | <span data-ttu-id="1710a-197">1</span><span class="sxs-lookup"><span data-stu-id="1710a-197">1</span></span>        |
| <span data-ttu-id="1710a-198">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="1710a-198">Tags</span></span>      | <span data-ttu-id="1710a-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="1710a-199">System.Keywords</span></span>      | <span data-ttu-id="1710a-200">1</span><span class="sxs-lookup"><span data-stu-id="1710a-200">1</span></span>        |
| <span data-ttu-id="1710a-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="1710a-201">Type</span></span>      | <span data-ttu-id="1710a-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1710a-202">System.PerceivedType</span></span> | <span data-ttu-id="1710a-203">1</span><span class="sxs-lookup"><span data-stu-id="1710a-203">1</span></span>        |
| <span data-ttu-id="1710a-204">Category</span><span class="sxs-lookup"><span data-stu-id="1710a-204">Category</span></span>  | <span data-ttu-id="1710a-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="1710a-205">System.Category</span></span>      | <span data-ttu-id="1710a-206">2</span><span class="sxs-lookup"><span data-stu-id="1710a-206">2</span></span>        |
| <span data-ttu-id="1710a-207">Título</span><span class="sxs-lookup"><span data-stu-id="1710a-207">Title</span></span>     | <span data-ttu-id="1710a-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="1710a-208">System.Title</span></span>         | <span data-ttu-id="1710a-209">2</span><span class="sxs-lookup"><span data-stu-id="1710a-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="1710a-210">Genérico</span><span class="sxs-lookup"><span data-stu-id="1710a-210">Generic</span></span>



| <span data-ttu-id="1710a-211">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-211">Name</span></span>     | <span data-ttu-id="1710a-212">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-212">Property</span></span>             | <span data-ttu-id="1710a-213">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="1710a-214">Authors</span><span class="sxs-lookup"><span data-stu-id="1710a-214">Authors</span></span>  | <span data-ttu-id="1710a-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="1710a-215">System.Author</span></span>        | <span data-ttu-id="1710a-216">1</span><span class="sxs-lookup"><span data-stu-id="1710a-216">1</span></span>        |
| <span data-ttu-id="1710a-217">Title</span><span class="sxs-lookup"><span data-stu-id="1710a-217">Title</span></span>    | <span data-ttu-id="1710a-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="1710a-218">System.Title</span></span>         | <span data-ttu-id="1710a-219">1</span><span class="sxs-lookup"><span data-stu-id="1710a-219">1</span></span>        |
| <span data-ttu-id="1710a-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="1710a-220">Type</span></span>     | <span data-ttu-id="1710a-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1710a-221">System.PerceivedType</span></span> | <span data-ttu-id="1710a-222">1</span><span class="sxs-lookup"><span data-stu-id="1710a-222">1</span></span>        |
| <span data-ttu-id="1710a-223">Category</span><span class="sxs-lookup"><span data-stu-id="1710a-223">Category</span></span> | <span data-ttu-id="1710a-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="1710a-224">System.Category</span></span>      | <span data-ttu-id="1710a-225">2</span><span class="sxs-lookup"><span data-stu-id="1710a-225">2</span></span>        |
| <span data-ttu-id="1710a-226">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="1710a-226">Tags</span></span>     | <span data-ttu-id="1710a-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="1710a-227">System.Keywords</span></span>      | <span data-ttu-id="1710a-228">2</span><span class="sxs-lookup"><span data-stu-id="1710a-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="1710a-229">Música</span><span class="sxs-lookup"><span data-stu-id="1710a-229">Music</span></span>



| <span data-ttu-id="1710a-230">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-230">Name</span></span>         | <span data-ttu-id="1710a-231">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-231">Property</span></span>                     | <span data-ttu-id="1710a-232">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="1710a-233">System. Music. TrackNumber</span><span class="sxs-lookup"><span data-stu-id="1710a-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="1710a-234">1</span><span class="sxs-lookup"><span data-stu-id="1710a-234">1</span></span>        |
| <span data-ttu-id="1710a-235">Álbum</span><span class="sxs-lookup"><span data-stu-id="1710a-235">Album</span></span>        | <span data-ttu-id="1710a-236">System. Music. álbum</span><span class="sxs-lookup"><span data-stu-id="1710a-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="1710a-237">1</span><span class="sxs-lookup"><span data-stu-id="1710a-237">1</span></span>        |
| <span data-ttu-id="1710a-238">Intérprete</span><span class="sxs-lookup"><span data-stu-id="1710a-238">Artists</span></span>      | <span data-ttu-id="1710a-239">System. Music. artista</span><span class="sxs-lookup"><span data-stu-id="1710a-239">System.Music.Artist</span></span>          | <span data-ttu-id="1710a-240">1</span><span class="sxs-lookup"><span data-stu-id="1710a-240">1</span></span>        |
| <span data-ttu-id="1710a-241">Género</span><span class="sxs-lookup"><span data-stu-id="1710a-241">Genre</span></span>        | <span data-ttu-id="1710a-242">System. Music. Genre</span><span class="sxs-lookup"><span data-stu-id="1710a-242">System.Music.Genre</span></span>           | <span data-ttu-id="1710a-243">1</span><span class="sxs-lookup"><span data-stu-id="1710a-243">1</span></span>        |
| <span data-ttu-id="1710a-244">Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-244">Rating</span></span>       | <span data-ttu-id="1710a-245">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-245">System.Rating</span></span>                | <span data-ttu-id="1710a-246">1</span><span class="sxs-lookup"><span data-stu-id="1710a-246">1</span></span>        |
| <span data-ttu-id="1710a-247">Title</span><span class="sxs-lookup"><span data-stu-id="1710a-247">Title</span></span>        | <span data-ttu-id="1710a-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="1710a-248">System.Title</span></span>                 | <span data-ttu-id="1710a-249">1</span><span class="sxs-lookup"><span data-stu-id="1710a-249">1</span></span>        |
| <span data-ttu-id="1710a-250">Intérprete del álbum</span><span class="sxs-lookup"><span data-stu-id="1710a-250">Album Artist</span></span> | <span data-ttu-id="1710a-251">System. Music. AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="1710a-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="1710a-252">2</span><span class="sxs-lookup"><span data-stu-id="1710a-252">2</span></span>        |
| <span data-ttu-id="1710a-253">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="1710a-253">Bit Rate</span></span>     | <span data-ttu-id="1710a-254">System. audio. EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="1710a-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="1710a-255">2</span><span class="sxs-lookup"><span data-stu-id="1710a-255">2</span></span>        |
| <span data-ttu-id="1710a-256">Conductores</span><span class="sxs-lookup"><span data-stu-id="1710a-256">Conductors</span></span>   | <span data-ttu-id="1710a-257">System. Music. conductores</span><span class="sxs-lookup"><span data-stu-id="1710a-257">System.Music.Conductor</span></span>       | <span data-ttu-id="1710a-258">2</span><span class="sxs-lookup"><span data-stu-id="1710a-258">2</span></span>        |
| <span data-ttu-id="1710a-259">Length</span><span class="sxs-lookup"><span data-stu-id="1710a-259">Length</span></span>       | <span data-ttu-id="1710a-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="1710a-260">System.Media.Duration</span></span>        | <span data-ttu-id="1710a-261">2</span><span class="sxs-lookup"><span data-stu-id="1710a-261">2</span></span>        |
| <span data-ttu-id="1710a-262">Protegido</span><span class="sxs-lookup"><span data-stu-id="1710a-262">Protected</span></span>    | <span data-ttu-id="1710a-263">System. DRM. IsProtected</span><span class="sxs-lookup"><span data-stu-id="1710a-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="1710a-264">2</span><span class="sxs-lookup"><span data-stu-id="1710a-264">2</span></span>        |
| <span data-ttu-id="1710a-265">Year</span><span class="sxs-lookup"><span data-stu-id="1710a-265">Year</span></span>         | <span data-ttu-id="1710a-266">System. Media. Year</span><span class="sxs-lookup"><span data-stu-id="1710a-266">System.Media.Year</span></span>            | <span data-ttu-id="1710a-267">2</span><span class="sxs-lookup"><span data-stu-id="1710a-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="1710a-268">Imágenes</span><span class="sxs-lookup"><span data-stu-id="1710a-268">Pictures</span></span>



| <span data-ttu-id="1710a-269">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-269">Name</span></span>          | <span data-ttu-id="1710a-270">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-270">Property</span></span>                        | <span data-ttu-id="1710a-271">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="1710a-272">Fecha de importación</span><span class="sxs-lookup"><span data-stu-id="1710a-272">Date imported</span></span> | <span data-ttu-id="1710a-273">System. DateImported</span><span class="sxs-lookup"><span data-stu-id="1710a-273">System.DateImported</span></span>             | <span data-ttu-id="1710a-274">1</span><span class="sxs-lookup"><span data-stu-id="1710a-274">1</span></span>        |
| <span data-ttu-id="1710a-275">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="1710a-275">Date Taken</span></span>    | <span data-ttu-id="1710a-276">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="1710a-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="1710a-277">1</span><span class="sxs-lookup"><span data-stu-id="1710a-277">1</span></span>        |
| <span data-ttu-id="1710a-278">Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-278">Rating</span></span>        | <span data-ttu-id="1710a-279">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-279">System.Rating</span></span>                   | <span data-ttu-id="1710a-280">1</span><span class="sxs-lookup"><span data-stu-id="1710a-280">1</span></span>        |
| <span data-ttu-id="1710a-281">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="1710a-281">Tags</span></span>          | <span data-ttu-id="1710a-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="1710a-282">System.Keywords</span></span>                 | <span data-ttu-id="1710a-283">1</span><span class="sxs-lookup"><span data-stu-id="1710a-283">1</span></span>        |
| <span data-ttu-id="1710a-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="1710a-284">Type</span></span>          | <span data-ttu-id="1710a-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1710a-285">System.PerceivedType</span></span>            | <span data-ttu-id="1710a-286">1</span><span class="sxs-lookup"><span data-stu-id="1710a-286">1</span></span>        |
| <span data-ttu-id="1710a-287">Authors</span><span class="sxs-lookup"><span data-stu-id="1710a-287">Authors</span></span>       | <span data-ttu-id="1710a-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="1710a-288">System.Author</span></span>                   | <span data-ttu-id="1710a-289">2</span><span class="sxs-lookup"><span data-stu-id="1710a-289">2</span></span>        |
| <span data-ttu-id="1710a-290">Creador de cámara</span><span class="sxs-lookup"><span data-stu-id="1710a-290">Camera maker</span></span>  | <span data-ttu-id="1710a-291">System. Photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="1710a-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="1710a-292">2</span><span class="sxs-lookup"><span data-stu-id="1710a-292">2</span></span>        |
| <span data-ttu-id="1710a-293">Modelo de cámara</span><span class="sxs-lookup"><span data-stu-id="1710a-293">Camera model</span></span>  | <span data-ttu-id="1710a-294">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="1710a-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="1710a-295">2</span><span class="sxs-lookup"><span data-stu-id="1710a-295">2</span></span>        |
| <span data-ttu-id="1710a-296">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1710a-296">Comments</span></span>      | <span data-ttu-id="1710a-297">System. Comment</span><span class="sxs-lookup"><span data-stu-id="1710a-297">System.Comment</span></span>                  | <span data-ttu-id="1710a-298">2</span><span class="sxs-lookup"><span data-stu-id="1710a-298">2</span></span>        |
| <span data-ttu-id="1710a-299">Dimensions</span><span class="sxs-lookup"><span data-stu-id="1710a-299">Dimensions</span></span>    | <span data-ttu-id="1710a-300">System. Image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="1710a-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="1710a-301">2</span><span class="sxs-lookup"><span data-stu-id="1710a-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="1710a-302">Vídeos</span><span class="sxs-lookup"><span data-stu-id="1710a-302">Videos</span></span>



| <span data-ttu-id="1710a-303">Nombre</span><span class="sxs-lookup"><span data-stu-id="1710a-303">Name</span></span>         | <span data-ttu-id="1710a-304">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1710a-304">Property</span></span>                 | <span data-ttu-id="1710a-305">Prioridad</span><span class="sxs-lookup"><span data-stu-id="1710a-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="1710a-306">Length</span><span class="sxs-lookup"><span data-stu-id="1710a-306">Length</span></span>       | <span data-ttu-id="1710a-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="1710a-307">System.Media.Duration</span></span>    | <span data-ttu-id="1710a-308">1</span><span class="sxs-lookup"><span data-stu-id="1710a-308">1</span></span>        |
| <span data-ttu-id="1710a-309">Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-309">Rating</span></span>       | <span data-ttu-id="1710a-310">System. Rating</span><span class="sxs-lookup"><span data-stu-id="1710a-310">System.Rating</span></span>            | <span data-ttu-id="1710a-311">1</span><span class="sxs-lookup"><span data-stu-id="1710a-311">1</span></span>        |
| <span data-ttu-id="1710a-312">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="1710a-312">Tags</span></span>         | <span data-ttu-id="1710a-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="1710a-313">System.Keywords</span></span>          | <span data-ttu-id="1710a-314">1</span><span class="sxs-lookup"><span data-stu-id="1710a-314">1</span></span>        |
| <span data-ttu-id="1710a-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="1710a-315">Type</span></span>         | <span data-ttu-id="1710a-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1710a-316">System.PerceivedType</span></span>     | <span data-ttu-id="1710a-317">1</span><span class="sxs-lookup"><span data-stu-id="1710a-317">1</span></span>        |
| <span data-ttu-id="1710a-318">Alto de marco</span><span class="sxs-lookup"><span data-stu-id="1710a-318">Frame height</span></span> | <span data-ttu-id="1710a-319">System. video. FrameHeight</span><span class="sxs-lookup"><span data-stu-id="1710a-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="1710a-320">2</span><span class="sxs-lookup"><span data-stu-id="1710a-320">2</span></span>        |
| <span data-ttu-id="1710a-321">Ancho de marco</span><span class="sxs-lookup"><span data-stu-id="1710a-321">Frame width</span></span>  | <span data-ttu-id="1710a-322">System. video. FrameWidth</span><span class="sxs-lookup"><span data-stu-id="1710a-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="1710a-323">2</span><span class="sxs-lookup"><span data-stu-id="1710a-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1710a-324">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1710a-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1710a-325">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1710a-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1710a-326">Desarrollar controladores de propiedades para Windows Search</span><span class="sxs-lookup"><span data-stu-id="1710a-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="1710a-327">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="1710a-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1710a-328">Sistema de propiedades</span><span class="sxs-lookup"><span data-stu-id="1710a-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="1710a-329">[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="1710a-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
