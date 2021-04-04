---
title: Valores de atributo para el contenido de TV
description: Valores de atributo para el contenido de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, contenido de TV
- Valores de atributo de contenido de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076359"
---
# <a name="attribute-values-for-tv-content"></a><span data-ttu-id="84fa8-114">Valores de atributo para el contenido de TV</span><span class="sxs-lookup"><span data-stu-id="84fa8-114">Attribute Values for TV Content</span></span>

<span data-ttu-id="84fa8-115">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84fa8-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="84fa8-116">Windows Media Player 10 o posterior pueden organizar el contenido de la televisión en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="84fa8-116">Windows Media Player 10 or later can organize TV content in the library.</span></span> <span data-ttu-id="84fa8-117">Windows Media Player trata el contenido de TV como subcategoría del contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="84fa8-117">Windows Media Player treats TV content as a subcategory of video content.</span></span> <span data-ttu-id="84fa8-118">Para que el contenido de vídeo aparezca en los nodos de TV de la biblioteca, establezca los atributos **WM/MediaClassPrimaryID** y **WM/MediaClassSecondaryID** en los valores de la tabla siguiente mediante el uso de los *medios*. método **setItemInfo** :</span><span class="sxs-lookup"><span data-stu-id="84fa8-118">To make video content appear in the TV nodes in the library, set the **WM/MediaClassPrimaryID** and the **WM/MediaClassSecondaryID** attributes to the values in the following table by using the *media*.**setItemInfo** method:</span></span>



| <span data-ttu-id="84fa8-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="84fa8-119">Attribute</span></span>                    | <span data-ttu-id="84fa8-120">Value</span><span class="sxs-lookup"><span data-stu-id="84fa8-120">Value</span></span>                                |
|------------------------------|--------------------------------------|
| <span data-ttu-id="84fa8-121">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="84fa8-121">**WM/MediaClassPrimaryID**</span></span>   | <span data-ttu-id="84fa8-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span><span class="sxs-lookup"><span data-stu-id="84fa8-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span></span> |
| <span data-ttu-id="84fa8-123">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="84fa8-123">**WM/MediaClassSecondaryID**</span></span> | <span data-ttu-id="84fa8-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span><span class="sxs-lookup"><span data-stu-id="84fa8-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span></span> |



 

<span data-ttu-id="84fa8-125">También puede usar estos valores para determinar si un determinado elemento multimedia digital contiene contenido de TV mediante el uso de los *medios*. **getItemInfo** o *multimedia*. métodos de **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="84fa8-125">You can also use these values to determine whether a particular digital media item contains TV content by using the *media*.**getItemInfo** or *media*.**getItemInfoByType** methods.</span></span>

<span data-ttu-id="84fa8-126">Recuerde usar los valores de **GUID** como valores de **cadena** al especificar o recuperar estos valores.</span><span class="sxs-lookup"><span data-stu-id="84fa8-126">Remember to use the **GUID** values as **string** values when specifying or retrieving these values.</span></span>

<span data-ttu-id="84fa8-127">El siguiente código de ejemplo de C# establece los atributos de la clase multimedia para que un elemento multimedia se identifique como contenido de TV.</span><span class="sxs-lookup"><span data-stu-id="84fa8-127">The following C# example code sets the media class attributes so that a media item will be identified as TV content.</span></span>


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



<span data-ttu-id="84fa8-128">Para obtener más información sobre los posibles valores de los atributos de la clase multimedia, vea las directrices de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="84fa8-128">For more info about the possible values for the media class attributes, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84fa8-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84fa8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84fa8-130">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="84fa8-130">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="84fa8-131">**Acceso a bibliotecas**</span><span class="sxs-lookup"><span data-stu-id="84fa8-131">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="84fa8-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="84fa8-132">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




