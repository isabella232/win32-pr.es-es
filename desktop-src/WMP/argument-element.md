---
title: Elemento argument
description: El elemento argument contiene una parte de una cadena de condición.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Elemento argument de Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699801"
---
# <a name="argument-element"></a><span data-ttu-id="82857-104">Elemento argument</span><span class="sxs-lookup"><span data-stu-id="82857-104">argument Element</span></span>

<span data-ttu-id="82857-105">El elemento **argument** contiene una parte de una cadena de condición.</span><span class="sxs-lookup"><span data-stu-id="82857-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="82857-106">Normalmente, una cadena de condición tiene una parte de condición y una parte de valor.</span><span class="sxs-lookup"><span data-stu-id="82857-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="82857-107">Por ejemplo, en la cadena de condición "artista Equals Joe", la parte de la condición es "Equals" y la parte del valor es "Joe".</span><span class="sxs-lookup"><span data-stu-id="82857-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="82857-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="82857-108">Attributes</span></span>

<span data-ttu-id="82857-109">**nombre** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="82857-109">**name** (required)</span></span>

<span data-ttu-id="82857-110">Nombre de una parte de la cadena de condición.</span><span class="sxs-lookup"><span data-stu-id="82857-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="82857-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="82857-111">Parent/Child Elements</span></span>



| <span data-ttu-id="82857-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="82857-112">Hierarchy</span></span> | <span data-ttu-id="82857-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="82857-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="82857-114">Parent</span><span class="sxs-lookup"><span data-stu-id="82857-114">Parent</span></span>    | [<span data-ttu-id="82857-115">Fragment</span><span class="sxs-lookup"><span data-stu-id="82857-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="82857-116">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="82857-116">Child</span></span>     | <span data-ttu-id="82857-117">None</span><span class="sxs-lookup"><span data-stu-id="82857-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="82857-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82857-118">Remarks</span></span>

<span data-ttu-id="82857-119">Cuando el atributo **Name** de un elemento **Fragment** es una característica de elemento multimedia como el intérprete del álbum, o el género, el elemento **Fragment** debe contener dos elementos **argument** : uno que especifique una condición y otro que especifique un valor.</span><span class="sxs-lookup"><span data-stu-id="82857-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="82857-120">En la tabla siguiente se muestran dos valores posibles para el atributo **Name** y cómo se usan los elementos **argument** para especificar condiciones y valores.</span><span class="sxs-lookup"><span data-stu-id="82857-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82857-121">Valor del atributo</span><span class="sxs-lookup"><span data-stu-id="82857-121">Attribute value</span></span></th>
<th><span data-ttu-id="82857-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="82857-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82857-123">Condición</span><span class="sxs-lookup"><span data-stu-id="82857-123">Condition</span></span></td>
<td><span data-ttu-id="82857-124">El contenido del elemento <strong>argument</strong> es la parte de la condición de una cadena de condición.</span><span class="sxs-lookup"><span data-stu-id="82857-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="82857-125">Por ejemplo, en el intérprete de la cadena de condición es &quot; igual a Joe &quot; , la parte de la condición es &quot; igual a &quot; .</span><span class="sxs-lookup"><span data-stu-id="82857-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="82857-126">La parte de la condición de una cadena de condición debe ser uno de los siguientes: es igual a, no es igual a, contiene, no contiene, es menor que, es mayor que, es, no es, es anterior, es posterior a, es más reciente que, más abajo, ascendente, descendente, aleatorio, es al menos, no es más que.</span><span class="sxs-lookup"><span data-stu-id="82857-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82857-127">Value</span><span class="sxs-lookup"><span data-stu-id="82857-127">Value</span></span></td>
<td><span data-ttu-id="82857-128">El contenido del elemento <strong>argument</strong> es la parte del valor de una cadena de condición.</span><span class="sxs-lookup"><span data-stu-id="82857-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="82857-129">Por ejemplo, en el intérprete de la cadena de condición es &quot; igual a Joe &quot; , la parte del valor es &quot; Joe &quot; . Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82857-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82857-130">Cuando el atributo **Name** de un elemento **Fragment** es "Limit total size to" o "Limit total Duration to", el elemento **Fragment** debe contener dos elementos **argument** : uno que especifique un formato y otro que especifique un número.</span><span class="sxs-lookup"><span data-stu-id="82857-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="82857-131">En la tabla siguiente se muestran dos valores posibles para el atributo **Name** y cómo se usan los elementos **argument** para limitar el tamaño o la duración de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="82857-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82857-132">Valor del atributo</span><span class="sxs-lookup"><span data-stu-id="82857-132">Attribute value</span></span></th>
<th><span data-ttu-id="82857-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="82857-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82857-134">Formato</span><span class="sxs-lookup"><span data-stu-id="82857-134">Format</span></span></td>
<td><span data-ttu-id="82857-135">Cuando el atributo <strong>Name</strong> del elemento <strong>Fragment</strong> tiene el &quot; límite de tamaño total en &quot; , el contenido del elemento <strong>argument</strong> debe ser uno de los siguientes: kilobytes, megabytes o gigabytes. cuando el atributo <strong>Name</strong> del elemento <strong>Fragment</strong> es &quot; Limit total Duration to &quot; , el contenido del elemento <strong>argument</strong> debe ser uno de los siguientes: segundos, minutos, horas o días.</span><span class="sxs-lookup"><span data-stu-id="82857-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82857-136">Number</span><span class="sxs-lookup"><span data-stu-id="82857-136">Number</span></span></td>
<td><span data-ttu-id="82857-137">El contenido del elemento <strong>argument</strong> es un número que limita el tamaño o la duración de la lista de reproducción. Example</span><span class="sxs-lookup"><span data-stu-id="82857-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82857-138">Cuando el atributo **Name** de un elemento **Fragment** es "Limit Number of items", el elemento **Fragment** debe contener un elemento **argument** que especifique el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="82857-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="82857-139">En la tabla siguiente se muestra cómo utilizar el valor numérico del atributo **Name** .</span><span class="sxs-lookup"><span data-stu-id="82857-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82857-140">Valor del atributo</span><span class="sxs-lookup"><span data-stu-id="82857-140">Attribute value</span></span></th>
<th><span data-ttu-id="82857-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="82857-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82857-142">Number</span><span class="sxs-lookup"><span data-stu-id="82857-142">Number</span></span></td>
<td><span data-ttu-id="82857-143">El contenido del elemento <strong>argument</strong> es un número que limita el número de elementos de una lista de reproducción. Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82857-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="82857-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82857-144">Requirements</span></span>



| <span data-ttu-id="82857-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="82857-145">Requirement</span></span> | <span data-ttu-id="82857-146">Value</span><span class="sxs-lookup"><span data-stu-id="82857-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="82857-147">Versión</span><span class="sxs-lookup"><span data-stu-id="82857-147">Version</span></span><br/> | <span data-ttu-id="82857-148">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="82857-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82857-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="82857-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82857-150">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="82857-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="82857-151">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="82857-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





