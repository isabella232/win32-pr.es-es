---
title: Agregar vídeo
description: Agregar vídeo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- crear máscaras, vídeo
- Máscaras de Windows Media Player, vídeo
- máscaras, vídeo
- vídeo en máscaras, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695312"
---
# <a name="adding-video"></a><span data-ttu-id="7faa8-107">Agregar vídeo</span><span class="sxs-lookup"><span data-stu-id="7faa8-107">Adding Video</span></span>

<span data-ttu-id="7faa8-108">Puede Agregar un vídeo al archivo simplemente mediante el elemento de **vídeo** y definiendo dónde desea colocar la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7faa8-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="7faa8-109">Use el mismo código que en la sección elegir archivos; lo único que debe hacer es agregar el elemento de **vídeo** con los atributos superior, izquierdo, ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="7faa8-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="7faa8-110">Cuando reproduzca un vídeo, se mostrará en la ventana.</span><span class="sxs-lookup"><span data-stu-id="7faa8-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="7faa8-111">La imagen del ejemplo de vídeo se ha modificado para crear una máscara ligeramente más grande.</span><span class="sxs-lookup"><span data-stu-id="7faa8-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="7faa8-112">Dado que las capas se usaron en Photoshop, los botones se movieron fácilmente y se creó un nuevo conjunto con mucha rapidez.</span><span class="sxs-lookup"><span data-stu-id="7faa8-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="7faa8-113">Solo se ha cambiado la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="7faa8-113">Only the background image was changed.</span></span> <span data-ttu-id="7faa8-114">Se usó un relleno en una capa en blanco y se agregó un efecto de bisel y de relieve.</span><span class="sxs-lookup"><span data-stu-id="7faa8-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="7faa8-115">Puede ver una máscara de vídeo similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="7faa8-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7faa8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7faa8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7faa8-117">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="7faa8-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




