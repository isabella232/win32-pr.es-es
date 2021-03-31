---
title: Archivo insertado
description: Archivo insertado
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos insertados
- Máscaras móviles de Windows Media Player, archivos insertados
- máscaras, archivos insertados
- Archivos insertados en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418785"
---
# <a name="pushed-file"></a><span data-ttu-id="bd18a-110">Archivo insertado</span><span class="sxs-lookup"><span data-stu-id="bd18a-110">Pushed File</span></span>

<span data-ttu-id="bd18a-111">El archivo insertado contiene las imágenes que se mostrarán cuando el usuario puntee en un botón.</span><span class="sxs-lookup"><span data-stu-id="bd18a-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="bd18a-112">También puede incluir las imágenes normales e insertadas para el estado de pausa del botón PlayPause.</span><span class="sxs-lookup"><span data-stu-id="bd18a-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="bd18a-113">La siguiente imagen es un archivo insertado típico.</span><span class="sxs-lookup"><span data-stu-id="bd18a-113">The following image is a typical Pushed file.</span></span>

![archivo insertado](images/cesdkpus.png)

<span data-ttu-id="bd18a-115">Esto almacena las imágenes que se mostrarán cuando se PUNTEEN los botones de tipo de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="bd18a-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="bd18a-116">También se almacenan en este archivo las imágenes normales e insertadas para la imagen en pausa del botón PlayPause.</span><span class="sxs-lookup"><span data-stu-id="bd18a-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="bd18a-117">Excepto en el caso de las imágenes secundarias de PlayPause a la derecha, las demás imágenes de botón se alinean con la imagen de fondo mediante el desplazamiento definido en la sección de mapas de bits del archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="bd18a-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="bd18a-118">Observe que el fondo de la imagen del botón coincide exactamente con el área correspondiente en el archivo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bd18a-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="bd18a-119">Esto es importante, porque cuando el usuario pulsa un botón de tipo de posicionamiento, el rectángulo completo definido para la imagen insertada reemplazará el área de coincidencia en el archivo de fondo.</span><span class="sxs-lookup"><span data-stu-id="bd18a-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="bd18a-120">Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo cambian las partes del botón que desea que aparezcan de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="bd18a-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd18a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd18a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd18a-122">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="bd18a-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




