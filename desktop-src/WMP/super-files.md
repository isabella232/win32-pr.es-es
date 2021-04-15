---
title: Súper archivos
description: Súper archivos
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos de súper archivos
- Aspectos de Windows Media Player Mobile, archivos de superarchivos
- máscaras, súper archivos
- Súper archivos en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714219"
---
# <a name="super-files"></a><span data-ttu-id="83969-110">Súper archivos</span><span class="sxs-lookup"><span data-stu-id="83969-110">Super Files</span></span>

<span data-ttu-id="83969-111">Los súper archivos se usan para almacenar las imágenes deshabilitadas para trackbars.</span><span class="sxs-lookup"><span data-stu-id="83969-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="83969-112">Dado que la imagen principal de la barra de desplazamiento se muestra en el archivo de fondo y el usuario pulsa la imagen Thumb, no la imagen de TrackBar, solo se necesita la imagen deshabilitada para trackbars.</span><span class="sxs-lookup"><span data-stu-id="83969-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="83969-113">Se almacena en el archivo definido por Super en la sección de mapas de bits del archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="83969-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="83969-114">Un súper archivo también puede almacenar las imágenes insertadas y deshabilitadas para otros botones, como silenciar, que no es necesario que sea un botón de tipo de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="83969-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="83969-115">Los archivos de superart no se usan en máscaras para Windows Media Player 10 Mobile o posterior porque las imágenes deshabilitadas para Seek trackbars se encuentran en el archivo seekthumb.</span><span class="sxs-lookup"><span data-stu-id="83969-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="83969-116">La siguiente imagen es un súper archivo típico.</span><span class="sxs-lookup"><span data-stu-id="83969-116">The following image is a typical Super file.</span></span>

![Super File](images/cesdksup.png)

<span data-ttu-id="83969-118">Esto almacena las imágenes deshabilitadas para los trackbars y el botón silenciar.</span><span class="sxs-lookup"><span data-stu-id="83969-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="83969-119">Estas imágenes se desplazan tal y como se define en la sección de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="83969-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="83969-120">El área de fondo de la imagen de TrackBar deshabilitada coincide exactamente con el área correspondiente en el archivo de fondo.</span><span class="sxs-lookup"><span data-stu-id="83969-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="83969-121">Esto es importante, porque el rectángulo completo definido para la imagen de TrackBar deshabilitada reemplazará el área de coincidencia en el archivo de fondo.</span><span class="sxs-lookup"><span data-stu-id="83969-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="83969-122">Esto garantiza que la imagen de TrackBar deshabilitada se mezcle sin problemas en la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="83969-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83969-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83969-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83969-124">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="83969-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




