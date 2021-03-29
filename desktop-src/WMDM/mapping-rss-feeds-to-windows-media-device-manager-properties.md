---
title: Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media
description: Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Administrador de dispositivos, fuentes RSS
- Administrador de dispositivos, fuentes RSS
- Guía de programación, fuentes RSS
- aplicaciones de escritorio, fuentes RSS
- crear aplicaciones de Windows Media Administrador de dispositivos, fuentes RSS
- Fuentes RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903188"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="6d36a-109">Asignar fuentes RSS a propiedades de Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6d36a-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="6d36a-110">Windows Media Player 11 proporciona una característica de agregador RSS que permite a los usuarios almacenar contenido obtenido de podcasts en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="6d36a-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="6d36a-111">En este tema se describen los elementos XML que se encuentran en una fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="6d36a-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="6d36a-112">Además, asigna estos elementos RSS a las propiedades de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6d36a-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="6d36a-113">Los elementos de una fuente RSS tienen la jerarquía y los atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6d36a-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="6d36a-114">En la tabla siguiente se enumeran los elementos de canal en una fuente RSS y las propiedades correspondientes de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6d36a-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="6d36a-115">Elemento Channel</span><span class="sxs-lookup"><span data-stu-id="6d36a-115">Channel element</span></span> | <span data-ttu-id="6d36a-116">Status</span><span class="sxs-lookup"><span data-stu-id="6d36a-116">Status</span></span>         | <span data-ttu-id="6d36a-117">Propiedad de Administrador de dispositivos de Windows Media correspondiente</span><span class="sxs-lookup"><span data-stu-id="6d36a-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="6d36a-118">category</span><span class="sxs-lookup"><span data-stu-id="6d36a-118">category</span></span>        | <span data-ttu-id="6d36a-119">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-119">Optional</span></span>       | [<span data-ttu-id="6d36a-120">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="6d36a-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="6d36a-121">cloud</span><span class="sxs-lookup"><span data-stu-id="6d36a-121">cloud</span></span>           | <span data-ttu-id="6d36a-122">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-122">Not applicable</span></span> | <span data-ttu-id="6d36a-123">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-123">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-124">copyright</span><span class="sxs-lookup"><span data-stu-id="6d36a-124">copyright</span></span>       | <span data-ttu-id="6d36a-125">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-125">Optional</span></span>       | [<span data-ttu-id="6d36a-126">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="6d36a-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="6d36a-127">description</span><span class="sxs-lookup"><span data-stu-id="6d36a-127">description</span></span>     | <span data-ttu-id="6d36a-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-128">Required</span></span>       | [<span data-ttu-id="6d36a-129">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6d36a-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="6d36a-130">Documentación</span><span class="sxs-lookup"><span data-stu-id="6d36a-130">docs</span></span>            | <span data-ttu-id="6d36a-131">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-131">Not applicable</span></span> | <span data-ttu-id="6d36a-132">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-132">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-133">generador</span><span class="sxs-lookup"><span data-stu-id="6d36a-133">generator</span></span>       | <span data-ttu-id="6d36a-134">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-134">Not applicable</span></span> | <span data-ttu-id="6d36a-135">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-135">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-136">language</span><span class="sxs-lookup"><span data-stu-id="6d36a-136">language</span></span>        | <span data-ttu-id="6d36a-137">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-137">Not applicable</span></span> | <span data-ttu-id="6d36a-138">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-138">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-139">lastBuildDate</span></span>   | <span data-ttu-id="6d36a-140">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-140">Optional</span></span>       | [<span data-ttu-id="6d36a-141">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="6d36a-142">link</span><span class="sxs-lookup"><span data-stu-id="6d36a-142">link</span></span>            | <span data-ttu-id="6d36a-143">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-143">Required</span></span>       | [<span data-ttu-id="6d36a-144">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="6d36a-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="6d36a-145">managingEditor</span></span>  | <span data-ttu-id="6d36a-146">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-146">Optional</span></span>       | [<span data-ttu-id="6d36a-147">g \_ wszWMDMEditor</span><span class="sxs-lookup"><span data-stu-id="6d36a-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="6d36a-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-148">pubDate</span></span>         | <span data-ttu-id="6d36a-149">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-149">Optional</span></span>       | [<span data-ttu-id="6d36a-150">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="6d36a-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="6d36a-151">rating</span><span class="sxs-lookup"><span data-stu-id="6d36a-151">rating</span></span>          | <span data-ttu-id="6d36a-152">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-152">Not applicable</span></span> | <span data-ttu-id="6d36a-153">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-153">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-154">skipDays</span><span class="sxs-lookup"><span data-stu-id="6d36a-154">skipDays</span></span>        | <span data-ttu-id="6d36a-155">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-155">Not applicable</span></span> | <span data-ttu-id="6d36a-156">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-156">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-157">skipHours</span><span class="sxs-lookup"><span data-stu-id="6d36a-157">skipHours</span></span>       | <span data-ttu-id="6d36a-158">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-158">Not applicable</span></span> | <span data-ttu-id="6d36a-159">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-159">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-160">textInput</span><span class="sxs-lookup"><span data-stu-id="6d36a-160">textInput</span></span>       | <span data-ttu-id="6d36a-161">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-161">Not applicable</span></span> | <span data-ttu-id="6d36a-162">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-162">Not applicable</span></span>                                        |
| <span data-ttu-id="6d36a-163">title</span><span class="sxs-lookup"><span data-stu-id="6d36a-163">title</span></span>           | <span data-ttu-id="6d36a-164">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-164">Required</span></span>       | [<span data-ttu-id="6d36a-165">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="6d36a-166">ttl</span><span class="sxs-lookup"><span data-stu-id="6d36a-166">ttl</span></span>             | <span data-ttu-id="6d36a-167">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-167">Optional</span></span>       | [<span data-ttu-id="6d36a-168">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="6d36a-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="6d36a-169">webmaster</span><span class="sxs-lookup"><span data-stu-id="6d36a-169">webMaster</span></span>       | <span data-ttu-id="6d36a-170">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-170">Optional</span></span>       | [<span data-ttu-id="6d36a-171">g \_ wszWMDMWebMaster</span><span class="sxs-lookup"><span data-stu-id="6d36a-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="6d36a-172">En la tabla siguiente se enumeran los elementos de imagen de una fuente RSS y las propiedades de WMDM correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6d36a-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="6d36a-173">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="6d36a-173">Image element</span></span> | <span data-ttu-id="6d36a-174">Status</span><span class="sxs-lookup"><span data-stu-id="6d36a-174">Status</span></span>   | <span data-ttu-id="6d36a-175">Propiedad de Administrador de dispositivos de Windows Media correspondiente</span><span class="sxs-lookup"><span data-stu-id="6d36a-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="6d36a-176">description</span><span class="sxs-lookup"><span data-stu-id="6d36a-176">description</span></span>   | <span data-ttu-id="6d36a-177">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-177">Optional</span></span> | [<span data-ttu-id="6d36a-178">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6d36a-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="6d36a-179">height</span><span class="sxs-lookup"><span data-stu-id="6d36a-179">height</span></span>        | <span data-ttu-id="6d36a-180">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-180">Optional</span></span> | [<span data-ttu-id="6d36a-181">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="6d36a-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="6d36a-182">link</span><span class="sxs-lookup"><span data-stu-id="6d36a-182">link</span></span>          | <span data-ttu-id="6d36a-183">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-183">Optional</span></span> | [<span data-ttu-id="6d36a-184">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="6d36a-185">title</span><span class="sxs-lookup"><span data-stu-id="6d36a-185">title</span></span>         | <span data-ttu-id="6d36a-186">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-186">Optional</span></span> | [<span data-ttu-id="6d36a-187">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="6d36a-188">url</span><span class="sxs-lookup"><span data-stu-id="6d36a-188">url</span></span>           | <span data-ttu-id="6d36a-189">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-189">Optional</span></span> | [<span data-ttu-id="6d36a-190">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="6d36a-191">width</span><span class="sxs-lookup"><span data-stu-id="6d36a-191">width</span></span>         | <span data-ttu-id="6d36a-192">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-192">Optional</span></span> | [<span data-ttu-id="6d36a-193">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="6d36a-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="6d36a-194">En la tabla siguiente se enumeran los elementos de elemento de una fuente RSS y las propiedades correspondientes de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6d36a-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="6d36a-195">Elemento Item</span><span class="sxs-lookup"><span data-stu-id="6d36a-195">Item element</span></span> | <span data-ttu-id="6d36a-196">Atributo</span><span class="sxs-lookup"><span data-stu-id="6d36a-196">Attribute</span></span>   | <span data-ttu-id="6d36a-197">Status</span><span class="sxs-lookup"><span data-stu-id="6d36a-197">Status</span></span>         | <span data-ttu-id="6d36a-198">Propiedad de Administrador de dispositivos de Windows Media correspondiente</span><span class="sxs-lookup"><span data-stu-id="6d36a-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="6d36a-199">autor</span><span class="sxs-lookup"><span data-stu-id="6d36a-199">author</span></span>       |             | <span data-ttu-id="6d36a-200">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-200">Optional</span></span>       | [<span data-ttu-id="6d36a-201">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="6d36a-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="6d36a-202">category</span><span class="sxs-lookup"><span data-stu-id="6d36a-202">category</span></span>     |             | <span data-ttu-id="6d36a-203">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-203">Optional</span></span>       | [<span data-ttu-id="6d36a-204">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="6d36a-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="6d36a-205">dominio</span><span class="sxs-lookup"><span data-stu-id="6d36a-205">domain</span></span>      | <span data-ttu-id="6d36a-206">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-206">Not applicable</span></span> | <span data-ttu-id="6d36a-207">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="6d36a-208">description</span><span class="sxs-lookup"><span data-stu-id="6d36a-208">description</span></span>  |             | <span data-ttu-id="6d36a-209">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-209">Optional</span></span>       | [<span data-ttu-id="6d36a-210">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6d36a-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="6d36a-211">caja</span><span class="sxs-lookup"><span data-stu-id="6d36a-211">enclosure</span></span>    |             | <span data-ttu-id="6d36a-212">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-212">Optional</span></span>       | <span data-ttu-id="6d36a-213">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="6d36a-214">length</span><span class="sxs-lookup"><span data-stu-id="6d36a-214">length</span></span>      | <span data-ttu-id="6d36a-215">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-215">Required</span></span>       | [<span data-ttu-id="6d36a-216">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="6d36a-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="6d36a-217">type</span><span class="sxs-lookup"><span data-stu-id="6d36a-217">type</span></span>        | <span data-ttu-id="6d36a-218">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-218">Required</span></span>       | <span data-ttu-id="6d36a-219">(El tipo MIME debe asignarse al tipo de contenido de la propiedad).</span><span class="sxs-lookup"><span data-stu-id="6d36a-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="6d36a-220">url</span><span class="sxs-lookup"><span data-stu-id="6d36a-220">url</span></span>         | <span data-ttu-id="6d36a-221">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6d36a-221">Required</span></span>       | [<span data-ttu-id="6d36a-222">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="6d36a-223">guid</span><span class="sxs-lookup"><span data-stu-id="6d36a-223">guid</span></span>         |             | <span data-ttu-id="6d36a-224">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-224">Optional</span></span>       | [<span data-ttu-id="6d36a-225">g \_ wszWMDMediaGuid</span><span class="sxs-lookup"><span data-stu-id="6d36a-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="6d36a-226">isPermaLink</span><span class="sxs-lookup"><span data-stu-id="6d36a-226">isPermaLink</span></span> | <span data-ttu-id="6d36a-227">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-227">Not applicable</span></span> | <span data-ttu-id="6d36a-228">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="6d36a-229">link</span><span class="sxs-lookup"><span data-stu-id="6d36a-229">link</span></span>         |             | <span data-ttu-id="6d36a-230">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-230">Optional</span></span>       | [<span data-ttu-id="6d36a-231">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="6d36a-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-232">pubDate</span></span>      |             | <span data-ttu-id="6d36a-233">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-233">Optional</span></span>       | [<span data-ttu-id="6d36a-234">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="6d36a-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="6d36a-235">source</span><span class="sxs-lookup"><span data-stu-id="6d36a-235">source</span></span>       |             | <span data-ttu-id="6d36a-236">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-236">Not applicable</span></span> | <span data-ttu-id="6d36a-237">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6d36a-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="6d36a-238">title</span><span class="sxs-lookup"><span data-stu-id="6d36a-238">title</span></span>        |             | <span data-ttu-id="6d36a-239">Opcionales</span><span class="sxs-lookup"><span data-stu-id="6d36a-239">Optional</span></span>       | [<span data-ttu-id="6d36a-240">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="6d36a-241">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d36a-241">Example</span></span>

<span data-ttu-id="6d36a-242">En el ejemplo siguiente se muestra una fuente RSS completa para un podcast ficticio proporcionado por el CEO de una empresa de publicación.</span><span class="sxs-lookup"><span data-stu-id="6d36a-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="6d36a-243">Asignación de elementos de canal RSS a Windows Media Administrador de dispositivos valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d36a-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="6d36a-244">En la tabla siguiente se describe cómo se asignan los valores de los elementos de canal RSS en el ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6d36a-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="6d36a-245">Propiedad Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6d36a-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="6d36a-246">Value</span><span class="sxs-lookup"><span data-stu-id="6d36a-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d36a-247">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="6d36a-248">Vie, 9 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="6d36a-249">g \_ wszWMDMDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d36a-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="6d36a-250">Lucerne Publishing CEO Peter Bankov examina las últimas tendencias de las publicaciones en línea.</span><span class="sxs-lookup"><span data-stu-id="6d36a-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="6d36a-251">\_ \_ dirección URL de g wszWMDMDESTINATION</span><span class="sxs-lookup"><span data-stu-id="6d36a-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="6d36a-252">g \_ wszWMDMEDITOR</span><span class="sxs-lookup"><span data-stu-id="6d36a-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="6d36a-253">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="6d36a-254">Vie, 9 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="6d36a-255">g \_ wszWMDMFileName</span><span class="sxs-lookup"><span data-stu-id="6d36a-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="6d36a-256">La publicación digital</span><span class="sxs-lookup"><span data-stu-id="6d36a-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="6d36a-257">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="6d36a-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="6d36a-258">13.790</span><span class="sxs-lookup"><span data-stu-id="6d36a-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="6d36a-259">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="6d36a-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="6d36a-260">\_ \_ conversión multimedia FORMATCODE de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="6d36a-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="6d36a-261">g \_ wszWMDMGENRE</span><span class="sxs-lookup"><span data-stu-id="6d36a-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="6d36a-262">Noticias</span><span class="sxs-lookup"><span data-stu-id="6d36a-262">News</span></span>                                                                                          |
| [<span data-ttu-id="6d36a-263">g \_ wszWMDMLAST \_ fecha de modificación \_</span><span class="sxs-lookup"><span data-stu-id="6d36a-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="6d36a-264">Vie, 9 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="6d36a-265">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="6d36a-266">Vie, 9 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="6d36a-267">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="6d36a-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="6d36a-268">2006 Lucerne Publishing LP, LLLP.</span><span class="sxs-lookup"><span data-stu-id="6d36a-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="6d36a-269">All Rights Reserved.</span><span class="sxs-lookup"><span data-stu-id="6d36a-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="6d36a-270">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="6d36a-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="6d36a-271">240</span><span class="sxs-lookup"><span data-stu-id="6d36a-271">240</span></span>                                                                                           |
| [<span data-ttu-id="6d36a-272">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="6d36a-273">La publicación digital</span><span class="sxs-lookup"><span data-stu-id="6d36a-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="6d36a-274">g \_ wszWMDMWEBMASTER</span><span class="sxs-lookup"><span data-stu-id="6d36a-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="6d36a-275">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="6d36a-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="6d36a-276">Vie, 9 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="6d36a-277">Asignación de elementos de imagen RSS a Windows Media Administrador de dispositivos valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d36a-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="6d36a-278">En la tabla siguiente se describe cómo se asignan los valores de los elementos de imagen RSS en el ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6d36a-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="6d36a-279">Propiedad Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6d36a-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="6d36a-280">Value</span><span class="sxs-lookup"><span data-stu-id="6d36a-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="6d36a-281">g \_ wszWMDMAlbumCoverFormat</span><span class="sxs-lookup"><span data-stu-id="6d36a-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="6d36a-282">\_formato de objeto WPD \_ \_ GIF</span><span class="sxs-lookup"><span data-stu-id="6d36a-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="6d36a-283">g \_ wszWMDMAlbumCoverSize</span><span class="sxs-lookup"><span data-stu-id="6d36a-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="6d36a-284">512</span><span class="sxs-lookup"><span data-stu-id="6d36a-284">512</span></span>                                              |
| [<span data-ttu-id="6d36a-285">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6d36a-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="6d36a-286">Logotipo de Lucerne</span><span class="sxs-lookup"><span data-stu-id="6d36a-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="6d36a-287">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="6d36a-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="6d36a-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="6d36a-289">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="6d36a-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="6d36a-290">300</span><span class="sxs-lookup"><span data-stu-id="6d36a-290">300</span></span>                                              |
| [<span data-ttu-id="6d36a-291">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="6d36a-292">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="6d36a-293">Publicación de Lucerne</span><span class="sxs-lookup"><span data-stu-id="6d36a-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="6d36a-294">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="6d36a-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="6d36a-295">300</span><span class="sxs-lookup"><span data-stu-id="6d36a-295">300</span></span>                                              |



 

<span data-ttu-id="6d36a-296">Asignación de elementos RSS Item a Windows Media Administrador de dispositivos valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d36a-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="6d36a-297">En la tabla siguiente se describe cómo se asignan los valores de los elementos RSS del ejemplo anterior a determinadas propiedades de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6d36a-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="6d36a-298">Propiedad Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6d36a-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="6d36a-299">Value</span><span class="sxs-lookup"><span data-stu-id="6d36a-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d36a-300">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="6d36a-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="6d36a-301">Lucerne</span><span class="sxs-lookup"><span data-stu-id="6d36a-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="6d36a-302">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="6d36a-303">Jue, 1 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="6d36a-304">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6d36a-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="6d36a-305">Las publicaciones en línea cambian rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6d36a-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="6d36a-306">El CEO de un centro de publicaciones examina las tendencias de los últimos cinco años y sus implicaciones.</span><span class="sxs-lookup"><span data-stu-id="6d36a-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="6d36a-307">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="6d36a-308">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="6d36a-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="6d36a-309">120325445</span><span class="sxs-lookup"><span data-stu-id="6d36a-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="6d36a-310">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="6d36a-311">Jue, 1 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="6d36a-312">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="6d36a-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="6d36a-313">10329011</span><span class="sxs-lookup"><span data-stu-id="6d36a-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="6d36a-314">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="6d36a-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="6d36a-315">\_Mp3 FORMATCODE de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="6d36a-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="6d36a-316">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="6d36a-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="6d36a-317">Noticias</span><span class="sxs-lookup"><span data-stu-id="6d36a-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="6d36a-318">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="6d36a-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="6d36a-319">Jue, 1 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="6d36a-320">g \_ wszWMDMMediaGuid</span><span class="sxs-lookup"><span data-stu-id="6d36a-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="6d36a-321">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="6d36a-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="6d36a-322">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6d36a-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="6d36a-323">La publicación digital</span><span class="sxs-lookup"><span data-stu-id="6d36a-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="6d36a-324">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="6d36a-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="6d36a-325">Jue, 1 de junio 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="6d36a-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6d36a-326">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d36a-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d36a-327">**Constantes de metadatos**</span><span class="sxs-lookup"><span data-stu-id="6d36a-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




