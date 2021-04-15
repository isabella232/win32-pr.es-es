---
title: Elemento MOREINFO
description: El elemento MOREINFO especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un programa, un clip o un banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO Media Player Windows
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708261"
---
# <a name="moreinfo-element"></a><span data-ttu-id="c521b-104">Elemento MOREINFO</span><span class="sxs-lookup"><span data-stu-id="c521b-104">MOREINFO Element</span></span>

<span data-ttu-id="c521b-105">El elemento **MOREINFO** especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un programa, un clip o un banner.</span><span class="sxs-lookup"><span data-stu-id="c521b-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="c521b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c521b-106">Attributes</span></span>

<span data-ttu-id="c521b-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="c521b-107">**HREF** (required)</span></span>

<span data-ttu-id="c521b-108">Dirección URL de un sitio web, una dirección de correo electrónico o un comando de script.</span><span class="sxs-lookup"><span data-stu-id="c521b-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="c521b-109">**DIRIGIR**</span><span class="sxs-lookup"><span data-stu-id="c521b-109">**TARGET**</span></span>

<span data-ttu-id="c521b-110">Valor que define el marco o la ventana en la que el explorador abrirá la página definida por el atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="c521b-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="c521b-111">Puede ser una cadena que contenga un nombre de ventana o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c521b-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="c521b-112">Value</span><span class="sxs-lookup"><span data-stu-id="c521b-112">Value</span></span>    | <span data-ttu-id="c521b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c521b-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c521b-114">\_en blanco</span><span class="sxs-lookup"><span data-stu-id="c521b-114">\_blank</span></span>  | <span data-ttu-id="c521b-115">El documento se carga en una nueva ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="c521b-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="c521b-116">\_self</span><span class="sxs-lookup"><span data-stu-id="c521b-116">\_self</span></span>   | <span data-ttu-id="c521b-117">El documento se carga en el mismo marco que el documento actual que contiene el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c521b-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="c521b-118">\_aérea</span><span class="sxs-lookup"><span data-stu-id="c521b-118">\_parent</span></span> | <span data-ttu-id="c521b-119">El documento se carga en el marco primario inmediato del fotograma actual o en el fotograma actual si no hay ningún marco primario.</span><span class="sxs-lookup"><span data-stu-id="c521b-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="c521b-120">\_Arriba</span><span class="sxs-lookup"><span data-stu-id="c521b-120">\_top</span></span>    | <span data-ttu-id="c521b-121">El documento se carga en la ventana completa del explorador, reemplazando todos los demás marcos o documentos.</span><span class="sxs-lookup"><span data-stu-id="c521b-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="c521b-122">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="c521b-122">Parent/Child Elements</span></span>



| <span data-ttu-id="c521b-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="c521b-123">Hierarchy</span></span>       | <span data-ttu-id="c521b-124">Elementos</span><span class="sxs-lookup"><span data-stu-id="c521b-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="c521b-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c521b-125">Parent elements</span></span> | <span data-ttu-id="c521b-126">**ASX**, **entrada**, **banner**</span><span class="sxs-lookup"><span data-stu-id="c521b-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="c521b-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c521b-127">Child elements</span></span>  | <span data-ttu-id="c521b-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c521b-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="c521b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c521b-129">Remarks</span></span>

<span data-ttu-id="c521b-130">Este elemento especifica una dirección URL a un sitio web, una dirección de correo electrónico **o un comando de script. El usuario puede tener acceso al destino de la dirección URL haciendo clic en el gráfico o en el texto asociado con el elemento MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="c521b-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="c521b-131">Los detalles dependen del elemento primario del elemento **MOREINFO** :</span><span class="sxs-lookup"><span data-stu-id="c521b-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="c521b-132">Si el elemento **MOREINFO** es el elemento secundario de un elemento **ASX** , el usuario puede tener acceso a la dirección URL haciendo clic en el título Mostrar.</span><span class="sxs-lookup"><span data-stu-id="c521b-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="c521b-133">Si el elemento **MOREINFO** es el elemento secundario de un elemento **entry** , el usuario puede tener acceso a la dirección URL haciendo clic en el título del clip.</span><span class="sxs-lookup"><span data-stu-id="c521b-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="c521b-134">Si el elemento **MOREINFO** es el elemento secundario de un elemento **banner** , el usuario puede tener acceso a la dirección URL haciendo clic en el gráfico de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c521b-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="c521b-135">Si el atributo **href** especifica una dirección URL a un sitio web, el explorador se abrirá y navegará a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c521b-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="c521b-136">Si el atributo **href** especifica una dirección de correo electrónico, se inicia la aplicación de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="c521b-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="c521b-137">Si el atributo **href** especifica un comando de script, el comando de script se ejecuta en el explorador.</span><span class="sxs-lookup"><span data-stu-id="c521b-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="c521b-138">**Note**</span><span class="sxs-lookup"><span data-stu-id="c521b-138">**Note**</span></span>

<span data-ttu-id="c521b-139">Si el elemento **MOREINFO** aparece dentro de un elemento **ASX** o **entry** , cuando el cursor del mouse se mantiene sobre el título de la presentación (para un elemento **ASX** ) o un recorte (para un elemento de **entrada** ), Windows Media Player puede seleccionar la dirección URL definida en el atributo **href** y obtener acceso a ella.</span><span class="sxs-lookup"><span data-stu-id="c521b-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="c521b-140">El atributo de **destino** define el marco o la ventana en la que el explorador abrirá la página definida por el atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="c521b-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="c521b-141">Los valores de este atributo siguen la sintaxis y las definiciones HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="c521b-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="c521b-142">En el caso de un control incrustado en una página web, si no se define ningún atributo de **destino** , la dirección URL carga la ventana del explorador actual y reemplaza la página existente, lo que significa que el contenido deja de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="c521b-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="c521b-143">Por lo tanto, se recomienda especificar siempre un atributo de **destino** al insertar el control Media Player de Windows en una página web.</span><span class="sxs-lookup"><span data-stu-id="c521b-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="c521b-144">Si el metarchivo está abierto en el Media Player de Windows independiente, se omite el atributo de **destino** y la dirección URL se carga en una ventana del explorador existente.</span><span class="sxs-lookup"><span data-stu-id="c521b-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="c521b-145">Si no hay ninguna ventana del explorador abierta actualmente, la dirección URL se carga en una nueva ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="c521b-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="c521b-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c521b-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="c521b-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c521b-147">Requirements</span></span>



| <span data-ttu-id="c521b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c521b-148">Requirement</span></span> | <span data-ttu-id="c521b-149">Value</span><span class="sxs-lookup"><span data-stu-id="c521b-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="c521b-150">Versión</span><span class="sxs-lookup"><span data-stu-id="c521b-150">Version</span></span><br/> | <span data-ttu-id="c521b-151">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="c521b-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c521b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="c521b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c521b-153">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c521b-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c521b-154">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c521b-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





