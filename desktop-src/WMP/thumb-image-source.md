---
title: Origen de la imagen de Thumb
description: Origen de la imagen de Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, origen de imagen
- trackbars en máscaras, origen de la imagen de Thumb
- origen de imagen para máscaras, trackbars
- Thumb, origen de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075384"
---
# <a name="thumb-image-source"></a><span data-ttu-id="0cc91-110">Origen de la imagen de Thumb</span><span class="sxs-lookup"><span data-stu-id="0cc91-110">Thumb Image Source</span></span>

<span data-ttu-id="0cc91-111">Debe definir el nombre del archivo que contiene la imagen de Thumb.</span><span class="sxs-lookup"><span data-stu-id="0cc91-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="0cc91-112">Debe ser un nombre de archivo válido con la extensión. bmp,. gif,. jpg o. png.</span><span class="sxs-lookup"><span data-stu-id="0cc91-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="0cc91-113">El archivo debe contener tres imágenes en paralelo de tamaño idéntico.</span><span class="sxs-lookup"><span data-stu-id="0cc91-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="0cc91-114">Deben ser adyacentes entre sí sin espacio.</span><span class="sxs-lookup"><span data-stu-id="0cc91-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="0cc91-115">La posición superior izquierda de la imagen izquierda debe estar en la esquina superior izquierda del archivo.</span><span class="sxs-lookup"><span data-stu-id="0cc91-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="0cc91-116">La imagen del lado izquierdo es la imagen normal de la imagen Thumb y la imagen en el centro representa el estado pushd y la imagen de la derecha describe el Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0cc91-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="0cc91-117">Puede que desee que determinadas áreas de la imagen de Thumb sean transparentes.</span><span class="sxs-lookup"><span data-stu-id="0cc91-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="0cc91-118">Esto le permitirá crear imágenes Thumb en formas que no sean rectangulares.</span><span class="sxs-lookup"><span data-stu-id="0cc91-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="0cc91-119">Cualquier región de la imagen de Thumb que rellene con el color especificado por el valor RGB 255, 0 y 255 aparecerá transparente en la máscara.</span><span class="sxs-lookup"><span data-stu-id="0cc91-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cc91-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cc91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc91-121">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="0cc91-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




