---
description: Intervalo de imagen
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Intervalo de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568110"
---
# <a name="image-stride"></a><span data-ttu-id="fef35-103">Intervalo de imagen</span><span class="sxs-lookup"><span data-stu-id="fef35-103">Image Stride</span></span>

<span data-ttu-id="fef35-104">Cuando una imagen de vídeo se almacena en memoria, el búfer de memoria podría contener bytes de relleno adicionales después de cada fila de píxeles.</span><span class="sxs-lookup"><span data-stu-id="fef35-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="fef35-105">Los bytes de relleno afectan a cómo se almacena la imagen en memoria, pero no afectan al modo en que se muestra la imagen.</span><span class="sxs-lookup"><span data-stu-id="fef35-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="fef35-106">*STRIDE* es el número de bytes de una fila de píxeles en memoria hasta la siguiente fila de píxeles de la memoria.</span><span class="sxs-lookup"><span data-stu-id="fef35-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="fef35-107">STRIDE también se denomina *paso*.</span><span class="sxs-lookup"><span data-stu-id="fef35-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="fef35-108">Si los bytes de relleno están presentes, el intervalo es más ancho que el ancho de la imagen, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="fef35-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![diagrama que muestra una imagen más el relleno.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="fef35-110">Dos búferes que contienen fotogramas de vídeo con dimensiones iguales pueden tener dos progresos diferentes.</span><span class="sxs-lookup"><span data-stu-id="fef35-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="fef35-111">Si procesa una imagen de vídeo, debe tener en cuenta el intervalo.</span><span class="sxs-lookup"><span data-stu-id="fef35-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="fef35-112">Además, hay dos formas de organizar una imagen en memoria.</span><span class="sxs-lookup"><span data-stu-id="fef35-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="fef35-113">En una imagen de *arriba abajo* , la fila superior de píxeles de la imagen aparece en primer lugar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="fef35-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="fef35-114">En una imagen de *abajo arriba* , la última fila de píxeles aparece en primer lugar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="fef35-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="fef35-115">En la ilustración siguiente se muestra la diferencia entre una imagen de arriba abajo y una imagen de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="fef35-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![diagrama que muestra imágenes de arriba abajo e inferior.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="fef35-117">Una imagen de orden ascendente tiene un intervalo negativo, porque STRIDE se define como el número de bytes necesario para bajar una fila de píxeles, con respecto a la imagen mostrada.</span><span class="sxs-lookup"><span data-stu-id="fef35-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="fef35-118">Las imágenes YUV siempre deben ser de arriba abajo y cualquier imagen que esté contenida en una superficie de Direct3D debe ser de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="fef35-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="fef35-119">Las imágenes RGB en la memoria del sistema suelen estar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="fef35-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="fef35-120">En particular, las transformaciones de vídeo necesitan controlar los búferes con los progresos no coincidentes, ya que el búfer de entrada podría no coincidir con el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fef35-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="fef35-121">Por ejemplo, supongamos que desea convertir una imagen de origen y escribir el resultado en una imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="fef35-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="fef35-122">Suponga que ambas imágenes tienen el mismo ancho y alto, pero puede que no tengan el mismo formato de píxel o el mismo intervalo de imagen.</span><span class="sxs-lookup"><span data-stu-id="fef35-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="fef35-123">En el ejemplo de código siguiente se muestra un enfoque generalizado para escribir este tipo de función.</span><span class="sxs-lookup"><span data-stu-id="fef35-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="fef35-124">No se trata de un ejemplo de trabajo completo, porque abstrae muchos de los detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="fef35-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



<span data-ttu-id="fef35-125">Esta función toma seis parámetros:</span><span class="sxs-lookup"><span data-stu-id="fef35-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="fef35-126">Un puntero al inicio de la línea de recorrido 0 en la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="fef35-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="fef35-127">El paso de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="fef35-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="fef35-128">Un puntero al inicio de la línea de recorrido 0 en la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="fef35-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="fef35-129">El paso de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="fef35-129">The stride of the source image.</span></span>
-   <span data-ttu-id="fef35-130">Ancho de la imagen en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fef35-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="fef35-131">Alto de la imagen en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fef35-131">The height of the image in pixels.</span></span>

<span data-ttu-id="fef35-132">La idea general es procesar una fila cada vez, iterando por cada píxel de la fila.</span><span class="sxs-lookup"><span data-stu-id="fef35-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="fef35-133">Supongamos que el tipo \_ \_ de píxel de origen y el \_ tipo de píxel de destino \_ son estructuras que representan el diseño de píxeles para las imágenes de origen y de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fef35-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="fef35-134">(Por ejemplo, RGB de 32 bits usa la estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) .</span><span class="sxs-lookup"><span data-stu-id="fef35-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="fef35-135">No todos los formatos de píxel tienen una estructura predefinida). Convertir el puntero de matriz al tipo de estructura le permite tener acceso a los componentes RGB o YUV de cada píxel.</span><span class="sxs-lookup"><span data-stu-id="fef35-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="fef35-136">Al principio de cada fila, la función almacena un puntero a la fila.</span><span class="sxs-lookup"><span data-stu-id="fef35-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="fef35-137">Al final de la fila, incrementa el puntero en el ancho del intervalo de la imagen, lo que hace avanzar el puntero a la fila siguiente.</span><span class="sxs-lookup"><span data-stu-id="fef35-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="fef35-138">En este ejemplo se llama a una función hipotética denominada TransformPixelValue para cada píxel.</span><span class="sxs-lookup"><span data-stu-id="fef35-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="fef35-139">Puede ser cualquier función que calcule un píxel de destino de un píxel de origen.</span><span class="sxs-lookup"><span data-stu-id="fef35-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="fef35-140">Por supuesto, los detalles exactos dependerán de la tarea determinada.</span><span class="sxs-lookup"><span data-stu-id="fef35-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="fef35-141">Por ejemplo, si tiene un formato YUV plano, debe tener acceso a los planos de croma independientemente del plano de luminancia; con vídeo entrelazado, es posible que tenga que procesar los campos por separado. etc.</span><span class="sxs-lookup"><span data-stu-id="fef35-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="fef35-142">Para dar un ejemplo más concreto, el código siguiente convierte una imagen RGB de 32 bits en una imagen AYUV.</span><span class="sxs-lookup"><span data-stu-id="fef35-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="fef35-143">Se tiene acceso a los píxeles RGB mediante una estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) y se tiene acceso a los píxeles de AYUV mediante una estructura de estructura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .</span><span class="sxs-lookup"><span data-stu-id="fef35-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



<span data-ttu-id="fef35-144">En el ejemplo siguiente se convierte una imagen RGB de 32 bits en una imagen YV12.</span><span class="sxs-lookup"><span data-stu-id="fef35-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="fef35-145">En este ejemplo se muestra cómo controlar un formato YUV plano.</span><span class="sxs-lookup"><span data-stu-id="fef35-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="fef35-146">(YV12 es un formato plano 4:2:0). En este ejemplo, la función mantiene tres punteros independientes para los tres planos de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="fef35-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="fef35-147">Sin embargo, el enfoque básico es el mismo que el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="fef35-147">However, the basic approach is the same as the previous example.</span></span>


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



<span data-ttu-id="fef35-148">En todos estos ejemplos, se supone que la aplicación ya ha determinado el intervalo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="fef35-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="fef35-149">A veces, puede obtener esta información del búfer de medios.</span><span class="sxs-lookup"><span data-stu-id="fef35-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="fef35-150">De lo contrario, debe calcularlo en función del formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fef35-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="fef35-151">Para obtener más información sobre cómo calcular el intervalo de imagen y trabajar con búferes multimedia para vídeo, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="fef35-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fef35-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fef35-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fef35-153">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="fef35-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="fef35-154">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="fef35-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
