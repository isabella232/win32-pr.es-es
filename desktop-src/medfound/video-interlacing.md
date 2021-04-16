---
description: Entrelazado de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelazado de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705887"
---
# <a name="video-interlacing"></a><span data-ttu-id="06b67-103">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="06b67-103">Video Interlacing</span></span>

<span data-ttu-id="06b67-104">En este tema se describe cómo los orígenes y descodificadores multimedia deben controlar el contenido de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="06b67-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="06b67-105">Para descodificar y representar correctamente el vídeo entrelazado, se necesita la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="06b67-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="06b67-106">Progresiva o entrelazada.</span><span class="sxs-lookup"><span data-stu-id="06b67-106">Progressive or interlaced.</span></span> <span data-ttu-id="06b67-107">Un flujo de vídeo puede contener fotogramas progresivos, fotogramas entrelazados o una combinación de ambos.</span><span class="sxs-lookup"><span data-stu-id="06b67-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="06b67-108">Dominio de campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-108">Field dominance.</span></span> <span data-ttu-id="06b67-109">Dominio de campo describe el campo que aparece en primer lugar, el campo superior o el campo inferior.</span><span class="sxs-lookup"><span data-stu-id="06b67-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="06b67-110">Repite el primer campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-110">Repeat first field.</span></span> <span data-ttu-id="06b67-111">Esta marca se usa en el desplegable 3:2, cuando el fotograma es progresivo, pero la secuencia está entrelazada.</span><span class="sxs-lookup"><span data-stu-id="06b67-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="06b67-112">En este contexto, el primer campo puede ser el campo superior o inferior.</span><span class="sxs-lookup"><span data-stu-id="06b67-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="06b67-113">Campos intercalados o un solo campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-113">Interleaved fields or single field.</span></span> <span data-ttu-id="06b67-114">Un ejemplo puede contener un solo campo o dos campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="06b67-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="06b67-115">Si un ejemplo contiene un solo campo, el alto de ejemplo es la mitad del alto del marco, ya que el ejemplo solo contiene la mitad de las líneas de recorrido de un fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="06b67-116">Los campos intercalados se recomiendan a menos que las características del contenido de origen dicten lo contrario.</span><span class="sxs-lookup"><span data-stu-id="06b67-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="06b67-117">Cualquiera de estas características puede cambiar de una muestra a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="06b67-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="06b67-118">Sin embargo, los componentes de vídeo deben saber algo sobre el contenido general antes de comenzar la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="06b67-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="06b67-119">Por ejemplo, si el vídeo está entrelazado, el representador de vídeo mejorado (EVR) debe reservar la memoria de vídeo para el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="06b67-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="06b67-120">Si el vídeo es totalmente fotogramas progresivos, por otro lado, el EVR puede optimizar la canalización de representación.</span><span class="sxs-lookup"><span data-stu-id="06b67-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="06b67-121">Agregar un paso de desentrelazado a la canalización aumenta la latencia de representación.</span><span class="sxs-lookup"><span data-stu-id="06b67-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="06b67-122">La información sobre el entrelazado se almacena en dos lugares:</span><span class="sxs-lookup"><span data-stu-id="06b67-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="06b67-123">La información general sobre el entrelazado en una secuencia se coloca en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="06b67-124">Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="06b67-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="06b67-125">La información que puede cambiar con cada ejemplo se coloca en el ejemplo como un atributo.</span><span class="sxs-lookup"><span data-stu-id="06b67-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="06b67-126">Para obtener más información acerca de los ejemplos, vea [ejemplos de medios](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="06b67-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="06b67-127">Información de entrelazado en el tipo de medio</span><span class="sxs-lookup"><span data-stu-id="06b67-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="06b67-128">El atributo de [**\_ \_ \_ modo entrelazado MF MT**](mf-mt-interlace-mode-attribute.md) en el tipo de medio describe cómo se entrelaza la secuencia en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="06b67-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="06b67-129">El valor de este atributo es un miembro de la enumeración [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="06b67-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="06b67-130">Un tipo de medio de vídeo siempre debe tener este atributo.</span><span class="sxs-lookup"><span data-stu-id="06b67-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="06b67-131">Si la secuencia contiene solo fotogramas progresivos, sin fotogramas entrelazados, use MFVideoInterlace \_ progresivo.</span><span class="sxs-lookup"><span data-stu-id="06b67-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="06b67-132">Si la secuencia contiene solo fotogramas entrelazados y cada ejemplo contiene dos campos intercalados, use MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="06b67-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="06b67-133">Si la secuencia contiene solo fotogramas entrelazados y cada ejemplo contiene un solo campo, utilice MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="06b67-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="06b67-134">Si los campos alternan entre la parte superior e inferior, no importa cuál de estos dos valores se use.</span><span class="sxs-lookup"><span data-stu-id="06b67-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="06b67-135">Si el formato contiene solo los campos superiores, o simplemente los campos inferiores, establezca el valor que se corresponda con el contenido.</span><span class="sxs-lookup"><span data-stu-id="06b67-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="06b67-136">Si la secuencia contiene una mezcla de fotogramas entrelazados y progresivos, o si el campo domina, establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="06b67-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="06b67-137">Use los atributos de ejemplo para describir cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="06b67-138">En la tabla siguiente se resume este atributo.</span><span class="sxs-lookup"><span data-stu-id="06b67-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="06b67-139">\_ \_ modo entrelazado MF MT \_</span><span class="sxs-lookup"><span data-stu-id="06b67-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="06b67-140">Entrelazadas?</span><span class="sxs-lookup"><span data-stu-id="06b67-140">Interlaced?</span></span> | <span data-ttu-id="06b67-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06b67-141">Samples</span></span>                                  | <span data-ttu-id="06b67-142">Primer campo</span><span class="sxs-lookup"><span data-stu-id="06b67-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="06b67-143">\_Progresiva MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="06b67-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="06b67-144">No</span><span class="sxs-lookup"><span data-stu-id="06b67-144">No</span></span>          | <span data-ttu-id="06b67-145">Fotograma progresivo</span><span class="sxs-lookup"><span data-stu-id="06b67-145">Progressive frame</span></span>                        | <span data-ttu-id="06b67-146">No aplicable</span><span class="sxs-lookup"><span data-stu-id="06b67-146">Not applicable</span></span> |
| <span data-ttu-id="06b67-147">MFVideoInterlace \_ FieldInterleavedUpperFirst</span><span class="sxs-lookup"><span data-stu-id="06b67-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="06b67-148">Sí</span><span class="sxs-lookup"><span data-stu-id="06b67-148">Yes</span></span>         | <span data-ttu-id="06b67-149">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="06b67-149">Interleaved fields</span></span>                       | <span data-ttu-id="06b67-150">Primero en primer lugar</span><span class="sxs-lookup"><span data-stu-id="06b67-150">Upper first</span></span>    |
| <span data-ttu-id="06b67-151">MFVideoInterlace \_ FieldInterleavedLowerFirst</span><span class="sxs-lookup"><span data-stu-id="06b67-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="06b67-152">Sí</span><span class="sxs-lookup"><span data-stu-id="06b67-152">Yes</span></span>         | <span data-ttu-id="06b67-153">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="06b67-153">Interleaved fields</span></span>                       | <span data-ttu-id="06b67-154">Inferior primero</span><span class="sxs-lookup"><span data-stu-id="06b67-154">Lower first</span></span>    |
| <span data-ttu-id="06b67-155">MFVideoInterlace \_ FieldSingleUpper</span><span class="sxs-lookup"><span data-stu-id="06b67-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="06b67-156">Sí</span><span class="sxs-lookup"><span data-stu-id="06b67-156">Yes</span></span>         | <span data-ttu-id="06b67-157">Campo único</span><span class="sxs-lookup"><span data-stu-id="06b67-157">Single field</span></span>                             | <span data-ttu-id="06b67-158">Primero en primer lugar</span><span class="sxs-lookup"><span data-stu-id="06b67-158">Upper first</span></span>    |
| <span data-ttu-id="06b67-159">MFVideoInterlace \_ FieldSingleLower</span><span class="sxs-lookup"><span data-stu-id="06b67-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="06b67-160">Sí</span><span class="sxs-lookup"><span data-stu-id="06b67-160">Yes</span></span>         | <span data-ttu-id="06b67-161">Campo único</span><span class="sxs-lookup"><span data-stu-id="06b67-161">Single field</span></span>                             | <span data-ttu-id="06b67-162">Inferior primero</span><span class="sxs-lookup"><span data-stu-id="06b67-162">Lower first</span></span>    |
| <span data-ttu-id="06b67-163">MFVideoInterlace \_ MixedInterlaceOrProgressive</span><span class="sxs-lookup"><span data-stu-id="06b67-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="06b67-164">Puede variar</span><span class="sxs-lookup"><span data-stu-id="06b67-164">Can vary</span></span>    | <span data-ttu-id="06b67-165">Campos intercalados o fotogramas progresivos</span><span class="sxs-lookup"><span data-stu-id="06b67-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="06b67-166">Puede variar</span><span class="sxs-lookup"><span data-stu-id="06b67-166">Can vary</span></span>       |



 

<span data-ttu-id="06b67-167">Los campos intercalados y los campos únicos no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="06b67-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="06b67-168">Cambiar de uno a otro requiere un cambio de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="06b67-169">Marcas de entrelazado en ejemplos</span><span class="sxs-lookup"><span data-stu-id="06b67-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="06b67-170">La información que puede cambiar de una muestra a la siguiente se indica mediante los atributos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="06b67-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="06b67-171">Use la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obtener o establecer estos atributos.</span><span class="sxs-lookup"><span data-stu-id="06b67-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="06b67-172">Todos los atributos de entrelazado que aparecen en esta sección tienen valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="06b67-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="06b67-173">En realidad, cada uno de estos atributos puede tener tres valores: **true**, **false** o Not Set.</span><span class="sxs-lookup"><span data-stu-id="06b67-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="06b67-174">Si no se establece un atributo, el valor se toma del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="06b67-175">Si se establece un atributo, el valor invalida el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="06b67-176">Algunas combinaciones de marcas y tipos de medios no son válidas.</span><span class="sxs-lookup"><span data-stu-id="06b67-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06b67-177">Atributo</span><span class="sxs-lookup"><span data-stu-id="06b67-177">Attribute</span></span></th>
<th><span data-ttu-id="06b67-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="06b67-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06b67-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="06b67-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="06b67-180">Si es <strong>true</strong>, el marco está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="06b67-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="06b67-181">Si es <strong>false</strong>, el marco es progresivo.</span><span class="sxs-lookup"><span data-stu-id="06b67-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="06b67-182">Establezca este atributo en cada ejemplo si el tipo de medio es MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="06b67-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b67-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="06b67-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="06b67-184">El significado de esta marca depende de si los ejemplos contienen campos intercalados o campos individuales.</span><span class="sxs-lookup"><span data-stu-id="06b67-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="06b67-185">Campos intercalados: si es <strong>true</strong>, el campo inferior es el primero.</span><span class="sxs-lookup"><span data-stu-id="06b67-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="06b67-186">Si es <strong>false</strong>, el campo superior es primero.</span><span class="sxs-lookup"><span data-stu-id="06b67-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="06b67-187">Campos únicos: Si <strong>es true</strong>, el ejemplo contiene un campo inferior.</span><span class="sxs-lookup"><span data-stu-id="06b67-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="06b67-188">Si <strong>es false</strong>, el ejemplo contiene un campo superior.</span><span class="sxs-lookup"><span data-stu-id="06b67-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="06b67-189">Establezca este atributo en cada ejemplo entrelazado si el tipo de medio es MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="06b67-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b67-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="06b67-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="06b67-191">Si es <strong>true</strong>, el primer campo se repite.</span><span class="sxs-lookup"><span data-stu-id="06b67-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="06b67-192">Si es <strong>false</strong> o no se establece, el primer campo no se repite.</span><span class="sxs-lookup"><span data-stu-id="06b67-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b67-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="06b67-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="06b67-194">Si <strong>es true</strong>, el ejemplo contiene un solo campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="06b67-195">Si <strong>es false</strong>, el ejemplo contiene campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="06b67-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="06b67-196">En la tabla siguiente se muestra qué marcas son necesarias, opcionales o prohibidas, en función del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="06b67-197">Tipo de soporte</span><span class="sxs-lookup"><span data-stu-id="06b67-197">Media Type</span></span>         | <span data-ttu-id="06b67-198">Marca entrelazada</span><span class="sxs-lookup"><span data-stu-id="06b67-198">Interlaced Flag</span></span>                      | <span data-ttu-id="06b67-199">Marca BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="06b67-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="06b67-200">Marca RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="06b67-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="06b67-201">Marca SingleField</span><span class="sxs-lookup"><span data-stu-id="06b67-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="06b67-202">progresivo</span><span class="sxs-lookup"><span data-stu-id="06b67-202">Progressive</span></span>        | <span data-ttu-id="06b67-203">Opta Si se establece, debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="06b67-204">No lo establezca.</span><span class="sxs-lookup"><span data-stu-id="06b67-204">Do not set.</span></span>                              | <span data-ttu-id="06b67-205">No lo establezca.</span><span class="sxs-lookup"><span data-stu-id="06b67-205">Do not set.</span></span>           | <span data-ttu-id="06b67-206">No lo establezca.</span><span class="sxs-lookup"><span data-stu-id="06b67-206">Do not set.</span></span>                          |
| <span data-ttu-id="06b67-207">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="06b67-207">Interleaved fields</span></span> | <span data-ttu-id="06b67-208">Opta Si se establece, debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="06b67-209">Opta Si se establece, debe coincidir con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="06b67-210">No lo establezca.</span><span class="sxs-lookup"><span data-stu-id="06b67-210">Do not set.</span></span>           | <span data-ttu-id="06b67-211">Opta Si se establece, debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="06b67-212">Campos únicos</span><span class="sxs-lookup"><span data-stu-id="06b67-212">Single fields</span></span>      | <span data-ttu-id="06b67-213">Opta Si se establece, debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="06b67-214">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06b67-214">Required.</span></span>                                | <span data-ttu-id="06b67-215">No lo establezca.</span><span class="sxs-lookup"><span data-stu-id="06b67-215">Do not set.</span></span>           | <span data-ttu-id="06b67-216">Establézcalo en **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="06b67-217">Mixto</span><span class="sxs-lookup"><span data-stu-id="06b67-217">Mixed</span></span>              | <span data-ttu-id="06b67-218">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06b67-218">Required.</span></span>                            | <span data-ttu-id="06b67-219">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06b67-219">Required.</span></span>                                | <span data-ttu-id="06b67-220">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06b67-220">Required.</span></span>             | <span data-ttu-id="06b67-221">Opta Si se establece, debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="06b67-222">En los casos en los que el atributo es opcional, el tipo de medio ya define la información.</span><span class="sxs-lookup"><span data-stu-id="06b67-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="06b67-223">Es válido establecer el atributo para que coincida, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="06b67-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="06b67-224">Por ejemplo, si el tipo de medio es MFVideoInterlace \_ progresivo, implica que todos los marcos de la secuencia son progresivos.</span><span class="sxs-lookup"><span data-stu-id="06b67-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="06b67-225">Por lo tanto, puede establecer el **atributo \_ entrelazado MFSampleExtension** en **false** o dejar el atributo como no establecido.</span><span class="sxs-lookup"><span data-stu-id="06b67-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="06b67-226">Recomendaciones</span><span class="sxs-lookup"><span data-stu-id="06b67-226">Recommendations</span></span>

<span data-ttu-id="06b67-227">Esta sección contiene recomendaciones para varios tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="06b67-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="06b67-228">El vídeo es todos los fotogramas progresivos.</span><span class="sxs-lookup"><span data-stu-id="06b67-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="06b67-229">Establezca el tipo de medio en MFVideoInterlace \_ progresivo.</span><span class="sxs-lookup"><span data-stu-id="06b67-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="06b67-230">No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **false** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="06b67-231">No establezca los atributos **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField** .</span><span class="sxs-lookup"><span data-stu-id="06b67-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="06b67-232">El vídeo son todos los campos entrelazados con el mismo dominio de campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="06b67-233">Los ejemplos contienen campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="06b67-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="06b67-234">Establezca el tipo de medio en MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="06b67-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="06b67-235">No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **true** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="06b67-236">No establezca el atributo **\_ BottomFieldFirst de MFSampleExtension** o establezca el valor en cada fotograma para que coincida con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="06b67-237">No establezca el atributo **\_ RepeatFirstField de MFSampleExtension** o establézcalo en **false** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="06b67-238">No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **false** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="06b67-239">El vídeo contiene una mezcla de fotogramas entrelazados y progresivos, con campos repetidos y una superposición de campo variable (por ejemplo, vídeo DVD).</span><span class="sxs-lookup"><span data-stu-id="06b67-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="06b67-240">Establezca el tipo de medio en MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="06b67-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="06b67-241">En cada fotograma, establezca los atributos **MFSampleExtension \_ entrelazad**, **MFSampleExtension \_ BottomFieldFirst** y **MFSampleExtension \_ RepeatFirstField** .</span><span class="sxs-lookup"><span data-stu-id="06b67-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="06b67-242">No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **false** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="06b67-243">El vídeo está entrelazado y los ejemplos contienen campos únicos.</span><span class="sxs-lookup"><span data-stu-id="06b67-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="06b67-244">Establezca el tipo de medio en MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="06b67-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="06b67-245">En cada fotograma, establezca el atributo **\_ BottomFieldFirst de MFSampleExtension** .</span><span class="sxs-lookup"><span data-stu-id="06b67-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="06b67-246">No establezca el atributo **\_ entrelazado MFSampleExtension** o establézcalo en **true** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="06b67-247">No establezca el atributo **\_ RepeatFirstField de MFSampleExtension** o establézcalo en **false** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="06b67-248">No establezca el atributo **\_ SingleField de MFSampleExtension** o establézcalo en **true** en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="06b67-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="06b67-249">La mayoría del contenido de vídeo se encuentra en una de estas categorías.</span><span class="sxs-lookup"><span data-stu-id="06b67-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="06b67-250">Asignaciones MPEG-2</span><span class="sxs-lookup"><span data-stu-id="06b67-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="06b67-251">En el caso de contenido MPEG-2, utilice las siguientes asignaciones para convertir las marcas MPEG-2 en Media Foundation atributos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="06b67-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="06b67-252">**estructura de la imagen \_**</span><span class="sxs-lookup"><span data-stu-id="06b67-252">**picture\_structure**</span></span>



| <span data-ttu-id="06b67-253">Value</span><span class="sxs-lookup"><span data-stu-id="06b67-253">Value</span></span>         | <span data-ttu-id="06b67-254">Atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b67-255">frame</span><span class="sxs-lookup"><span data-stu-id="06b67-255">frame</span></span>         | <span data-ttu-id="06b67-256">**MFSampleExtension \_ SingleField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="06b67-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="06b67-257">\_campo superior</span><span class="sxs-lookup"><span data-stu-id="06b67-257">top\_field</span></span>    | <span data-ttu-id="06b67-258">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="06b67-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="06b67-259">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="06b67-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="06b67-260">\_campo inferior</span><span class="sxs-lookup"><span data-stu-id="06b67-260">bottom\_field</span></span> | <span data-ttu-id="06b67-261">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="06b67-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="06b67-262">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="06b67-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="06b67-263">**fotograma progresivo \_**</span><span class="sxs-lookup"><span data-stu-id="06b67-263">**progressive\_frame**</span></span>



| <span data-ttu-id="06b67-264">Value</span><span class="sxs-lookup"><span data-stu-id="06b67-264">Value</span></span> | <span data-ttu-id="06b67-265">Atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="06b67-266">0</span><span class="sxs-lookup"><span data-stu-id="06b67-266">0</span></span>     | <span data-ttu-id="06b67-267">**MFSampleExtension \_ True entrelazado**  =  </span><span class="sxs-lookup"><span data-stu-id="06b67-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="06b67-268">1</span><span class="sxs-lookup"><span data-stu-id="06b67-268">1</span></span>     | <span data-ttu-id="06b67-269">**MFSampleExtension \_ FALSE entrelazado**  =  </span><span class="sxs-lookup"><span data-stu-id="06b67-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="06b67-270">**\_primer campo \_ primero**</span><span class="sxs-lookup"><span data-stu-id="06b67-270">**top\_field\_first**</span></span>



| <span data-ttu-id="06b67-271">Value</span><span class="sxs-lookup"><span data-stu-id="06b67-271">Value</span></span> | <span data-ttu-id="06b67-272">Atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="06b67-273">0</span><span class="sxs-lookup"><span data-stu-id="06b67-273">0</span></span>     | <span data-ttu-id="06b67-274">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="06b67-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="06b67-275">1</span><span class="sxs-lookup"><span data-stu-id="06b67-275">1</span></span>     | <span data-ttu-id="06b67-276">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="06b67-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="06b67-277">**repetir \_ primer \_ campo**</span><span class="sxs-lookup"><span data-stu-id="06b67-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="06b67-278">Value</span><span class="sxs-lookup"><span data-stu-id="06b67-278">Value</span></span> | <span data-ttu-id="06b67-279">Atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="06b67-280">0</span><span class="sxs-lookup"><span data-stu-id="06b67-280">0</span></span>     | <span data-ttu-id="06b67-281">**MFSampleExtension \_ RepeatFirstField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="06b67-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="06b67-282">1</span><span class="sxs-lookup"><span data-stu-id="06b67-282">1</span></span>     | <span data-ttu-id="06b67-283">**MFSampleExtension \_ RepeatFirstField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="06b67-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="06b67-284">Ejemplos de Single-Field</span><span class="sxs-lookup"><span data-stu-id="06b67-284">Single-Field Samples</span></span>

<span data-ttu-id="06b67-285">Si el tipo de medio es MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower, significa que cada ejemplo contiene un solo campo.</span><span class="sxs-lookup"><span data-stu-id="06b67-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="06b67-286">Sin embargo, el tipo de medio describe todo el marco.</span><span class="sxs-lookup"><span data-stu-id="06b67-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="06b67-287">Por lo tanto, cada búfer contiene solo la mitad del número de líneas de campo que se proporcionan en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="06b67-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="06b67-288">Por ejemplo, si el tipo de medio describe el vídeo como 720 × 480, cada campo contiene 240 líneas de análisis y, por tanto, cada búfer contiene solo 240 filas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="06b67-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="06b67-289">Si escribe un componente que acepta tipos de medios con muestras de un solo campo, debe tener en cuenta este hecho al tener acceso a los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="06b67-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="06b67-290">La misma regla se aplica a la abertura geométrica (atributo de[ \_ \_ \_ abertura geométrica de MF MT](mf-mt-geometric-aperture-attribute.md) ) y a la abertura mínima de pantalla (el atributo de[ \_ \_ \_ \_ abertura de pantalla mínima MF MT](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="06b67-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="06b67-291">Estas regiones se especifican en términos de todo el marco, no de los campos individuales.</span><span class="sxs-lookup"><span data-stu-id="06b67-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="06b67-292">Asignaciones de DirectShow</span><span class="sxs-lookup"><span data-stu-id="06b67-292">DirectShow Mappings</span></span>

<span data-ttu-id="06b67-293">En DirectShow, la información de entrelazado por muestra se incluye en el miembro **dwTypeSpecificFlags** de la estructura de **\_ \_ propiedades AM SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="06b67-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="06b67-294">En la tabla siguiente se muestran los atributos equivalentes para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="06b67-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="06b67-295">Marca de ejemplo de DirectShow</span><span class="sxs-lookup"><span data-stu-id="06b67-295">DirectShow sample flag</span></span>              | <span data-ttu-id="06b67-296">Media Foundation atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b67-297">\_marca de vídeo AM \_ \_ FOTOgrama intercalado \_</span><span class="sxs-lookup"><span data-stu-id="06b67-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="06b67-298">**MFSampleExtension \_ SingleField**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="06b67-299">\_Marca de vídeo AM \_ \_ Campo1</span><span class="sxs-lookup"><span data-stu-id="06b67-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="06b67-300">**MFSampleExtension \_ True entrelazado**  =  .</span><span class="sxs-lookup"><span data-stu-id="06b67-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="06b67-301">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="06b67-302">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="06b67-303">\_FIELD2 de \_ marca de vídeo AM \_</span><span class="sxs-lookup"><span data-stu-id="06b67-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="06b67-304">**MFSampleExtension \_ True entrelazado**  =  .</span><span class="sxs-lookup"><span data-stu-id="06b67-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="06b67-305">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="06b67-306">**MFSampleExtension \_ BottomFieldFirst**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="06b67-307">trama de la \_ marca de vídeo AM \_ \_</span><span class="sxs-lookup"><span data-stu-id="06b67-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="06b67-308">**MFSampleExtension \_ FALSE entrelazado**  =  .</span><span class="sxs-lookup"><span data-stu-id="06b67-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="06b67-309">(Este marcador indica que el controlador no debe Desentrelazar los dos campos).</span><span class="sxs-lookup"><span data-stu-id="06b67-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="06b67-310">\_Marca de vídeo AM \_ \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="06b67-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="06b67-311">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="06b67-312">Si el contenido está entrelazado y la marca de la \_ marca de vídeo AM \_ \_ FIELD1FIRST no está presente, establezca este atributo en **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="06b67-313">\_campo de \_ repetición de marca de vídeo AM \_ \_</span><span class="sxs-lookup"><span data-stu-id="06b67-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="06b67-314">**MFSampleExtension \_ RepeatFirstField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="06b67-315">Si el indicador de repetición de la \_ marca de vídeo AM \_ \_ \_ no está presente, establezca este atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="06b67-316">Si el ejemplo de DirectShow no contiene marcas de ejemplo, use el valor de **dwInterlaceFlags** de la estructura **VIDEOINFOHEADER2** :</span><span class="sxs-lookup"><span data-stu-id="06b67-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="06b67-317">Marca de entrelazado de DirectShow</span><span class="sxs-lookup"><span data-stu-id="06b67-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="06b67-318">Media Foundation atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="06b67-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="06b67-319">AMINTERLACE \_ IsInterlaced</span><span class="sxs-lookup"><span data-stu-id="06b67-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="06b67-320">**MFSampleExtension \_ True entrelazado**  =  .</span><span class="sxs-lookup"><span data-stu-id="06b67-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="06b67-321">AMINTERLACE \_ 1FieldPerSample</span><span class="sxs-lookup"><span data-stu-id="06b67-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="06b67-322">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="06b67-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="06b67-323">AMINTERLACE \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="06b67-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="06b67-324">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="06b67-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="06b67-325">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06b67-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b67-326">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="06b67-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="06b67-327">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="06b67-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




