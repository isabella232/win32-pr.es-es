---
description: Otros objetos de origen
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Otros objetos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806439"
---
# <a name="other-source-objects"></a><span data-ttu-id="012d5-103">Otros objetos de origen</span><span class="sxs-lookup"><span data-stu-id="012d5-103">Other Source Objects</span></span>

<span data-ttu-id="012d5-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="012d5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="012d5-105">Además de los orígenes de vídeo y audio, el [servicio de edición de DirectShow](directshow-editing-services.md) (des) admite los siguientes objetos de origen.</span><span class="sxs-lookup"><span data-stu-id="012d5-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="012d5-106">**Imágenes fijas**</span><span class="sxs-lookup"><span data-stu-id="012d5-106">**Still Images**</span></span>

<span data-ttu-id="012d5-107">DES admite los siguientes formatos de archivo para imágenes fijas:</span><span class="sxs-lookup"><span data-stu-id="012d5-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="012d5-108">Mapa de bits (.bmp)</span><span class="sxs-lookup"><span data-stu-id="012d5-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="012d5-109">GIF (formato de intercambio de gráficos)</span><span class="sxs-lookup"><span data-stu-id="012d5-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="012d5-110">JPEG (grupo de expertos fotográficos Unidos)</span><span class="sxs-lookup"><span data-stu-id="012d5-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="012d5-111">Adaptador de gráficos Targa o Truevision (. TGA): modo 2 (RGB sin comprimir) en formato de 16 bits, 24, bits o 32 bits.</span><span class="sxs-lookup"><span data-stu-id="012d5-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="012d5-112">Estos archivos se pueden usar como imágenes fijas o para crear animaciones.</span><span class="sxs-lookup"><span data-stu-id="012d5-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="012d5-113">En el caso de los archivos Bitmap, JPEG y Targa, si usa el archivo como imagen fija, llame al método [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para establecer la velocidad de fotogramas en cero.</span><span class="sxs-lookup"><span data-stu-id="012d5-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="012d5-114">**Secuencias DIB**</span><span class="sxs-lookup"><span data-stu-id="012d5-114">**DIB Sequences**</span></span>

<span data-ttu-id="012d5-115">Dado una serie de archivos de mapa de bits, JPEG o Targa, el motor de representación puede construir una secuencia DIB.</span><span class="sxs-lookup"><span data-stu-id="012d5-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="012d5-116">Para crear una secuencia DIB, asigne a los archivos nombres secuenciales numéricos, como Image001.bmp, Image002.bmp, Image003.bmp, etc.</span><span class="sxs-lookup"><span data-stu-id="012d5-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="012d5-117">Use el primer archivo de la secuencia como origen.</span><span class="sxs-lookup"><span data-stu-id="012d5-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="012d5-118">Establezca la velocidad de fotogramas para la secuencia mediante una llamada a [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span><span class="sxs-lookup"><span data-stu-id="012d5-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="012d5-119">El motor de representación recorre las imágenes de la secuencia a la velocidad de fotogramas especificada.</span><span class="sxs-lookup"><span data-stu-id="012d5-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="012d5-120">Si la secuencia es demasiado corta para rellenar la duración, dada la velocidad de fotogramas, el resto de la duración es el negro sólido.</span><span class="sxs-lookup"><span data-stu-id="012d5-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="012d5-121">No se produce ningún error durante la representación.</span><span class="sxs-lookup"><span data-stu-id="012d5-121">No error occurs during rendering.</span></span>

<span data-ttu-id="012d5-122">**Orígenes GIF**</span><span class="sxs-lookup"><span data-stu-id="012d5-122">**GIF Sources**</span></span>

<span data-ttu-id="012d5-123">DES admite orígenes GIF, incluidos los GIF animados y transparentes, mediante la especificación GIF89a.</span><span class="sxs-lookup"><span data-stu-id="012d5-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="012d5-124">Con un GIF animado, a diferencia de los demás tipos de archivo, no es necesario establecer la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="012d5-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="012d5-125">El archivo GIF especifica el retraso entre cada imagen de la animación.</span><span class="sxs-lookup"><span data-stu-id="012d5-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="012d5-126">Para admitir archivos GIF transparentes, DES convierte las regiones transparentes de la imagen en el triple Triple RGB (0,0).</span><span class="sxs-lookup"><span data-stu-id="012d5-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="012d5-127">Después, puede usar la [transición de clave](key-transition.md) a la clave en RGB (0,0).</span><span class="sxs-lookup"><span data-stu-id="012d5-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="012d5-128">DES también convierte las regiones negras que se encuentran dentro del intervalo RGB (0 – 7, 0 – 7, 0 – 7) al valor RGB (8, 8, 8), excepto para el índice de transparencia, si está en ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="012d5-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="012d5-129">Esta conversión no se detecta en el ojo.</span><span class="sxs-lookup"><span data-stu-id="012d5-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="012d5-130">**Origen de color de vídeo**</span><span class="sxs-lookup"><span data-stu-id="012d5-130">**Video Color Source**</span></span>

<span data-ttu-id="012d5-131">El objeto de [origen de color de vídeo](video-color-source.md) crea una imagen de vídeo continua de un color sólido.</span><span class="sxs-lookup"><span data-stu-id="012d5-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="012d5-132">Un uso para este objeto es convertirlo en una capa en una transición.</span><span class="sxs-lookup"><span data-stu-id="012d5-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="012d5-133">Por ejemplo, úselo en un fundido de vídeo o fundido de salida.</span><span class="sxs-lookup"><span data-stu-id="012d5-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="012d5-134">**Filtros de origen personalizados**</span><span class="sxs-lookup"><span data-stu-id="012d5-134">**Custom Source Filters**</span></span>

<span data-ttu-id="012d5-135">DES puede usar un filtro de origen de DirectShow como origen de la escala de tiempo, si el filtro cumple las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="012d5-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="012d5-136">Admite búsquedas</span><span class="sxs-lookup"><span data-stu-id="012d5-136">It supports seeking</span></span>
-   <span data-ttu-id="012d5-137">Genera un formato compatible con DES.</span><span class="sxs-lookup"><span data-stu-id="012d5-137">It produces a format that DES supports.</span></span> <span data-ttu-id="012d5-138">El formato se puede comprimir siempre que el sistema del usuario tenga un filtro DirectShow capaz de descodificarlo.</span><span class="sxs-lookup"><span data-stu-id="012d5-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="012d5-139">Para usar un origen personalizado, especifique el CLSID del filtro como el GUID del subobjeto del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="012d5-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="012d5-140">Para obtener más información, vea [subobjects](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="012d5-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="012d5-141">Para admitir propiedades personalizadas, impleméntelo como propiedades "put" de **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="012d5-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="012d5-142">Solo se admiten propiedades estáticas en objetos de origen; no se admiten las propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="012d5-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="012d5-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="012d5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="012d5-144">Trabajar con orígenes</span><span class="sxs-lookup"><span data-stu-id="012d5-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



