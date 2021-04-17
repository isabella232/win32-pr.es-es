---
title: EVENT (elemento, WMP SDK)
description: El elemento de evento define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Elemento de evento Media Player de Windows
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698678"
---
# <a name="event-element"></a><span data-ttu-id="b4cad-104">Elemento EVENT</span><span class="sxs-lookup"><span data-stu-id="b4cad-104">EVENT Element</span></span>

<span data-ttu-id="b4cad-105">El elemento de **evento** define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="b4cad-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4cad-106">Attributes</span></span>

<span data-ttu-id="b4cad-107">**Nombre** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="b4cad-107">**NAME** (required)</span></span>

<span data-ttu-id="b4cad-108">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-108">The name of the event.</span></span>

<span data-ttu-id="b4cad-109">**WHENDONE** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="b4cad-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="b4cad-110">Valor que define qué hace Windows Media Player después de reproducir el contenido al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="b4cad-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="b4cad-111">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="b4cad-111">The following values are possible.</span></span>



| <span data-ttu-id="b4cad-112">Value</span><span class="sxs-lookup"><span data-stu-id="b4cad-112">Value</span></span>  | <span data-ttu-id="b4cad-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4cad-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cad-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="b4cad-114">RESUME</span></span> | <span data-ttu-id="b4cad-115">La entrada actual (el clip interrumpido por el evento) se reanuda la reproducción.</span><span class="sxs-lookup"><span data-stu-id="b4cad-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="b4cad-116">Si el contenido se almacena en el contenido, se reanuda en el mismo punto en el que se detuvo; Si el contenido se emite, se reanuda en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="b4cad-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="b4cad-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="b4cad-117">NEXT</span></span>   | <span data-ttu-id="b4cad-118">El siguiente elemento de **entrada** se reproduce como si no se hubiera producido el evento y Windows Media Player había alcanzado el final del clip actual.</span><span class="sxs-lookup"><span data-stu-id="b4cad-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="b4cad-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="b4cad-119">BREAK</span></span>  | <span data-ttu-id="b4cad-120">Si la entrada actual está dentro de un bucle de **repetición** , el bucle finaliza como si se hubiera completado el recuento de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="b4cad-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="b4cad-121">De lo contrario, Windows Media Player salta al final de la lista de reproducción como si la entrada final se hubiera completado como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="b4cad-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="b4cad-122">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="b4cad-122">Parent/Child Elements</span></span>



| <span data-ttu-id="b4cad-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b4cad-123">Hierarchy</span></span>       | <span data-ttu-id="b4cad-124">Elementos</span><span class="sxs-lookup"><span data-stu-id="b4cad-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="b4cad-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b4cad-125">Parent elements</span></span> | <span data-ttu-id="b4cad-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="b4cad-126">**ASX**</span></span>                 |
| <span data-ttu-id="b4cad-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4cad-127">Child elements</span></span>  | <span data-ttu-id="b4cad-128">**entry**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="b4cad-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4cad-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4cad-129">Remarks</span></span>

<span data-ttu-id="b4cad-130">Este elemento define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="b4cad-131">Un evento es un tipo determinado de comando de script incrustado en una secuencia enviada a Windows Media Player que consta de una cadena doble.</span><span class="sxs-lookup"><span data-stu-id="b4cad-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="b4cad-132">La primera cadena es la palabra "Event" y la segunda cadena es el nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="b4cad-133">El nombre del evento en la segunda cadena debe coincidir con el nombre del evento definido en el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="b4cad-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="b4cad-134">(La coincidencia no distingue entre mayúsculas y minúsculas). Los eventos se pueden enviar a Windows Media Player recibir un flujo en tiempo real, o bien se pueden guardar en un archivo. ASF,. WMA o. wmv que se entrega como una secuencia de unidifusión a petición.</span><span class="sxs-lookup"><span data-stu-id="b4cad-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="b4cad-135">Cuando Windows Media Player recibe el comando de script, procesa el evento tal y como se define en el elemento de **evento** .</span><span class="sxs-lookup"><span data-stu-id="b4cad-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="b4cad-136">Este elemento define un ámbito de elementos **entry** o **ENTRYREF** que se procesan siempre que Windows Media Player recibe el comando de script con el evento con nombre.</span><span class="sxs-lookup"><span data-stu-id="b4cad-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="b4cad-137">**ENTRYREF** puede ser una dirección URL que apunta a una página ASP.</span><span class="sxs-lookup"><span data-stu-id="b4cad-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="b4cad-138">Con este elemento, puede especificar un comportamiento para el cambio de flujo casi en tiempo real, en lugar de los cambios de flujo previamente creados mediante referencias a otras partes de contenido o a los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4cad-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="b4cad-139">Al usar páginas ASP para generar listas de reproducción, debe especificar un valor para la *respuesta*. Propiedad **ContentType** y la *respuesta*. propiedad **Expires** en la página ASP debido a problemas de latencia con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b4cad-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="b4cad-140">La *respuesta*. **ContentType** debe ser una extensión de nombre de archivo válida para los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4cad-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="b4cad-141">Entre los tipos válidos se incluyen. ASF,. ASX,. WMA,. Wax,. WMV y. wvx.</span><span class="sxs-lookup"><span data-stu-id="b4cad-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="b4cad-142">Vea el SDK de la plataforma para obtener más información sobre cómo usar el objeto de **respuesta** en ASP.</span><span class="sxs-lookup"><span data-stu-id="b4cad-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="b4cad-143">Este elemento puede aparecer en cualquier parte del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="b4cad-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="b4cad-144">Si varios elementos **Event** dentro de un elemento **ASX** tienen valores idénticos para sus atributos **Name** , Windows Media Player usa la primera aparición dentro del elemento **ASX** y omite el resto.</span><span class="sxs-lookup"><span data-stu-id="b4cad-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="b4cad-145">Cuando los elementos de **evento** tienen atributos de **nombre** distintos, no importa su orden dentro del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="b4cad-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="b4cad-146">Windows Media Player descarta los eventos que recibe mientras procesa otro evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="b4cad-147">No se admite el anidamiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4cad-147">Nesting of events is not supported.</span></span> <span data-ttu-id="b4cad-148">Cuando Windows Media Player está en modo de vista previa, el contenido del evento no está restringido por el elemento **PREVIEWDURATION** ; la longitud total del contenido del evento puede reproducirse incluso si la duración de la vista previa del elemento de **entrada** activo expira antes del final del evento.</span><span class="sxs-lookup"><span data-stu-id="b4cad-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="b4cad-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4cad-149">Examples</span></span>

<span data-ttu-id="b4cad-150">En este ejemplo, cuando Windows Media Player recibe el evento de comando de script y la cadena de comando "Adlink" en el medio de streaming que se está representando, busca un **EVENTNAME** "Adlink" en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b4cad-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="b4cad-151">Windows Media Player cambia desde el flujo que se está representando y reproduce el contenido al que se hace referencia en el **evento**, " https://example.microsoft.com/adlink.htm ".</span><span class="sxs-lookup"><span data-stu-id="b4cad-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="b4cad-152">El atributo de **entrada** **CLIENTSKIP** está establecido en no para evitar que se omita el clip de **eventos** .</span><span class="sxs-lookup"><span data-stu-id="b4cad-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="b4cad-153">Debe reproducirse.</span><span class="sxs-lookup"><span data-stu-id="b4cad-153">It must be played.</span></span>

<span data-ttu-id="b4cad-154">El script `WHENDONE="RESUME"` indica a Windows Media Player que reanude la reproducción del medio anterior que cambió desde el momento en que se ha finalizado Adlink. ASF.</span><span class="sxs-lookup"><span data-stu-id="b4cad-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="b4cad-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4cad-155">Requirements</span></span>



| <span data-ttu-id="b4cad-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4cad-156">Requirement</span></span> | <span data-ttu-id="b4cad-157">Value</span><span class="sxs-lookup"><span data-stu-id="b4cad-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b4cad-158">Versión</span><span class="sxs-lookup"><span data-stu-id="b4cad-158">Version</span></span><br/> | <span data-ttu-id="b4cad-159">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b4cad-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4cad-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4cad-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cad-161">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b4cad-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b4cad-162">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b4cad-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="b4cad-163">**Modelo de objetos de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="b4cad-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





