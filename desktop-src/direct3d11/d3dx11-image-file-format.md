---
title: Enumeración D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Formatos de archivo de imagen compatibles con las funciones D3DX11Createxxx y D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Enumeración de D3DX11_IMAGE_FILE_FORMAT Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987217"
---
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="5273a-106">\_ \_ Enumeración de formato de archivo de imagen D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="5273a-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="5273a-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5273a-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="5273a-108">Formatos de archivo de imagen compatibles con las funciones D3DX11Createxxx y D3DX11Savexxx.</span><span class="sxs-lookup"><span data-stu-id="5273a-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5273a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5273a-109">Syntax</span></span>


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="5273a-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="5273a-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5273a-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF, \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="5273a-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-112">Formato de archivo de mapa de bits de Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="5273a-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="5273a-113">Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="5273a-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="5273a-114">La extensión de archivo para este formato es. bmp.</span><span class="sxs-lookup"><span data-stu-id="5273a-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="5273a-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-116">Formato de archivo comprimido JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="5273a-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="5273a-117">Especifica la compresión variable del color RGB de 24 bits y los archivos de documento de imagen de Tagged Image File Format de escala gris (TIFF) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="5273a-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="5273a-118">La extensión de archivo para este formato es. jpg.</span><span class="sxs-lookup"><span data-stu-id="5273a-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**\_PNG D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="5273a-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-120">Formato de archivo PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="5273a-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="5273a-121">Formato de mapa de bits no propietario mediante compresión sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="5273a-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="5273a-122">La extensión de archivo para este formato es. png.</span><span class="sxs-lookup"><span data-stu-id="5273a-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF ( \_ DDS)**</span><span class="sxs-lookup"><span data-stu-id="5273a-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-124">Formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="5273a-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="5273a-125">Almacena texturas, texturas de volumen y mapas de entorno cúbicos, con o sin niveles de mipmap y con o sin compresión de píxeles.</span><span class="sxs-lookup"><span data-stu-id="5273a-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="5273a-126">La extensión de archivo para este formato es. DDS.</span><span class="sxs-lookup"><span data-stu-id="5273a-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF IFF \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="5273a-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-128">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="5273a-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="5273a-129">Las extensiones de archivo para este formato son. tif y. tiff.</span><span class="sxs-lookup"><span data-stu-id="5273a-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_GIF IFF \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="5273a-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-131">Formato de intercambio de gráficos (GIF).</span><span class="sxs-lookup"><span data-stu-id="5273a-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="5273a-132">La extensión de archivo para este formato es. gif.</span><span class="sxs-lookup"><span data-stu-id="5273a-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ el \_ WMP IFF**</span><span class="sxs-lookup"><span data-stu-id="5273a-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-134">Formato de Windows Media Photo (WMP).</span><span class="sxs-lookup"><span data-stu-id="5273a-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="5273a-135">Este formato también se conoce como HD Photo y JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="5273a-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="5273a-136">Las extensiones de archivo para este formato son. HDP,. jxr y. WDP.</span><span class="sxs-lookup"><span data-stu-id="5273a-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="5273a-137">Para que funcione correctamente, D3DX11, a la vez, **\_ \_ WMP** le requiere que inicialice com.</span><span class="sxs-lookup"><span data-stu-id="5273a-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="5273a-138">Por lo tanto, llame a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) en la aplicación antes de llamar a D3DX.</span><span class="sxs-lookup"><span data-stu-id="5273a-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="5273a-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5273a-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5273a-140">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="5273a-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5273a-141">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5273a-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5273a-142">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5273a-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5273a-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5273a-143">Remarks</span></span>

<span data-ttu-id="5273a-144">Vea [tipos de mapas de bits (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="5273a-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="5273a-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5273a-145">Requirements</span></span>



| <span data-ttu-id="5273a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5273a-146">Requirement</span></span> | <span data-ttu-id="5273a-147">Value</span><span class="sxs-lookup"><span data-stu-id="5273a-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5273a-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5273a-148">Header</span></span><br/> | <dl> <span data-ttu-id="5273a-149"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5273a-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5273a-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="5273a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5273a-151">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="5273a-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

