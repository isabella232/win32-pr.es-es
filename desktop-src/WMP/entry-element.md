---
title: Elemento ENTRY
description: El elemento ENTRY especifica un archivo de Windows Media para representarlo como un clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento de entrada de Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700323"
---
# <a name="entry-element"></a><span data-ttu-id="e6149-104">Elemento ENTRY</span><span class="sxs-lookup"><span data-stu-id="e6149-104">ENTRY Element</span></span>

<span data-ttu-id="e6149-105">El elemento **entry** especifica un archivo de Windows Media para representarlo como un clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="e6149-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6149-106">Attributes</span></span>

<span data-ttu-id="e6149-107">**CLIENTSKIP**</span><span class="sxs-lookup"><span data-stu-id="e6149-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="e6149-108">Valor que indica si el usuario puede saltar hacia delante después del clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="e6149-109">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="e6149-109">Possible values include the following.</span></span>



| <span data-ttu-id="e6149-110">Value</span><span class="sxs-lookup"><span data-stu-id="e6149-110">Value</span></span> | <span data-ttu-id="e6149-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6149-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="e6149-112">SÍ</span><span class="sxs-lookup"><span data-stu-id="e6149-112">YES</span></span>   | <span data-ttu-id="e6149-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e6149-113">Default.</span></span> <span data-ttu-id="e6149-114">El usuario puede saltar adelante más allá del clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="e6149-115">No</span><span class="sxs-lookup"><span data-stu-id="e6149-115">NO</span></span>    | <span data-ttu-id="e6149-116">El usuario no puede saltar adelante más allá del clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="e6149-117">**SKIPIFREF**</span><span class="sxs-lookup"><span data-stu-id="e6149-117">**SKIPIFREF**</span></span>

<span data-ttu-id="e6149-118">Valor que indica si Windows Media Player debe omitir este clip cuando el elemento de **entrada** está incluido en un segundo metarchivo mediante el uso de un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="e6149-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="e6149-119">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="e6149-119">Possible values include the following.</span></span>



| <span data-ttu-id="e6149-120">Value</span><span class="sxs-lookup"><span data-stu-id="e6149-120">Value</span></span> | <span data-ttu-id="e6149-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6149-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6149-122">SÍ</span><span class="sxs-lookup"><span data-stu-id="e6149-122">YES</span></span>   | <span data-ttu-id="e6149-123">Windows Media Player omitirá esta entrada, si se hace referencia a ella a través de un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="e6149-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="e6149-124">No</span><span class="sxs-lookup"><span data-stu-id="e6149-124">NO</span></span>    | <span data-ttu-id="e6149-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e6149-125">Default.</span></span> <span data-ttu-id="e6149-126">Windows Media Player no omitirá esta entrada.</span><span class="sxs-lookup"><span data-stu-id="e6149-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="e6149-127">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="e6149-127">Parent/Child Elements</span></span>



| <span data-ttu-id="e6149-128">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e6149-128">Hierarchy</span></span>       | <span data-ttu-id="e6149-129">Elementos</span><span class="sxs-lookup"><span data-stu-id="e6149-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6149-130">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e6149-130">Parent elements</span></span> | <span data-ttu-id="e6149-131">**ASX**, **evento**, **repetición**</span><span class="sxs-lookup"><span data-stu-id="e6149-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="e6149-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6149-132">Child elements</span></span>  | <span data-ttu-id="e6149-133">**abstract**, **Author**, **banner**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **MOREINFO**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **STARTTIME**, **title**</span><span class="sxs-lookup"><span data-stu-id="e6149-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e6149-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6149-134">Remarks</span></span>

<span data-ttu-id="e6149-135">Este elemento es la construcción fundamental en un metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e6149-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="e6149-136">El elemento de **entrada** y sus atributos asociados definen la metainformación de una única parte lógica de contenido, denominada clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="e6149-137">Los elementos secundarios dentro del ámbito de un elemento de **entrada** definen el contenido multimedia para Windows Media Player que se va a abrir (**ref**), información sobre el clip que Windows Media Player mostrará como texto (**autor**, **Copyright**, **título**) y otras opciones relacionadas con el clip.</span><span class="sxs-lookup"><span data-stu-id="e6149-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="e6149-138">El elemento secundario **ref** vincula el contenido que se va a transmitir para el elemento de **entrada** primario.</span><span class="sxs-lookup"><span data-stu-id="e6149-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="e6149-139">Aunque el script no se interrumpirá, la **entrada** no tiene sentido sin un elemento secundario **ref** .</span><span class="sxs-lookup"><span data-stu-id="e6149-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="e6149-140">Si el valor del atributo **CLIENTSKIP** es no, el usuario no puede saltar adelante más allá del contenido definido por el elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="e6149-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="e6149-141">Esto no funciona si el elemento **ref** secundario hace referencia a otro metarchivo.</span><span class="sxs-lookup"><span data-stu-id="e6149-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="e6149-142">Se debe hacer referencia a los metaarchivos anidados mediante el elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="e6149-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="e6149-143">El atributo **SKIPIFREF** solo pertenece a los elementos de **entrada** que se incluyen en un segundo metarchivo mediante el uso de un elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="e6149-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="e6149-144">El elemento **ENTRYREF** hace referencia a otro metarchivo para la inclusión lógica en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="e6149-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="e6149-145">Si el valor del atributo **SKIPIFREF** de un elemento de **entrada** del archivo de metarchivo al que se hace referencia es sí, Windows Media Player omitirá esta entrada extraída y pasará al siguiente elemento de **entrada** , si existe.</span><span class="sxs-lookup"><span data-stu-id="e6149-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="e6149-146">El siguiente elemento de **entrada** puede ser la siguiente entrada en el archivo original o la entrada siguiente en el metarchivo al que se hace referencia en el elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="e6149-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="e6149-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e6149-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="e6149-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6149-148">Requirements</span></span>



| <span data-ttu-id="e6149-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6149-149">Requirement</span></span> | <span data-ttu-id="e6149-150">Value</span><span class="sxs-lookup"><span data-stu-id="e6149-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="e6149-151">Versión</span><span class="sxs-lookup"><span data-stu-id="e6149-151">Version</span></span><br/> | <span data-ttu-id="e6149-152">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="e6149-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6149-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6149-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6149-154">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e6149-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e6149-155">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e6149-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





