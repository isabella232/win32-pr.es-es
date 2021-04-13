---
description: Describe los formatos de archivo de imagen compatibles. Vea la sección Comentarios para obtener descripciones de estos formatos.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Enumeración D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362565"
---
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="c2e1d-104">\_Enumeración de D3DXIMAGE FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="c2e1d-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="c2e1d-105">Describe los formatos de archivo de imagen compatibles.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-105">Describes the supported image file formats.</span></span> <span data-ttu-id="c2e1d-106">Vea la sección Comentarios para obtener descripciones de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2e1d-107">Syntax</span></span>


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a><span data-ttu-id="c2e1d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c2e1d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c2e1d-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-110">Formato de archivo de mapa de bits de Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-112">Formato de archivo comprimido de JPEG (Joint Graphics Experts Group).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-114">Formato de archivo de imagen Truevision (Targa o TGA).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**\_PNG D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-116">Formato de archivo PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-118">Formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-120">Formato de archivo portable pixmap (PPM).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-122">Formato de archivo de mapa de bits independiente del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-124">Formato de archivo de intervalo dinámico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**\_PFM D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-126">Formato de archivo de asignación Float portátil.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="c2e1d-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2e1d-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c2e1d-128">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c2e1d-129">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c2e1d-130">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2e1d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2e1d-131">Remarks</span></span>

<span data-ttu-id="c2e1d-132">Las funciones que comienzan por D3DXLoadxxx admiten todos los formatos enumerados.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="c2e1d-133">Las funciones que comienzan por D3DXSavexxx admiten todos los formatos enumerados, excepto los formatos Truevision (. TGA) y pixmap (. ppm) portable.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="c2e1d-134">En la tabla siguiente se enumeran los formatos de entrada y salida disponibles.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="c2e1d-135">Extensión de archivo</span><span class="sxs-lookup"><span data-stu-id="c2e1d-135">File Extension</span></span> | <span data-ttu-id="c2e1d-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2e1d-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e1d-137">.bmp</span><span class="sxs-lookup"><span data-stu-id="c2e1d-137">.bmp</span></span>           | <span data-ttu-id="c2e1d-138">Formato de mapa de bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-138">Windows bitmap format.</span></span> <span data-ttu-id="c2e1d-139">Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="c2e1d-140">.dds</span><span class="sxs-lookup"><span data-stu-id="c2e1d-140">.dds</span></span>           | <span data-ttu-id="c2e1d-141">Formato de archivo de superficie de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="c2e1d-142">Almacena texturas, texturas de volumen y mapas de entorno cúbicos, con o sin niveles de mipmap y con o sin compresión de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="c2e1d-143">Consulte [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="c2e1d-144">.dib</span><span class="sxs-lookup"><span data-stu-id="c2e1d-144">.dib</span></span>           | <span data-ttu-id="c2e1d-145">DIB de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-145">Windows DIB.</span></span> <span data-ttu-id="c2e1d-146">Contiene una matriz de bits combinados con estructuras que especifican el ancho y el alto de la imagen de mapa de bits, el formato de color del dispositivo en el que se creó la imagen y la resolución del dispositivo que se usa para crear la imagen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="c2e1d-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="c2e1d-147">.hdr</span></span>           | <span data-ttu-id="c2e1d-148">Formato HDR.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-148">HDR format.</span></span> <span data-ttu-id="c2e1d-149">Codifica cada píxel como un color de RGBE de 32 bits, con 8 bits de mantisa para rojo, verde y azul, y un exponente de 8 bits compartido.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="c2e1d-150">Cada canal se comprime por separado con la codificación de longitud de ejecución (RLE).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="c2e1d-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="c2e1d-151">.jpg</span></span>           | <span data-ttu-id="c2e1d-152">Estándar JPEG.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-152">JPEG standard.</span></span> <span data-ttu-id="c2e1d-153">Especifica la compresión variable del color RGB de 24 bits y los archivos de documento de imagen de Tagged Image File Format de escala gris (TIFF) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="c2e1d-154">. PFM</span><span class="sxs-lookup"><span data-stu-id="c2e1d-154">.pfm</span></span>           | <span data-ttu-id="c2e1d-155">Formato de mapa Float portátil.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-155">Portable float map format.</span></span> <span data-ttu-id="c2e1d-156">Formato de imagen de punto flotante sin formato, sin compresión.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="c2e1d-157">El encabezado de archivo especifica el ancho de la imagen, el alto, monocromo o color, y el orden de las palabras del equipo.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="c2e1d-158">Los datos de píxeles se almacenan como valores de punto flotante de 32 bits, con 3 valores por píxel para el color y un valor por píxel para monocromo.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="c2e1d-159">.png</span><span class="sxs-lookup"><span data-stu-id="c2e1d-159">.png</span></span>           | <span data-ttu-id="c2e1d-160">Formato PNG.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-160">PNG format.</span></span> <span data-ttu-id="c2e1d-161">Formato de mapa de bits no propietario mediante compresión sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="c2e1d-162">. ppm</span><span class="sxs-lookup"><span data-stu-id="c2e1d-162">.ppm</span></span>           | <span data-ttu-id="c2e1d-163">Formato Pixmap portátil.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-163">Portable Pixmap format.</span></span> <span data-ttu-id="c2e1d-164">Formato de archivo binario o ASCII para imágenes de color que incluye el alto y el ancho de la imagen y el valor del componente de color máximo.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="c2e1d-165">.tga</span><span class="sxs-lookup"><span data-stu-id="c2e1d-165">.tga</span></span>           | <span data-ttu-id="c2e1d-166">Formato del adaptador de gráficos Targa o Truevision.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="c2e1d-167">Admite profundidades de 8, 15, 16, 24 y 32 bits, incluida la escala de grises de 8 bits, y contiene datos de paleta de colores opcionales, datos de origen y de tamaño de imagen (x, y) y datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="c2e1d-168">Vea [tipos de mapas de bits](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e1d-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e1d-169">Requirements</span></span>



| <span data-ttu-id="c2e1d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e1d-170">Requirement</span></span> | <span data-ttu-id="c2e1d-171">Value</span><span class="sxs-lookup"><span data-stu-id="c2e1d-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e1d-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2e1d-172">Header</span></span><br/> | <dl> <span data-ttu-id="c2e1d-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e1d-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e1d-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2e1d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e1d-175">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="c2e1d-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
