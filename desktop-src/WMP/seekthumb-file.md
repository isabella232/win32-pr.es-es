---
title: Archivo SeekThumb
description: Archivo SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos SeekThumbd
- Aspectos de Windows Media Player Mobile, archivos SeekThumb
- máscaras, archivos SeekThumb
- SeekThumb de archivos en máscaras
- Thumb, archivos SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994362"
---
# <a name="seekthumb-file"></a><span data-ttu-id="ca821-111">Archivo SeekThumb</span><span class="sxs-lookup"><span data-stu-id="ca821-111">SeekThumb File</span></span>

<span data-ttu-id="ca821-112">El archivo SeekThumb define la imagen que indica la ubicación de reproducción dentro del elemento multimedia para una barra de búsqueda de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ca821-112">The SeekThumb file defines the image that indicates the playback location within the media item for a Seek trackbar.</span></span> <span data-ttu-id="ca821-113">Puede usar un archivo y definirlo para su uso por SeekThumb y VolumeThumb.</span><span class="sxs-lookup"><span data-stu-id="ca821-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="ca821-114">A diferencia de los demás archivos de arte, los archivos de control de posición se definen en la sección Trackbars del archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="ca821-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="ca821-115">La siguiente imagen es un archivo SeekThumb típico.</span><span class="sxs-lookup"><span data-stu-id="ca821-115">The following image is a typical SeekThumb file.</span></span>

![archivo seekthumb](images/cesdksee.gif)

<span data-ttu-id="ca821-117">Estos dos archivos de botón tienen el mismo aspecto pero tienen tamaños ligeramente diferentes.</span><span class="sxs-lookup"><span data-stu-id="ca821-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="ca821-118">La imagen izquierda es la vista normal que ve el usuario y la imagen de la derecha es la imagen insertada que el usuario ve al puntear en el botón.</span><span class="sxs-lookup"><span data-stu-id="ca821-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

> [!Note]  
> <span data-ttu-id="ca821-119">Los archivos de SeekThumb Art creados para las máscaras usadas en Windows Media Player 10 Mobile o posterior deben tener las tres imágenes siguientes (de izquierda a derecha): normal, insertado y deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ca821-119">SeekThumb art files created for skins used in Windows Media Player 10 Mobile or later must have the following three images (from left to right): normal, pushed, and disabled.</span></span>

 

<span data-ttu-id="ca821-120">Puede que desee que determinadas áreas de las imágenes de Thumb sean transparentes.</span><span class="sxs-lookup"><span data-stu-id="ca821-120">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="ca821-121">Esto le permitirá crear imágenes Thumb en formas que no sean rectangulares.</span><span class="sxs-lookup"><span data-stu-id="ca821-121">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="ca821-122">Cualquier región de una imagen Thumb que rellene con el color especificado por el valor RGB 255, 0 y 255 aparecerá transparente en la máscara.</span><span class="sxs-lookup"><span data-stu-id="ca821-122">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca821-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca821-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca821-124">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="ca821-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




