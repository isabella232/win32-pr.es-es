---
title: Usar URL y sustitución de servidor
description: Usar URL y sustitución de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Listas de reproducción de metarchivos de Windows Media, sustitución de direcciones URL
- listas de reproducción, sustitución de direcciones URL
- listas de reproducción de metarchivos, sustitución de direcciones URL
- Listas de reproducción de metarchivos de Windows Media, sustituciones de servidor
- listas de reproducción, sustitución de servidor
- listas de reproducción de metarchivos, sustitución de servidor
- Listas de reproducción de metarchivos de Windows Media, sustitución de protocolo
- listas de reproducción, sustitución de protocolo
- listas de reproducción de metarchivos, sustitución de protocolo
- Windows Media Player, sustitución de direcciones URL
- Windows Media Player, sustitución de servidor
- Windows Media Player, sustitución de protocolos
- Sustitución de direcciones URL
- sustituciones de servidor
- sustituciones de protocolo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357167"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="45749-118">Usar URL y sustitución de servidor</span><span class="sxs-lookup"><span data-stu-id="45749-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="45749-119">Puede usar listas de reproducción de metarchivos para proporcionar un medio de propagación automática a orígenes de contenido alternativo cuando no se puede tener acceso a una secuencia o reproducirla.</span><span class="sxs-lookup"><span data-stu-id="45749-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="45749-120">Puede usar este método de sustitución incremental para especificar orígenes del mismo contenido en distintos servidores o en diferentes tipos de servidores.</span><span class="sxs-lookup"><span data-stu-id="45749-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="45749-121">Por ejemplo, puede especificar una primera alternativa en otro servidor de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="45749-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="45749-122">Si no se puede reproducir el contenido, el cliente puede pasar a una segunda alternativa en un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="45749-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="45749-123">Windows Media Player intenta revertir automáticamente a protocolos diferentes según su configuración de propiedades de Windows Media antes de probar las direcciones URL de sustitución en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="45749-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="45749-124">Establezca la sustitución de servidor y protocolo colocando varios elementos **ref** en sucesión dentro de un elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="45749-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="45749-125">Cada elemento **ref** especifica una ubicación alternativa o protocolo para un archivo multimedia o una secuencia.</span><span class="sxs-lookup"><span data-stu-id="45749-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="45749-126">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="45749-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="45749-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45749-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45749-128">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="45749-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="45749-129">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="45749-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




