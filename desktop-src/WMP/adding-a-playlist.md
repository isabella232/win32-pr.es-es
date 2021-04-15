---
title: Agregar una lista de reproducción
description: Agregar una lista de reproducción
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- crear máscaras, listas de reproducción
- Máscaras de Windows Media Player, listas de reproducción
- máscaras, listas de reproducción
- listas de reproducción, máscaras
- listas de reproducción de metarchivos, máscaras
- Listas de reproducción de metarchivos de Windows Media, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695404"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="828ec-109">Agregar una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="828ec-109">Adding a Playlist</span></span>

<span data-ttu-id="828ec-110">Puede usar listas de reproducción para elegir entre las recopilaciones de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="828ec-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="828ec-111">Con la ilustración de la primera máscara, puede realizar algunos cambios en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="828ec-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="828ec-112">El primer paso es usar el shell que usará para la mayoría de las máscaras:</span><span class="sxs-lookup"><span data-stu-id="828ec-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="828ec-113">Ahora, agregue una segunda **vista** que contenga una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="828ec-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="828ec-114">Coloque el código siguiente después del </VIEW> del código de Shell.</span><span class="sxs-lookup"><span data-stu-id="828ec-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="828ec-115">Tendrá que dar un identificador a esta segunda vista para poder hacer referencia a ella más adelante.</span><span class="sxs-lookup"><span data-stu-id="828ec-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="828ec-116">Agregue un PLAYELEMENT y un STOPELEMENT.</span><span class="sxs-lookup"><span data-stu-id="828ec-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="828ec-117">Estos botones predefinidos facilitan la vida.</span><span class="sxs-lookup"><span data-stu-id="828ec-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="828ec-118">Por último, agregue un evento onClick a PLAYELEMENT para mostrar una lista de reproducción en la segunda vista:</span><span class="sxs-lookup"><span data-stu-id="828ec-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="828ec-119">Puede ver una máscara de lista de reproducción en funcionamiento similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="828ec-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="828ec-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="828ec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="828ec-121">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="828ec-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




