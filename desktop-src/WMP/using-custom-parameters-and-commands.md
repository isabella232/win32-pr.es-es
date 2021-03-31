---
title: Usar parámetros y comandos personalizados
description: Usar parámetros y comandos personalizados
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Listas de reproducción de metarchivos de Windows Media, parámetros personalizados
- listas de reproducción, parámetros personalizados
- listas de reproducción de metarchivos, parámetros personalizados
- Listas de reproducción de metarchivos de Windows Media, comandos personalizados
- listas de reproducción, comandos personalizados
- listas de reproducción de metarchivos, comandos personalizados
- Listas de reproducción de metarchivos de Windows Media, parámetros
- listas de reproducción, parámetros
- listas de reproducción de metarchivos, parámetros
- parámetros personalizados
- comandos personalizados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903565"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="6afac-114">Usar parámetros y comandos personalizados</span><span class="sxs-lookup"><span data-stu-id="6afac-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="6afac-115">Puede crear parámetros personalizados para pasar metadatos adicionales en una lista de reproducción de metarchivo mediante el elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="6afac-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="6afac-116">Use el atributo **Name** del elemento **param** para definir el nombre del parámetro personalizado.</span><span class="sxs-lookup"><span data-stu-id="6afac-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="6afac-117">Use el atributo **Value** para definir el valor del parámetro personalizado con nombre.</span><span class="sxs-lookup"><span data-stu-id="6afac-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="6afac-118">Recupere los metadatos del **parámetro** mediante los métodos **getItemInfo** de los objetos **multimedia** y de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="6afac-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="6afac-119">Para obtener un ejemplo del uso de estos métodos para recuperar metadatos, vea el método [attributeCount](playlist-attributecount.md) del objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="6afac-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="6afac-120">En la siguiente lista de reproducción de metarchivo de ejemplo se muestra el uso del elemento **param** para definir los parámetros personalizados.</span><span class="sxs-lookup"><span data-stu-id="6afac-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="6afac-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6afac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6afac-122">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="6afac-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




