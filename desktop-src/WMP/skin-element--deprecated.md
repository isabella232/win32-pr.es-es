---
title: Elemento SKIN (obsoleto)
description: En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (obsoleto) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660885"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="ce6ce-104">Elemento SKIN (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="ce6ce-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="ce6ce-105">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="ce6ce-106">El elemento **Skin** especifica una dirección URL a un borde.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="ce6ce-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce6ce-107">Attributes</span></span>

<span data-ttu-id="ce6ce-108">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="ce6ce-108">**HREF** (required)</span></span>

<span data-ttu-id="ce6ce-109">Dirección URL de un archivo de borde comprimido con una extensión de nombre de archivo. WMZ.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="ce6ce-110">En Windows Media Player serie 9 o versiones posteriores, este valor solo puede hacer referencia a los archivos de borde del disco duro del usuario ubicado en el mismo directorio que la lista de reproducción del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="ce6ce-111">Vea el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ce6ce-112">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="ce6ce-112">Parent/Child Elements</span></span>



| <span data-ttu-id="ce6ce-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ce6ce-113">Hierarchy</span></span>       | <span data-ttu-id="ce6ce-114">Elementos</span><span class="sxs-lookup"><span data-stu-id="ce6ce-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="ce6ce-115">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ce6ce-115">Parent elements</span></span> | <span data-ttu-id="ce6ce-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-116">**ASX**</span></span>  |
| <span data-ttu-id="ce6ce-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce6ce-117">Child elements</span></span>  | <span data-ttu-id="ce6ce-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ce6ce-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="ce6ce-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce6ce-119">Remarks</span></span>

<span data-ttu-id="ce6ce-120">El elemento **Skin** se usa para crear un borde, que es similar a una máscara, pero que se muestra en el área **reproducción en curso** del Media Player de Windows en modo completo.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="ce6ce-121">El elemento **Skin** solo se usa para los bordes, que aparecen dentro del Media Player de Windows en modo completo y no para las máscaras normales, que reemplazan por completo a la Media Player de Windows en modo compacto.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="ce6ce-122">En un paquete de descarga de Windows Media (con la extensión de nombre de archivo. WMD), el elemento de **máscara** habilita un borde para tener contenido y vincular a otros sitios.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="ce6ce-123">El paquete de descarga de Windows Media es un archivo comprimido que contiene un archivo de borde y un metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="ce6ce-124">El archivo de borde (con la extensión de nombre de archivo. WMZ) se comprime e incluye un archivo de definición de máscara (con una extensión de nombre de archivo. WMS).</span><span class="sxs-lookup"><span data-stu-id="ce6ce-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="ce6ce-125">Un elemento **Skin** tiene tres componentes:</span><span class="sxs-lookup"><span data-stu-id="ce6ce-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="ce6ce-126">Una máscara</span><span class="sxs-lookup"><span data-stu-id="ce6ce-126">A skin</span></span>
-   <span data-ttu-id="ce6ce-127">Algún contenido</span><span class="sxs-lookup"><span data-stu-id="ce6ce-127">Some content</span></span>
-   <span data-ttu-id="ce6ce-128">Un metarchivo</span><span class="sxs-lookup"><span data-stu-id="ce6ce-128">A metafile</span></span>

<span data-ttu-id="ce6ce-129">Las máscaras que se incluyen con los paquetes de descarga de Windows Media deben ser rectangulares.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="ce6ce-130">La creación de bordes con máscaras que no son rectangulares puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="ce6ce-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="ce6ce-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ce6ce-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="ce6ce-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6ce-132">Requirements</span></span>



| <span data-ttu-id="ce6ce-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6ce-133">Requirement</span></span> | <span data-ttu-id="ce6ce-134">Value</span><span class="sxs-lookup"><span data-stu-id="ce6ce-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ce6ce-135">Versión</span><span class="sxs-lookup"><span data-stu-id="ce6ce-135">Version</span></span><br/> | <span data-ttu-id="ce6ce-136">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="ce6ce-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce6ce-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce6ce-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6ce-138">**Bordes de Media Player de Windows (desusado)**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-139">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ce6ce-140">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ce6ce-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





