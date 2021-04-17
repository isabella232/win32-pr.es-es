---
title: Estructura de _BITMAPINFOHEADER
description: La \_ estructura BITMAPINFOHEADER define el formato de un fotograma de vídeo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Estructura _BITMAPINFOHEADER Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700181"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="06922-104">\_Estructura BITMAPINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="06922-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="06922-105">La estructura **\_ BITMAPINFOHEADER** define el formato de un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="06922-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="06922-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06922-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="06922-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="06922-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="06922-108">**bisize**</span><span class="sxs-lookup"><span data-stu-id="06922-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="06922-109">Especifica el número de bytes requerido por la estructura.</span><span class="sxs-lookup"><span data-stu-id="06922-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="06922-110">**biwidth**</span><span class="sxs-lookup"><span data-stu-id="06922-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="06922-111">Especifica el ancho del mapa de bits, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="06922-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="06922-112">**bialtura**</span><span class="sxs-lookup"><span data-stu-id="06922-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="06922-113">Especifica el alto del mapa de bits, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="06922-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="06922-114">Si **biheight** es positivo, el mapa de bits es un DIB de nivel inferior y su origen es la esquina inferior izquierda.</span><span class="sxs-lookup"><span data-stu-id="06922-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="06922-115">Si el valor de **biheight** es negativo, el mapa de bits es un DIB de arriba abajo y su origen es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="06922-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="06922-116">Si el valor de **biheight** es negativo, lo que indica un DIB de arriba abajo, la **bicompresión** debe ser de BI RGB o de campos de bits de \_ BI \_ .</span><span class="sxs-lookup"><span data-stu-id="06922-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="06922-117">Los DIB de arriba abajo no se pueden comprimir.</span><span class="sxs-lookup"><span data-stu-id="06922-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="06922-118">**biplanas**</span><span class="sxs-lookup"><span data-stu-id="06922-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="06922-119">Especifica el número de planos para el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="06922-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="06922-120">Este valor debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="06922-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="06922-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="06922-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="06922-122">Especifica el número de bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="06922-123">El miembro **biBitCount** de la estructura **BITMAPINFOHEADER** determina el número de bits que definen cada píxel y el número máximo de colores del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="06922-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="06922-124">Este miembro debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06922-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="06922-125">Value</span><span class="sxs-lookup"><span data-stu-id="06922-125">Value</span></span> | <span data-ttu-id="06922-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="06922-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06922-127">1</span><span class="sxs-lookup"><span data-stu-id="06922-127">1</span></span>     | <span data-ttu-id="06922-128">El mapa de bits es monocromo y el miembro bmiColors contiene dos entradas.</span><span class="sxs-lookup"><span data-stu-id="06922-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="06922-129">Cada bit de la matriz de mapas de bits representa un píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="06922-130">Si el bit está claro, se muestra el píxel con el color de la primera entrada de la tabla bmiColors. Si se establece el bit, el píxel tiene el color de la segunda entrada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="06922-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="06922-131">2</span><span class="sxs-lookup"><span data-stu-id="06922-131">2</span></span>     | <span data-ttu-id="06922-132">El mapa de bits tiene cuatro valores de color posibles.</span><span class="sxs-lookup"><span data-stu-id="06922-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="06922-133">4</span><span class="sxs-lookup"><span data-stu-id="06922-133">4</span></span>     | <span data-ttu-id="06922-134">El mapa de bits tiene un máximo de 16 colores y el miembro bmiColors contiene hasta 16 entradas.</span><span class="sxs-lookup"><span data-stu-id="06922-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="06922-135">Cada píxel del mapa de bits se representa mediante un índice de 4 bits en la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="06922-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="06922-136">Por ejemplo, si el primer byte del mapa de bits es 0x1F, el byte representa dos píxeles.</span><span class="sxs-lookup"><span data-stu-id="06922-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="06922-137">El primer píxel contiene el color de la segunda entrada de la tabla y el segundo píxel contiene el color de la entrada de la tabla decimosexto.</span><span class="sxs-lookup"><span data-stu-id="06922-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="06922-138">8</span><span class="sxs-lookup"><span data-stu-id="06922-138">8</span></span>     | <span data-ttu-id="06922-139">El mapa de bits tiene un máximo de 256 colores y el miembro bmiColors contiene hasta 256 entradas.</span><span class="sxs-lookup"><span data-stu-id="06922-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="06922-140">En este caso, cada byte de la matriz representa un único píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="06922-141">16</span><span class="sxs-lookup"><span data-stu-id="06922-141">16</span></span>    | <span data-ttu-id="06922-142">El mapa de bits tiene un máximo de 2 ^ 16 colores.</span><span class="sxs-lookup"><span data-stu-id="06922-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="06922-143">Si el miembro de bicompresión del BITMAPINFOHEADER es BI \_ RGB, el miembro bmiColors es **null**.</span><span class="sxs-lookup"><span data-stu-id="06922-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="06922-144">Cada palabra de la matriz de mapas de bits representa un solo píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="06922-145">Las intensidades relativas de rojo, verde y azul se representan con 5 bits para cada componente de color.</span><span class="sxs-lookup"><span data-stu-id="06922-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="06922-146">El valor de Blue está en los 5 bits menos significativos, seguido de 5 bits para cada verde y rojo.</span><span class="sxs-lookup"><span data-stu-id="06922-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="06922-147">No se usa el bit más significativo.</span><span class="sxs-lookup"><span data-stu-id="06922-147">The most significant bit is not used.</span></span> <span data-ttu-id="06922-148">La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="06922-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="06922-149">24</span><span class="sxs-lookup"><span data-stu-id="06922-149">24</span></span>    | <span data-ttu-id="06922-150">El mapa de bits tiene un máximo de 2 ^ 24 colores y el miembro bmiColors es **null**.</span><span class="sxs-lookup"><span data-stu-id="06922-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="06922-151">Cada tríptico de 3 bytes de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="06922-152">La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="06922-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="06922-153">32</span><span class="sxs-lookup"><span data-stu-id="06922-153">32</span></span>    | <span data-ttu-id="06922-154">El mapa de bits tiene un máximo de 2 ^ 32 colores.</span><span class="sxs-lookup"><span data-stu-id="06922-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="06922-155">Si el miembro de bicompression es BI \_ RGB, el miembro bmiColors es **null**.</span><span class="sxs-lookup"><span data-stu-id="06922-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="06922-156">Cada DWORD de la matriz de mapas de bits representa las intensidades relativas de azul, verde y rojo, respectivamente, para un píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="06922-157">No se utiliza el byte alto en cada DWORD.</span><span class="sxs-lookup"><span data-stu-id="06922-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="06922-158">La tabla de colores bmiColors se usa para optimizar los colores utilizados en los dispositivos basados en paletas y debe contener el número de entradas especificadas por el miembro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="06922-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="06922-159">**bicompresión**</span><span class="sxs-lookup"><span data-stu-id="06922-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="06922-160">Especifica el tipo de compresión de un mapa de bits comprimido de arriba abajo (no se pueden comprimir los DIB de arriba abajo).</span><span class="sxs-lookup"><span data-stu-id="06922-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="06922-161">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06922-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="06922-162">Value</span><span class="sxs-lookup"><span data-stu-id="06922-162">Value</span></span>         | <span data-ttu-id="06922-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="06922-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06922-164">\_RGB BI</span><span class="sxs-lookup"><span data-stu-id="06922-164">BI\_RGB</span></span>       | <span data-ttu-id="06922-165">Formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="06922-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="06922-166">\_campos de campos BI</span><span class="sxs-lookup"><span data-stu-id="06922-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="06922-167">Especifica que el mapa de bits no se comprime y que la tabla de colores consta de tres máscaras de color DWORD que especifican los componentes rojo, verde y azul, respectivamente, de cada píxel.</span><span class="sxs-lookup"><span data-stu-id="06922-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="06922-168">Esto es válido cuando se usa con mapas de bits de 16 BPP y 32-bpp.</span><span class="sxs-lookup"><span data-stu-id="06922-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="06922-169">Este valor es válido en Microsoft Windows CE versión 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="06922-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="06922-170">**biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="06922-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="06922-171">Especifica el tamaño de la imagen, en bytes.</span><span class="sxs-lookup"><span data-stu-id="06922-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="06922-172">Se puede establecer en cero para los mapas de bits de BI \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="06922-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="06922-173">**biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="06922-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="06922-174">Especifica la resolución horizontal, en píxeles por medidor, del dispositivo de destino para el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="06922-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="06922-175">Una aplicación puede usar este valor para seleccionar un mapa de bits de un grupo de recursos que coincida mejor con las características del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="06922-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="06922-176">**biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="06922-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="06922-177">Especifica la resolución vertical, en píxeles por medidor, del dispositivo de destino para el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="06922-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="06922-178">**biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="06922-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="06922-179">Especifica el número de índices de color de la tabla de colores que el mapa de bits usa realmente.</span><span class="sxs-lookup"><span data-stu-id="06922-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="06922-180">Si este valor es cero, el mapa de bits utiliza el número máximo de colores correspondientes al valor del miembro **biBitCount** para el modo de compresión especificado por **bicompression**.</span><span class="sxs-lookup"><span data-stu-id="06922-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="06922-181">**biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="06922-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="06922-182">Especifica el número de índices de color necesarios para mostrar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="06922-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="06922-183">Si este valor es cero, se requieren todos los colores.</span><span class="sxs-lookup"><span data-stu-id="06922-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="06922-184">Si biClrUsed es distinto de cero y el miembro biBitCount es menor que 16, el miembro biClrUsed especifica el número real de colores a los que accede el motor de gráficos o el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06922-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="06922-185">Si biBitCount es 16 o superior, el miembro biClrUsed especifica el tamaño de la tabla de colores que se usa para optimizar el rendimiento de las paletas de colores del sistema.</span><span class="sxs-lookup"><span data-stu-id="06922-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="06922-186">Si biBitCount es igual a 16 ó 32, la paleta de colores óptima se inicia inmediatamente después de las tres máscaras DWORD.</span><span class="sxs-lookup"><span data-stu-id="06922-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="06922-187">Si el mapa de bits es un mapa de bits empaquetado (un mapa de bits en el que la matriz de mapas de bits sigue inmediatamente a la \_ estructura BITMAPINFOHEADER y se hace referencia a él mediante un solo puntero), el miembro biClrUsed debe ser cero o el tamaño real de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="06922-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06922-188">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06922-188">Remarks</span></span>

<span data-ttu-id="06922-189">Esta estructura está contenida en una estructura **\_ VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="06922-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="06922-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06922-190">Requirements</span></span>



| <span data-ttu-id="06922-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="06922-191">Requirement</span></span> | <span data-ttu-id="06922-192">Value</span><span class="sxs-lookup"><span data-stu-id="06922-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06922-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06922-193">Header</span></span><br/> | <dl> <span data-ttu-id="06922-194"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06922-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06922-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="06922-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06922-196">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="06922-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="06922-197">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="06922-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





