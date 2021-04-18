---
title: Elemento PARAM (WMP SDK)
description: El elemento PARAM define un parámetro personalizado asociado a una lista de reproducción o un elemento de una lista de reproducción.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Elemento PARAM de Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700233"
---
# <a name="param-element"></a><span data-ttu-id="9e517-104">Elemento PARAM</span><span class="sxs-lookup"><span data-stu-id="9e517-104">PARAM Element</span></span>

<span data-ttu-id="9e517-105">El elemento **param** define un parámetro personalizado asociado a una lista de reproducción o un elemento de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9e517-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="9e517-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e517-106">Parameters</span></span>

<span data-ttu-id="9e517-107">Un parámetro también se puede asociar a la presentación en lugar de a un clip individual, colocando este elemento directamente después de la etiqueta **ASX** .</span><span class="sxs-lookup"><span data-stu-id="9e517-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="9e517-108">Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.</span><span class="sxs-lookup"><span data-stu-id="9e517-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="9e517-109">Este elemento **ASX** solo está disponible para Windows Media Player versión 6,01 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9e517-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="9e517-110">La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9e517-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="9e517-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e517-111">Attributes</span></span>

<span data-ttu-id="9e517-112">**NOMBRE**</span><span class="sxs-lookup"><span data-stu-id="9e517-112">**NAME**</span></span>

<span data-ttu-id="9e517-113">Nombre usado para obtener acceso al valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="9e517-113">Name used to access the parameter value.</span></span> <span data-ttu-id="9e517-114">El nombre puede ser cualquier cadena válida.</span><span class="sxs-lookup"><span data-stu-id="9e517-114">The name can be any valid string.</span></span> <span data-ttu-id="9e517-115">Ya se han definido las siguientes cadenas.</span><span class="sxs-lookup"><span data-stu-id="9e517-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="9e517-116">String</span><span class="sxs-lookup"><span data-stu-id="9e517-116">String</span></span>                          | <span data-ttu-id="9e517-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e517-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e517-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="9e517-118">AllowShuffle</span></span>                    | <span data-ttu-id="9e517-119">El atributo **valor** especifica si la lista de reproducción del metarchivo permite a Windows Media Player característica de orden aleatorio para reproducir las entradas en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="9e517-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="9e517-120">El atributo de **valor** se puede establecer en "sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="9e517-121">El valor predeterminado es "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9e517-122">CanPause</span><span class="sxs-lookup"><span data-stu-id="9e517-122">CanPause</span></span>                        | <span data-ttu-id="9e517-123">El atributo **Value** especifica si el usuario puede pausar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9e517-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="9e517-124">El atributo de **valor** se puede establecer en "sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="9e517-125">El valor predeterminado es "Yes".</span><span class="sxs-lookup"><span data-stu-id="9e517-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9e517-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="9e517-126">CanSeek</span></span>                         | <span data-ttu-id="9e517-127">El atributo **valor** especifica si el usuario puede cambiar la posición de reproducción actual mediante la barra de búsqueda, el avance rápido o el retroceso rápido.</span><span class="sxs-lookup"><span data-stu-id="9e517-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="9e517-128">El atributo de **valor** se puede establecer en "sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="9e517-129">El valor predeterminado es "Yes".</span><span class="sxs-lookup"><span data-stu-id="9e517-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9e517-130">CanSkipBack</span><span class="sxs-lookup"><span data-stu-id="9e517-130">CanSkipBack</span></span>                     | <span data-ttu-id="9e517-131">El atributo **valor** especifica si el usuario puede omitir el elemento anterior de la lista de reproducción haciendo clic en **anterior**.</span><span class="sxs-lookup"><span data-stu-id="9e517-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="9e517-132">El atributo de **valor** se puede establecer en "sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="9e517-133">El valor predeterminado es "Yes".</span><span class="sxs-lookup"><span data-stu-id="9e517-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9e517-134">CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="9e517-134">CanSkipForward</span></span>                  | <span data-ttu-id="9e517-135">El atributo **valor** especifica si el usuario puede saltar hacia delante hasta el siguiente elemento de la lista de reproducción haciendo clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9e517-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="9e517-136">El atributo de **valor** se puede establecer en "sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="9e517-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="9e517-137">El valor predeterminado es "Yes".</span><span class="sxs-lookup"><span data-stu-id="9e517-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9e517-138">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="9e517-138">CPRadioID</span></span>                       | <span data-ttu-id="9e517-139">El atributo **Value** especifica el identificador de una fuente de radio proporcionada por un almacén en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="9e517-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="9e517-140">Es decir, el atributo de **valor** debe ser igual que el campo RadioID de una de las fuentes de radio del catálogo de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="9e517-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="9e517-141">El elemento primario es el elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="9e517-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9e517-142">Encoding</span><span class="sxs-lookup"><span data-stu-id="9e517-142">Encoding</span></span>                        | <span data-ttu-id="9e517-143">El atributo de **valor** se establece en "UTF-8" para indicar que el metarchivo es un archivo codificado de Unicode (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="9e517-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9e517-144">HtmlFlink</span><span class="sxs-lookup"><span data-stu-id="9e517-144">HtmlFlink</span></span>                       | <span data-ttu-id="9e517-145">El atributo **Value** es una cadena que proporciona un almacén en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="9e517-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="9e517-146">Windows Media Player pasa la cadena al método [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , que se implementa mediante el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="9e517-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="9e517-147">El método **GetItemInfo** devuelve la dirección URL de la página web que se va a mostrar en el panel **reproducción en curso** del reproductor.</span><span class="sxs-lookup"><span data-stu-id="9e517-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="9e517-148">La página web tiene acceso a todos los métodos que expone el objeto **externo** a los almacenes de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="9e517-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="9e517-149">Para obtener una lista de estos métodos, consulte [objeto externo para las tiendas en línea de tipo 1](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="9e517-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="9e517-150">HTMLView</span><span class="sxs-lookup"><span data-stu-id="9e517-150">HTMLView</span></span>                        | <span data-ttu-id="9e517-151">El atributo **valor** especifica una dirección URL que se muestra en el panel **reproducción en curso** del reproductor en modo completo mientras dure la lista de reproducción o la entrada actual, dependiendo de si el elemento primario es el elemento **ASX** o un elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="9e517-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="9e517-152">HTMLView no es compatible con el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e517-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9e517-153">Log:*FieldName* \[ :*namespace*\]</span><span class="sxs-lookup"><span data-stu-id="9e517-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="9e517-154">El atributo **Value** especifica el valor en el que se establecerá el campo de registro indicado.</span><span class="sxs-lookup"><span data-stu-id="9e517-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="9e517-155">La parte del *espacio de nombres* : del atributo **Name** es opcional.</span><span class="sxs-lookup"><span data-stu-id="9e517-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9e517-156">Búfer</span><span class="sxs-lookup"><span data-stu-id="9e517-156">Prebuffer</span></span>                       | <span data-ttu-id="9e517-157">El atributo **valor** especifica si la siguiente entrada de lista de reproducción comienza el almacenamiento en búfer antes del final de la entrada actual, lo que permite una transición sin problemas.</span><span class="sxs-lookup"><span data-stu-id="9e517-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="9e517-158">El atributo de **valor** se puede establecer en "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="9e517-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9e517-159">ShowWhileBuffering</span><span class="sxs-lookup"><span data-stu-id="9e517-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="9e517-160">El atributo **Value** especifica si un archivo de imagen al que hace referencia el elemento de **entrada** actual continúa mostrándose más allá de su tiempo de duración especificado mientras se almacena en búfer la siguiente entrada de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9e517-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="9e517-161">El atributo de **valor** se puede establecer en "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="9e517-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="9e517-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="9e517-162">**VALUE**</span></span>

<span data-ttu-id="9e517-163">Valor asociado a este parámetro.</span><span class="sxs-lookup"><span data-stu-id="9e517-163">Value associated with this parameter.</span></span> <span data-ttu-id="9e517-164">Puede ser un valor numérico o de cadena.</span><span class="sxs-lookup"><span data-stu-id="9e517-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="9e517-165">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="9e517-165">Parent/Child Elements</span></span>



| <span data-ttu-id="9e517-166">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="9e517-166">Hierarchy</span></span>       | <span data-ttu-id="9e517-167">Elementos</span><span class="sxs-lookup"><span data-stu-id="9e517-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="9e517-168">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9e517-168">Parent elements</span></span> | <span data-ttu-id="9e517-169">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="9e517-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="9e517-170">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9e517-170">Child elements</span></span>  | <span data-ttu-id="9e517-171">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9e517-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="9e517-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e517-172">Remarks</span></span>

<span data-ttu-id="9e517-173">Este elemento permite a los usuarios colocar información adicional sobre cada clip dentro del elemento de **entrada** que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="9e517-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="9e517-174">Para recuperar la información de metadatos especificada en la **entrada** de la lista de reproducción, utilice el *medio*. método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="9e517-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="9e517-175">El *medio*. el método **getItemInfo** recupera el valor del atributo **Value** , dado el nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="9e517-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="9e517-176">Las versiones anteriores de Windows Media Player recuperar la información de metadatos especificada en la **entrada** de la lista de reproducción, mediante el método **GetMediaParameter** dado el nombre del parámetro y un número de índice de la entrada.</span><span class="sxs-lookup"><span data-stu-id="9e517-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="9e517-177">Un parámetro también se puede asociar a la presentación en lugar de a un clip individual, colocando este elemento directamente después de la etiqueta **ASX** .</span><span class="sxs-lookup"><span data-stu-id="9e517-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="9e517-178">Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.</span><span class="sxs-lookup"><span data-stu-id="9e517-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="9e517-179">**Note**</span><span class="sxs-lookup"><span data-stu-id="9e517-179">**Note**</span></span>

<span data-ttu-id="9e517-180">Este elemento **ASX** solo está disponible para Windows Media Player versión 6,01 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9e517-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="9e517-181">La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9e517-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="9e517-182">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9e517-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="9e517-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e517-183">Requirements</span></span>



| <span data-ttu-id="9e517-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e517-184">Requirement</span></span> | <span data-ttu-id="9e517-185">Value</span><span class="sxs-lookup"><span data-stu-id="9e517-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e517-186">Versión</span><span class="sxs-lookup"><span data-stu-id="9e517-186">Version</span></span><br/> | <span data-ttu-id="9e517-187">Windows Media Player versión 7,0 o posterior, se requiere Windows Media Player 9 series o posterior para los atributos de nombre predefinidos, se requiere Windows Media Player 10 o posterior para los nombres predefinidos CanPause, CanSeek, CanSkipBack y CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="9e517-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e517-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e517-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e517-189">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="9e517-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="9e517-190">**Datos de la secuencia de registro**</span><span class="sxs-lookup"><span data-stu-id="9e517-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="9e517-191">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9e517-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9e517-192">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9e517-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





