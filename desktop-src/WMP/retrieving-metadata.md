---
title: Recuperación de metadatos
description: Recuperación de metadatos
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Listas de reproducción de metarchivos de Windows Media, recuperar metadatos
- listas de reproducción, recuperar metadatos
- listas de reproducción de metarchivos, recuperar metadatos
- Listas de reproducción de metarchivos de Windows Media, recuperación de metadatos
- listas de reproducción, recuperación de metadatos
- listas de reproducción de metarchivos, recuperación de metadatos
- metadatos, recuperar
- recuperar metadatos
- Windows Media Player, recuperar metadatos
- Windows Media Player, recuperación de metadatos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994368"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="fc5fa-113">Recuperación de metadatos</span><span class="sxs-lookup"><span data-stu-id="fc5fa-113">Retrieving Metadata</span></span>

<span data-ttu-id="fc5fa-114">Mientras se reproduce un programa o un clip, el script puede recuperar metadatos, como el título y el autor, mediante los métodos **getItemInfo** de los objetos **multimedia** y **lista de reproducción** de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fc5fa-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="fc5fa-115">Puede recuperar los metadatos del ámbito de ASX mediante métodos de objeto de **lista de reproducción** y desde el ámbito de entrada mediante métodos de objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="fc5fa-116">Por ejemplo, para recuperar los valores de AUTHOR, ABSTRACT y PARAM en el siguiente archivo, use el método **getItemInfo** del objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="fc5fa-117">El nombre de atributo es necesario para este método.</span><span class="sxs-lookup"><span data-stu-id="fc5fa-117">The attribute name is required for this method.</span></span> <span data-ttu-id="fc5fa-118">Los nombres de atributo se pueden obtener proporcionando el número de índice a la propiedad **attributeName** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="fc5fa-119">Los índices disponibles para un objeto de **lista de reproducción** se pueden obtener mediante la propiedad **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="fc5fa-120">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc5fa-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="fc5fa-121">Para recuperar los valores del objeto **multimedia** actual en el ámbito de entrada para ref, title, copyright y param ("tres"), use la propiedad **CurrentMedia** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="fc5fa-122">Use la propiedad **attributeCount** del objeto **multimedia** para determinar el número de atributos disponibles para el objeto **multimedia** especificado.</span><span class="sxs-lookup"><span data-stu-id="fc5fa-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="fc5fa-123">Use los números de índice con el método **getItemInfoByAtom** para recuperar los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="fc5fa-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="fc5fa-124">Use los números de índice con el método **getAttributeName** del objeto **multimedia** para determinar los nombres de los atributos disponibles y, a continuación, use los resultados con el método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="fc5fa-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="fc5fa-125">Para obtener un ejemplo del uso de métodos de objetos de Media Player de Windows para recuperar metadatos, vea [playlist. attributeCount](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="fc5fa-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc5fa-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc5fa-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc5fa-127">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="fc5fa-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fc5fa-128">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="fc5fa-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fc5fa-129">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fc5fa-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




