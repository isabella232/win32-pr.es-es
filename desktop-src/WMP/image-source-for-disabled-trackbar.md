---
title: Origen de imagen para TrackBar deshabilitado
description: Origen de imagen para TrackBar deshabilitado
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, origen de imagen
- origen de imagen para máscaras, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695320"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="52755-108">Origen de imagen para TrackBar deshabilitado</span><span class="sxs-lookup"><span data-stu-id="52755-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="52755-109">Debe definir el origen de la imagen que desea mostrar cuando se deshabilita una barra de información mediante el tipo de mapa de bits del que desea dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="52755-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="52755-110">La imagen que se muestra normalmente estará dentro del superarchivo o si está creando una máscara para Windows Media Player 10 Mobile, la imagen estará dentro del archivo SeekThumb.</span><span class="sxs-lookup"><span data-stu-id="52755-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="52755-111">Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="52755-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="52755-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.</span><span class="sxs-lookup"><span data-stu-id="52755-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="52755-113">Por ejemplo, para usar una imagen del mapa de bits SeekThumb que tiene una posición superior e izquierda de 50, 60 píxeles, escriba:</span><span class="sxs-lookup"><span data-stu-id="52755-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="52755-114">Debe definir una ubicación de imagen para una imagen de TrackBar deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="52755-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="52755-115">Si no desea mostrar una nueva imagen, puede definir la imagen de fondo como la imagen deshabilitada con un desplazamiento de 0, 0:</span><span class="sxs-lookup"><span data-stu-id="52755-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="52755-116">En el ejemplo anterior, 50, 60 representa la ubicación del botón con el que está trabajando en el archivo SeekThumb (en este caso, la misma ubicación que el botón en el mapa de bits de fondo).</span><span class="sxs-lookup"><span data-stu-id="52755-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="52755-117">Sin embargo, se recomienda encarecidamente mostrar una imagen deshabilitada para todos los trackbars para que el usuario tenga una indicación visual, porque trackbars no se podrá usar en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="52755-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="52755-118">Por ejemplo, la búsqueda de trackbars puede estar deshabilitada si la lista de reproducción actual está vacía.</span><span class="sxs-lookup"><span data-stu-id="52755-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52755-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52755-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52755-120">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="52755-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




