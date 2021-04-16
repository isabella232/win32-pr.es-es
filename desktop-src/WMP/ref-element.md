---
title: Elemento REF
description: El elemento REF especifica una dirección URL para el contenido multimedia digital.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF de Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708795"
---
# <a name="ref-element"></a><span data-ttu-id="281d9-104">Elemento REF</span><span class="sxs-lookup"><span data-stu-id="281d9-104">REF Element</span></span>

<span data-ttu-id="281d9-105">El elemento **ref** especifica una dirección URL para el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="281d9-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="281d9-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="281d9-106">Attributes</span></span>

<span data-ttu-id="281d9-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="281d9-107">**HREF** (required)</span></span>

<span data-ttu-id="281d9-108">Dirección URL a cualquier parte del contenido multimedia compatible con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="281d9-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="281d9-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="281d9-109">Parent/Child Elements</span></span>



| <span data-ttu-id="281d9-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="281d9-110">Hierarchy</span></span>       | <span data-ttu-id="281d9-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="281d9-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="281d9-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="281d9-112">Parent elements</span></span> | <span data-ttu-id="281d9-113">**MOVIMIENTOS**</span><span class="sxs-lookup"><span data-stu-id="281d9-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="281d9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="281d9-114">Child elements</span></span>  | <span data-ttu-id="281d9-115">**Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span><span class="sxs-lookup"><span data-stu-id="281d9-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="281d9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="281d9-116">Remarks</span></span>

<span data-ttu-id="281d9-117">Este elemento especifica una dirección URL para un fragmento de contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="281d9-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="281d9-118">La dirección URL puede apuntar a cualquier tipo de medio admitido, mediante cualquier protocolo compatible con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="281d9-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="281d9-119">Entre los tipos de medios admitidos se incluyen imágenes fijas como imágenes. gif y. jpg y archivos Flash con una extensión de nombre de archivo. SWF.</span><span class="sxs-lookup"><span data-stu-id="281d9-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="281d9-120">Estos tipos de medios son útiles para incluir contenido de publicidad en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="281d9-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="281d9-121">Con los archivos de imagen y los archivos Flash que se reproducen en un bucle, también debe especificar la cantidad de tiempo que se va a mostrar el elemento multimedia incluyendo un elemento **Duration** en el elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="281d9-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="281d9-122">Si desea que una imagen continúe mostrándose mientras se almacena en búfer la siguiente entrada de la lista de reproducción, incluya un elemento **param** en el elemento **entry** , establezca su atributo **Name** en ShowWhileBuffering y establezca su atributo **Value** en true.</span><span class="sxs-lookup"><span data-stu-id="281d9-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="281d9-123">Para hacer referencia al contenido de un CD o DVD que lo permita, se proporcionan los protocolos wmpcd y wmpdvd.</span><span class="sxs-lookup"><span data-stu-id="281d9-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="281d9-124">Por ejemplo, si se establece el atributo **href** en "wmpdvd://f/5/3", se reproducirá el capítulo 3 del título 5 en un DVD, pero solo si se ha creado el DVD para permitirlo.</span><span class="sxs-lookup"><span data-stu-id="281d9-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="281d9-125">Las aplicaciones que abren archivos multimedia digitales desde detrás de un firewall tendrán un mejor rendimiento al abrir los elementos multimedia si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="281d9-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="281d9-126">El uso más común de este elemento es para la sustitución de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="281d9-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="281d9-127">Si Windows Media Player no puede abrir un fragmento de medio definido en un elemento **ref** , intentará la dirección URL en el siguiente elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="281d9-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="281d9-128">Una vez que Windows Media Player abre el contenido multimedia desde una dirección URL definida dentro del ámbito de un elemento de **entrada** , omite las siguientes etiquetas de **referencia** en el elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="281d9-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="281d9-129">Una vez finalizada la reproducción de la parte del contenido, Windows Media Player pasa al siguiente elemento de **entrada** , si existe.</span><span class="sxs-lookup"><span data-stu-id="281d9-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="281d9-130">**Importante** Una vez que Windows Media Player establece una conexión a una parte de contenido a la que se hace referencia, omite todos los demás elementos **ref** de esa **entrada**, tanto si la conexión finaliza con normalidad o de forma anómala.</span><span class="sxs-lookup"><span data-stu-id="281d9-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="281d9-131">Si el elemento multimedia al que se hace referencia es un archivo de imagen, se debe usar el elemento **Duration** para especificar el tiempo de visualización de la imagen.</span><span class="sxs-lookup"><span data-stu-id="281d9-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="281d9-132">**Note**</span><span class="sxs-lookup"><span data-stu-id="281d9-132">**Note**</span></span>

<span data-ttu-id="281d9-133">Si intenta reproducir medios Flash que incluyen sonido con el primer fotograma, se pueden producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="281d9-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="281d9-134">Debe crear contenido de Flash para reproducir el sonido a partir del segundo fotograma.</span><span class="sxs-lookup"><span data-stu-id="281d9-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="281d9-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="281d9-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="281d9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="281d9-136">Requirements</span></span>



| <span data-ttu-id="281d9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="281d9-137">Requirement</span></span> | <span data-ttu-id="281d9-138">Value</span><span class="sxs-lookup"><span data-stu-id="281d9-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="281d9-139">Versión</span><span class="sxs-lookup"><span data-stu-id="281d9-139">Version</span></span><br/> | <span data-ttu-id="281d9-140">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="281d9-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="281d9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="281d9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281d9-142">**Tipos de archivos y protocolos admitidos**</span><span class="sxs-lookup"><span data-stu-id="281d9-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="281d9-143">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="281d9-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="281d9-144">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="281d9-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





