---
description: Define los términos que se usan en WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glosario de componentes de Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697346"
---
# <a name="windows-imaging-component-glossary"></a><span data-ttu-id="72c51-103">Glosario de componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="72c51-103">Windows Imaging Component Glossary</span></span>

## <a name="b"></a><span data-ttu-id="72c51-104">B</span><span class="sxs-lookup"><span data-stu-id="72c51-104">B</span></span>

<dl> <dt>

<span data-ttu-id="72c51-105">**profundidad de bits**</span><span class="sxs-lookup"><span data-stu-id="72c51-105">**bit depth**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-106">Número de valores de color que se pueden asignar a un solo píxel en una imagen.</span><span class="sxs-lookup"><span data-stu-id="72c51-106">The number of color values that can be assigned to a single pixel in an image.</span></span> <span data-ttu-id="72c51-107">La profundidad de color puede oscilar entre 1 bit (blanco y negro) y 32 bits (más de 16,7 millones de colores).</span><span class="sxs-lookup"><span data-stu-id="72c51-107">Color depth can range from 1 bit (black and white) to 32 bits (over 16.7 million colors).</span></span> <span data-ttu-id="72c51-108">Vea también: profundidad de color</span><span class="sxs-lookup"><span data-stu-id="72c51-108">See also: Color Depth</span></span>

</dd> <dt>

<span data-ttu-id="72c51-109">**bits por píxel (BPP)**</span><span class="sxs-lookup"><span data-stu-id="72c51-109">**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-110">Número de bits que representan el valor de color de cada píxel de una imagen digitalizada.</span><span class="sxs-lookup"><span data-stu-id="72c51-110">The number of bits that represent the color value of each pixel in a digitized image.</span></span> <span data-ttu-id="72c51-111">Vea también: BPP</span><span class="sxs-lookup"><span data-stu-id="72c51-111">See also:BPP</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="72c51-112">C</span><span class="sxs-lookup"><span data-stu-id="72c51-112">C</span></span>

<dl> <dt>

<span data-ttu-id="72c51-113">**Clipper**</span><span class="sxs-lookup"><span data-stu-id="72c51-113">**clipper**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-114">Objeto IWICBitmapClipper.</span><span class="sxs-lookup"><span data-stu-id="72c51-114">An IWICBitmapClipper object.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-115">**Codec**</span><span class="sxs-lookup"><span data-stu-id="72c51-115">**codec**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-116">Un filtro que comprime (codifica) o descomprime (descodifica) un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="72c51-116">A filter that compresses (encodes) or decompresses (decodes) a data stream.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-117">**contexto de color**</span><span class="sxs-lookup"><span data-stu-id="72c51-117">**color context**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-118">Abstracción de un perfil de color.</span><span class="sxs-lookup"><span data-stu-id="72c51-118">An abstraction for a color profile.</span></span> <span data-ttu-id="72c51-119">El perfil se puede cargar desde un archivo (es decir, "sRGB color Space Profile. ICM") o desde un búfer de memoria que se obtiene al leer.</span><span class="sxs-lookup"><span data-stu-id="72c51-119">The profile can be loaded from a file (ie. "sRGB Color Space Profile.icm") or from a memory buffer obtained by reading.</span></span> <span data-ttu-id="72c51-120">La información de contexto de color se define mediante la interfaz IWICColorContext para WIC y se recupera con el método GetColorContext.</span><span class="sxs-lookup"><span data-stu-id="72c51-120">Color context information is defined by the IWICColorContext interface for WIC, and is retrieved with the GetColorContext method.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-121">**transformación de color**</span><span class="sxs-lookup"><span data-stu-id="72c51-121">**color transform**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-122">Asignar colores del contexto de color de origen al contexto de color de destino en un formato de píxel de salida determinado.</span><span class="sxs-lookup"><span data-stu-id="72c51-122">Mapping colors from the source color context to the destination color context in a given output pixel format.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-123">**Modelo de color CYMK**</span><span class="sxs-lookup"><span data-stu-id="72c51-123">**CYMK color model**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-124">Espacio de colores multidimensional compuesto por las intensidades aguamarina, fucsia, amarillo y negro que constituyen un color determinado.</span><span class="sxs-lookup"><span data-stu-id="72c51-124">Multidimensional color space consisting of the cyan, magenta, yellow, and black intensities that make up a given color.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="72c51-125">D</span><span class="sxs-lookup"><span data-stu-id="72c51-125">D</span></span>

<dl> <dt>

<span data-ttu-id="72c51-126">**descodificador**</span><span class="sxs-lookup"><span data-stu-id="72c51-126">**decoder**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-127">Véase: códec</span><span class="sxs-lookup"><span data-stu-id="72c51-127">See Other Term: codec</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="72c51-128">E</span><span class="sxs-lookup"><span data-stu-id="72c51-128">E</span></span>

<dl> <dt>

<span data-ttu-id="72c51-129">**codificador**</span><span class="sxs-lookup"><span data-stu-id="72c51-129">**encoder**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-130">Véase: códec</span><span class="sxs-lookup"><span data-stu-id="72c51-130">See Other Term: codec</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="72c51-131">L</span><span class="sxs-lookup"><span data-stu-id="72c51-131">L</span></span>

<dl> <dt>

<span data-ttu-id="72c51-132">**alguna**</span><span class="sxs-lookup"><span data-stu-id="72c51-132">**lossless**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-133">Un tipo de compresión que garantiza que los datos originales se pueden recuperar exactamente, sin pérdida de calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="72c51-133">A type of compression that ensures that the original data can be recovered exactly, with no loss in image quality.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-134">**con pérdida**</span><span class="sxs-lookup"><span data-stu-id="72c51-134">**lossy**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-135">Se quita un proceso para comprimir los datos en los que la información no es necesaria y no se puede recuperar tras la descompresión.</span><span class="sxs-lookup"><span data-stu-id="72c51-135">A process for compressing data in which information deemed unnecessary is removed and cannot be recovered upon decompression.</span></span> <span data-ttu-id="72c51-136">Normalmente se utiliza con datos de audio y objetos visuales en los que es aceptable una ligera degradación de la calidad.</span><span class="sxs-lookup"><span data-stu-id="72c51-136">Typically used with audio and visual data in which a slight degradation of quality is acceptable.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="72c51-137">M</span><span class="sxs-lookup"><span data-stu-id="72c51-137">M</span></span>

<dl> <dt>

<span data-ttu-id="72c51-138">**contenedor multiproceso (MTA)**</span><span class="sxs-lookup"><span data-stu-id="72c51-138">**multithreaded apartment (MTA)**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-139">Forma de multithreading compatible con el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="72c51-139">A form of multithreading that is supported by Component Object Model (COM).</span></span> <span data-ttu-id="72c51-140">En un modelo de Apartamento multiproceso, todos los subprocesos del proceso que se han inicializado como subproceso libre se encuentran en un único apartamento.</span><span class="sxs-lookup"><span data-stu-id="72c51-140">In a multithreaded apartment model, all of the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="72c51-141">N</span><span class="sxs-lookup"><span data-stu-id="72c51-141">N</span></span>

<dl> <dt>

<span data-ttu-id="72c51-142">**formato de píxel nativo**</span><span class="sxs-lookup"><span data-stu-id="72c51-142">**native pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-143">Uno de los formatos de píxel que proporciona WIC, donde se describe el diseño de memoria de cada píxel de un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="72c51-143">One of the pixel formats provided by WIC, wherein the memory layout of each pixel in a bitmap is described.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="72c51-144">P</span><span class="sxs-lookup"><span data-stu-id="72c51-144">P</span></span>

<dl> <dt>

<span data-ttu-id="72c51-145">**índ**</span><span class="sxs-lookup"><span data-stu-id="72c51-145">**palette**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-146">Conjunto de colores utilizados por un objeto o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="72c51-146">Set of colors used by an object or application.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-147">**Directiva de metadatos de fotos**</span><span class="sxs-lookup"><span data-stu-id="72c51-147">**photo metadata policy**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-148">Directiva de Windows para leer, escribir y quitar metadatos de imagen.</span><span class="sxs-lookup"><span data-stu-id="72c51-148">The windows policy for reading, writing, and removing image metadata.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-149">**formato de píxeles**</span><span class="sxs-lookup"><span data-stu-id="72c51-149">**pixel format**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-150">Tamaño y organización de los componentes de color de píxeles en la memoria.</span><span class="sxs-lookup"><span data-stu-id="72c51-150">Size and arrangement of pixel color components in memory.</span></span> <span data-ttu-id="72c51-151">Se especifica mediante el número total de bits usados por píxel y el número de bits usados para almacenar los componentes rojo, verde, azul y alfa del color.</span><span class="sxs-lookup"><span data-stu-id="72c51-151">It is specified by the total number of bits used per pixel and the number of bits used to store the red, green, blue, and alpha components of the color.</span></span> <span data-ttu-id="72c51-152">Por ejemplo, el formato de píxel RGB24 usa 24 bits para almacenar un color de píxeles, con ocho bits cada uno para rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="72c51-152">For example, the RGB24 pixel format uses 24 bits to store a pixel color, with eight bits each for red, green, and blue.</span></span> <span data-ttu-id="72c51-153">El formato de píxel de ARGB32 usa 32 bits, con 24 bits de información de color y 8 bits de información de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="72c51-153">The ARGB32 pixel format uses 32 bits, with 24 bits of color information and 8 bits of alpha channel information.</span></span>

</dd> <dt>

<span data-ttu-id="72c51-154">**descodificación progresiva**</span><span class="sxs-lookup"><span data-stu-id="72c51-154">**progressive decoding**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-155">Proceso para descodificar imágenes que se han codificado con información sobre los distintos niveles de descodificación.</span><span class="sxs-lookup"><span data-stu-id="72c51-155">The process for decoding images that have been encoded with information about the different decoding levels.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="72c51-156">S</span><span class="sxs-lookup"><span data-stu-id="72c51-156">S</span></span>

<dl> <dt>

<span data-ttu-id="72c51-157">**misiones**</span><span class="sxs-lookup"><span data-stu-id="72c51-157">**stream**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-158">Hace referencia a una interfaz COM IStream que se puede utilizar para leer o escribir datos de forma secuencial en archivos, memoria o ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="72c51-158">Refers to an IStream COM interface which can be used to sequentially read or write data to files, memory, or network locations.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="72c51-159">T</span><span class="sxs-lookup"><span data-stu-id="72c51-159">T</span></span>

<dl> <dt>

<span data-ttu-id="72c51-160">**curva de tono**</span><span class="sxs-lookup"><span data-stu-id="72c51-160">**tone curve**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-161">Un gráfico que se usa en la fotografía digital y que muestra el rango tonal de la imagen.</span><span class="sxs-lookup"><span data-stu-id="72c51-161">A graph used in digital photography that displays the tonal range of the image.</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="72c51-162">W</span><span class="sxs-lookup"><span data-stu-id="72c51-162">W</span></span>

<dl> <dt>

<span data-ttu-id="72c51-163">**Windows Imaging Component (WIC)**</span><span class="sxs-lookup"><span data-stu-id="72c51-163">**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="72c51-164">Plataforma extensible que proporciona una API de bajo nivel para imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="72c51-164">An extensible platform that provides low-level API for digital images.</span></span>

</dd> </dl>

 

 



