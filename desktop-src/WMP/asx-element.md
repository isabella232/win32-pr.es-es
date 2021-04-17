---
title: Elemento ASX
description: El elemento ASX define un archivo como un metarchivo.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX de Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700063"
---
# <a name="asx-element"></a><span data-ttu-id="01915-104">Elemento ASX</span><span class="sxs-lookup"><span data-stu-id="01915-104">ASX Element</span></span>

<span data-ttu-id="01915-105">El elemento **ASX** define un archivo como un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="01915-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="01915-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="01915-106">Attributes</span></span>

<span data-ttu-id="01915-107">`VERSION` (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="01915-107">`VERSION` (required)</span></span>

<span data-ttu-id="01915-108">Número decimal que representa el número de versión de la sintaxis del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="01915-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="01915-109">Establezca en 3 o 3,0.</span><span class="sxs-lookup"><span data-stu-id="01915-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="01915-110">**PREVIEWMODE** (opcional)</span><span class="sxs-lookup"><span data-stu-id="01915-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="01915-111">Valor que indica si Windows Media Player entra en el modo de vista previa antes de reproducir el primer clip.</span><span class="sxs-lookup"><span data-stu-id="01915-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="01915-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="01915-112">Must be one of the following values.</span></span>



| <span data-ttu-id="01915-113">Value</span><span class="sxs-lookup"><span data-stu-id="01915-113">Value</span></span> | <span data-ttu-id="01915-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="01915-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01915-115">SÍ</span><span class="sxs-lookup"><span data-stu-id="01915-115">YES</span></span>   | <span data-ttu-id="01915-116">Windows Media Player entra en el modo de vista previa antes de reproducir el primer clip.</span><span class="sxs-lookup"><span data-stu-id="01915-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="01915-117">No</span><span class="sxs-lookup"><span data-stu-id="01915-117">NO</span></span>    | <span data-ttu-id="01915-118">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="01915-118">The default value.</span></span> <span data-ttu-id="01915-119">Windows Media Player no entra en el modo de vista previa antes de reproducir el primer clip.</span><span class="sxs-lookup"><span data-stu-id="01915-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="01915-120">**BANNERBAR** (opcional)</span><span class="sxs-lookup"><span data-stu-id="01915-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="01915-121">Valor que indica si Windows Media Player Reserva espacio para un gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="01915-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="01915-122">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="01915-122">Must be one of the following values.</span></span>



| <span data-ttu-id="01915-123">Value</span><span class="sxs-lookup"><span data-stu-id="01915-123">Value</span></span> | <span data-ttu-id="01915-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="01915-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01915-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="01915-125">AUTO</span></span>  | <span data-ttu-id="01915-126">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="01915-126">The default value.</span></span> <span data-ttu-id="01915-127">Windows Media Player Reserva espacio para la barra de pancarta solo cuando una parte de contenido incluye una.</span><span class="sxs-lookup"><span data-stu-id="01915-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="01915-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="01915-128">FIXED</span></span> | <span data-ttu-id="01915-129">Windows Media Player reserva un espacio fijo para un gráfico de banner para cada fragmento de contenido reproducido, independientemente de si hay un banner asociado.</span><span class="sxs-lookup"><span data-stu-id="01915-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="01915-130">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="01915-130">Parent/Child Elements</span></span>



| <span data-ttu-id="01915-131">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="01915-131">Hierarchy</span></span>       | <span data-ttu-id="01915-132">Elementos</span><span class="sxs-lookup"><span data-stu-id="01915-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01915-133">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="01915-133">Parent elements</span></span> | <span data-ttu-id="01915-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="01915-134">None.</span></span> <span data-ttu-id="01915-135">El elemento **ASX** debe ser el primer elemento de cada metarchivo.</span><span class="sxs-lookup"><span data-stu-id="01915-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="01915-136">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01915-136">Child elements</span></span>  | <span data-ttu-id="01915-137">**abstract**, **Author**, **banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **MOREINFO**, **PREVIEWDURATION**, **param**, **REPEAT**, **title**</span><span class="sxs-lookup"><span data-stu-id="01915-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="01915-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01915-138">Remarks</span></span>

<span data-ttu-id="01915-139">Los cuatro primeros caracteres de una lista de reproducción de metarchivo deben ser "<ASX".</span><span class="sxs-lookup"><span data-stu-id="01915-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="01915-140">Otros elementos definidos dentro del ámbito del elemento **ASX** , como **title** y **Author**, se asocian con la información mostrada por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="01915-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="01915-141">En Windows Media Player, el número de versión de sintaxis es 3,0.</span><span class="sxs-lookup"><span data-stu-id="01915-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="01915-142">Windows Media Player es compatible con todas las versiones anteriores de la sintaxis de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="01915-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="01915-143">Los valores aceptables para el atributo **version** incluyen 3,0 y 3 (sin separador decimal).</span><span class="sxs-lookup"><span data-stu-id="01915-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="01915-144">Si el valor del atributo **PREVIEWMODE** es Yes, Windows Media Player entra inmediatamente en el modo de vista previa antes de reproducir el primer clip.</span><span class="sxs-lookup"><span data-stu-id="01915-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="01915-145">Cuando Windows Media Player entra en el modo de vista previa, muestra una vista previa de cada clip al que se hace referencia en el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="01915-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="01915-146">El elemento **PREVIEWDURATION** determina la duración de cada vista previa.</span><span class="sxs-lookup"><span data-stu-id="01915-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="01915-147">El atributo **BANNERBAR** define si Windows Media Player Reserva espacio para un gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="01915-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="01915-148">Un banner es un gráfico que se muestra en el área de presentación de vídeo mientras se reproduce el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="01915-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="01915-149">(Use el elemento **banner** para agregar un banner al contenido). Si el valor de **BANNERBAR** es fijo, Windows Media Player reserva el espacio de banner para cada fragmento de contenido multimedia, tanto si el contenido multimedia tiene un banner.</span><span class="sxs-lookup"><span data-stu-id="01915-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="01915-150">Si una parte del contenido multimedia no tiene un banner asociado, el espacio reservado para uno es negro.</span><span class="sxs-lookup"><span data-stu-id="01915-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="01915-151">Si el valor del atributo **BANNERBAR** es auto, Windows Media Player Reserva espacio para el banner solo cuando el contenido multimedia incluye uno.</span><span class="sxs-lookup"><span data-stu-id="01915-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="01915-152">Si crea un metarchivo con varios clips (elementos **entry** o **ENTRYREF** ) y establece el valor del atributo **BANNERBAR** en auto, Windows Media Player podría cambiar de tamaño para permitir el espacio para un gráfico de banner para un clip y, a continuación, volver a cambiar el tamaño si el siguiente clip no contiene un gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="01915-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="01915-153">Si desea que el tamaño de la ventana permanezca igual (excepto cuando cambie el tamaño del vídeo), use el valor fijo del atributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="01915-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="01915-154">El espacio reservado para un gráfico de banner es de 32 píxeles de alto por 194 píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="01915-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="01915-155">El espacio reservado aparece debajo de cualquier contenido de vídeo representado y 6 píxeles por encima del borde inferior del área de vídeo, lo que permite espacio para el borde del área de vídeo de 6 píxeles.</span><span class="sxs-lookup"><span data-stu-id="01915-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="01915-156">El espacio reservado del banner está centrado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="01915-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="01915-157">Windows Media Player representa el gráfico que comienza en el píxel situado más a la izquierda del espacio de la pancarta.</span><span class="sxs-lookup"><span data-stu-id="01915-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="01915-158">Si el gráfico rellena todo el espacio, aparecerá centrado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="01915-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="01915-159">De lo contrario, habrá espacio final.</span><span class="sxs-lookup"><span data-stu-id="01915-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="01915-160">Tenga en cuenta que el ancho mínimo de Windows Media Player siempre es mayor que el tamaño del clip de vídeo, independientemente del valor del atributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="01915-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="01915-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="01915-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="01915-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01915-162">Requirements</span></span>



| <span data-ttu-id="01915-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="01915-163">Requirement</span></span> | <span data-ttu-id="01915-164">Value</span><span class="sxs-lookup"><span data-stu-id="01915-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="01915-165">Versión</span><span class="sxs-lookup"><span data-stu-id="01915-165">Version</span></span><br/> | <span data-ttu-id="01915-166">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="01915-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01915-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="01915-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01915-168">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="01915-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="01915-169">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="01915-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





