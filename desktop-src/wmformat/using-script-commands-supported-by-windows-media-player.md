---
title: Usar comandos de script compatibles con Windows Media Player
description: Usar comandos de script compatibles con Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- SDK de Windows Media Format, comandos de script
- SDK de Windows Media Format, Windows Media Player
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- Advanced Systems Format (ASF), Windows Media Player
- ASF (formato de sistemas avanzados), Windows Media Player
- scripts, comandos
- scripts, Media Player de Windows
- Reproductor de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075806"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="894f3-112">Usar comandos de script compatibles con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="894f3-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="894f3-113">El SDK de Windows Media Format no proporciona compatibilidad nativa para el análisis y la respuesta a los comandos de script.</span><span class="sxs-lookup"><span data-stu-id="894f3-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="894f3-114">Debe incluir cualquier lógica relacionada con los comandos de script en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="894f3-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="894f3-115">Los tipos de script que se usan también deben definirse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="894f3-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="894f3-116">Puede incluir código para controlar los mismos comandos de script que se admiten en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="894f3-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="894f3-117">Mantener la compatibilidad con Windows Media Player hace que los archivos sean más universales que si se incrustan comandos de script personalizados.</span><span class="sxs-lookup"><span data-stu-id="894f3-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="894f3-118">En la tabla siguiente se enumeran los tipos de scripts compatibles con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="894f3-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="894f3-119">Tipo de script</span><span class="sxs-lookup"><span data-stu-id="894f3-119">Script type</span></span> | <span data-ttu-id="894f3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="894f3-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="894f3-121">URL</span><span class="sxs-lookup"><span data-stu-id="894f3-121">URL</span></span>         | <span data-ttu-id="894f3-122">El reproductor envía la dirección URL especificada al explorador para mostrarla al usuario.</span><span class="sxs-lookup"><span data-stu-id="894f3-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="894f3-123">Si se utiliza un control de reproductor incrustado, puede Agregar una referencia de marco específica a la dirección URL mediante la sintaxis de &&*FrameName* .</span><span class="sxs-lookup"><span data-stu-id="894f3-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="894f3-124">EXTENSIÓN</span><span class="sxs-lookup"><span data-stu-id="894f3-124">FILENAME</span></span>    | <span data-ttu-id="894f3-125">Una dirección URL a otro archivo multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="894f3-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="894f3-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="894f3-126">CAPTION</span></span>     | <span data-ttu-id="894f3-127">Cadena de texto que se muestra en el área de título de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="894f3-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="894f3-128">Este tipo admite el formato HTML estándar, por lo que el texto puede tener el formato que desee.</span><span class="sxs-lookup"><span data-stu-id="894f3-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="894f3-129">Un ejemplo de uso es el subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="894f3-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="894f3-130">CESO</span><span class="sxs-lookup"><span data-stu-id="894f3-130">EVENT</span></span>       | <span data-ttu-id="894f3-131">Nombre de un evento que se va a producir.</span><span class="sxs-lookup"><span data-stu-id="894f3-131">The name of an event that is to occur.</span></span> <span data-ttu-id="894f3-132">El tipo de evento admite la personalización para sus propios usos.</span><span class="sxs-lookup"><span data-stu-id="894f3-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="894f3-133">El código para el evento especificado debe definirse en el metarchivo de Windows Media para la secuencia con el fin de que el reproductor realice el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="894f3-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="894f3-134">Un ejemplo de uso es la inserción de anuncios.</span><span class="sxs-lookup"><span data-stu-id="894f3-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="894f3-135">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="894f3-135">OPENEVENT</span></span>   | <span data-ttu-id="894f3-136">Este script precede al evento real.</span><span class="sxs-lookup"><span data-stu-id="894f3-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="894f3-137">El OPENEVENT permite que el reproductor almacene previamente el contenido de modo que, cuando se produzca el evento, el cambio entre las secuencias parezca que sea sencillo.</span><span class="sxs-lookup"><span data-stu-id="894f3-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="894f3-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="894f3-138">TEXT</span></span>        | <span data-ttu-id="894f3-139">Cadena de texto que se muestra en el área de título de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="894f3-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="894f3-140">Puede ser texto sin formato, SAMI o texto con formato HTML.</span><span class="sxs-lookup"><span data-stu-id="894f3-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="894f3-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="894f3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="894f3-142">**Usar comandos de script**</span><span class="sxs-lookup"><span data-stu-id="894f3-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




