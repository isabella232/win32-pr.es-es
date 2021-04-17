---
title: Vídeo (SDK de Windows Media Player)
description: Vídeo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player las máscaras móviles, vídeo
- máscaras, vídeo
- referencia de las máscaras, vídeo
- vídeo en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705095"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="9fb62-107">Vídeo (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="9fb62-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="9fb62-108">Una pantalla de vídeo permite al usuario ver archivos de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="9fb62-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="9fb62-109">El área de presentación de vídeo solo está visible cuando el vídeo se reproduce o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9fb62-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="9fb62-110">Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga la pantalla del vídeo.</span><span class="sxs-lookup"><span data-stu-id="9fb62-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="9fb62-111">Si no lo hace, es posible que la pantalla de vídeo se superponga sobre cualquier arte visible, como el archivo de fondo, los botones y el trackbars, lo que evitará que el usuario opere con los controles de la máscara.</span><span class="sxs-lookup"><span data-stu-id="9fb62-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="9fb62-112">La sección de vídeo del archivo de definición de máscara debe comenzar con esta línea:</span><span class="sxs-lookup"><span data-stu-id="9fb62-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="9fb62-113">A continuación, debe agregar una línea que especifique la ubicación y el tamaño del área de presentación de vídeo en la máscara.</span><span class="sxs-lookup"><span data-stu-id="9fb62-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="9fb62-114">Puede usar la siguiente plantilla para la sección vídeo del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="9fb62-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="9fb62-115">En las secciones siguientes se proporcionan más detalles.</span><span class="sxs-lookup"><span data-stu-id="9fb62-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="9fb62-116">Ubicación del vídeo</span><span class="sxs-lookup"><span data-stu-id="9fb62-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="9fb62-117">Origen de imagen de vídeo</span><span class="sxs-lookup"><span data-stu-id="9fb62-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="9fb62-118">Tamaño de vídeo</span><span class="sxs-lookup"><span data-stu-id="9fb62-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="9fb62-119">Sección de vídeo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fb62-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="9fb62-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fb62-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fb62-121">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="9fb62-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




