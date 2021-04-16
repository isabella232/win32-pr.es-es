---
title: Elemento BANNER
description: El elemento BANNER define una dirección URL a un archivo gráfico que aparecerá en el panel de información.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento de pancarta Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700009"
---
# <a name="banner-element"></a><span data-ttu-id="0cd20-104">Elemento BANNER</span><span class="sxs-lookup"><span data-stu-id="0cd20-104">BANNER Element</span></span>

<span data-ttu-id="0cd20-105">El elemento **banner** define una dirección URL a un archivo gráfico que aparecerá en el panel de información.</span><span class="sxs-lookup"><span data-stu-id="0cd20-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="0cd20-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cd20-106">Attributes</span></span>

<span data-ttu-id="0cd20-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="0cd20-107">**HREF** (required)</span></span>

<span data-ttu-id="0cd20-108">Dirección URL de un archivo gráfico que se muestra en el panel de información.</span><span class="sxs-lookup"><span data-stu-id="0cd20-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0cd20-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="0cd20-109">Parent/Child Elements</span></span>



| <span data-ttu-id="0cd20-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="0cd20-110">Hierarchy</span></span>       | <span data-ttu-id="0cd20-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="0cd20-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="0cd20-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0cd20-112">Parent elements</span></span> | <span data-ttu-id="0cd20-113">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="0cd20-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="0cd20-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0cd20-114">Child elements</span></span>  | <span data-ttu-id="0cd20-115">**abstract**, **MOREINFO**</span><span class="sxs-lookup"><span data-stu-id="0cd20-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0cd20-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cd20-116">Remarks</span></span>

<span data-ttu-id="0cd20-117">Este elemento define una dirección URL a un archivo gráfico que aparece en el panel de información de Media Player de Windows, debajo del contenido del vídeo.</span><span class="sxs-lookup"><span data-stu-id="0cd20-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="0cd20-118">Si el medio es solo audio, el gráfico de banner se muestra por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="0cd20-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="0cd20-119">Windows Media Player reserva un espacio de 32 píxeles de alto por 194 píxeles de ancho (la barra de pancarta) para el gráfico.</span><span class="sxs-lookup"><span data-stu-id="0cd20-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="0cd20-120">Si el gráfico definido en la dirección URL es menor que ese, se muestra en su tamaño original.</span><span class="sxs-lookup"><span data-stu-id="0cd20-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="0cd20-121">Si el gráfico es mayor que el espacio reservado, Windows Media Player recortará la imagen para que quepa en el espacio.</span><span class="sxs-lookup"><span data-stu-id="0cd20-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="0cd20-122">Puede usar un elemento **abstracto** dentro del ámbito del elemento **banner** para mostrar texto como información sobre herramientas cuando el usuario detiene el puntero del mouse sobre el gráfico del banner.</span><span class="sxs-lookup"><span data-stu-id="0cd20-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="0cd20-123">Un elemento **MOREINFO** dentro de un elemento **banner** define una dirección URL a la que se realiza el usuario cuando el usuario hace clic en el gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="0cd20-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="0cd20-124">(La dirección URL puede ser cualquier ruta de acceso o protocolo, como un vínculo de correo electrónico, una dirección URL del Protocolo de transferencia de hipertexto (HTTP) a un sitio web o incluso un comando de Microsoft JScript). Cuando el puntero se mueve sobre el gráfico, el gráfico se vuelve a relieve y tiene el aspecto de un botón.</span><span class="sxs-lookup"><span data-stu-id="0cd20-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="0cd20-125">Un elemento **banner** definido para un elemento **ASX** se muestra mientras se reproducen todos los clips de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0cd20-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="0cd20-126">Un elemento **banner** definido en un elemento **entry** solo se muestra mientras se reproduce el clip y, durante ese tiempo, reemplaza cualquier banner definido en el elemento **ASX** primario.</span><span class="sxs-lookup"><span data-stu-id="0cd20-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="0cd20-127">Puede especificar cómo reserva Windows Media Player el espacio para el banner estableciendo el atributo **BANNERBAR** del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="0cd20-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="0cd20-128">Las imágenes de banner no son compatibles con los archivos DRM o cuando Windows Media Player está incrustado en una página web.</span><span class="sxs-lookup"><span data-stu-id="0cd20-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="0cd20-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0cd20-129">Examples</span></span>

<span data-ttu-id="0cd20-130">El siguiente es un ejemplo de un elemento **banner** sin elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="0cd20-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="0cd20-131">A continuación se incluye un ejemplo de un elemento **banner** que contiene elementos **abstractos** y **MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="0cd20-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="0cd20-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd20-132">Requirements</span></span>



| <span data-ttu-id="0cd20-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd20-133">Requirement</span></span> | <span data-ttu-id="0cd20-134">Value</span><span class="sxs-lookup"><span data-stu-id="0cd20-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0cd20-135">Versión</span><span class="sxs-lookup"><span data-stu-id="0cd20-135">Version</span></span><br/> | <span data-ttu-id="0cd20-136">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0cd20-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cd20-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cd20-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd20-138">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0cd20-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0cd20-139">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0cd20-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





