---
description: Formatos de archivo de imagen compatibles con las funciones D3DXCreatexxx y D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Enumeración D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821370"
---
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="658d8-103">\_ \_ Enumeración de formato de archivo de imagen D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="658d8-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="658d8-104">Formatos de archivo de imagen compatibles con las funciones D3DXCreatexxx y D3DX10Savexxx.</span><span class="sxs-lookup"><span data-stu-id="658d8-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="658d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="658d8-105">Syntax</span></span>


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="658d8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="658d8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="658d8-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF, \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="658d8-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-108">Formato de archivo de mapa de bits de Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="658d8-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="658d8-109">Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="658d8-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="658d8-110">La extensión de archivo para este formato es. bmp.</span><span class="sxs-lookup"><span data-stu-id="658d8-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="658d8-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-112">Formato de archivo comprimido JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="658d8-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="658d8-113">Especifica la compresión variable del color RGB de 24 bits y los archivos de documento de imagen de Tagged Image File Format de escala gris (TIFF) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="658d8-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="658d8-114">La extensión de archivo para este formato es. jpg.</span><span class="sxs-lookup"><span data-stu-id="658d8-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**\_PNG D3DX10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="658d8-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-116">Formato de archivo PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="658d8-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="658d8-117">Formato de mapa de bits no propietario mediante compresión sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="658d8-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="658d8-118">La extensión de archivo para este formato es. png.</span><span class="sxs-lookup"><span data-stu-id="658d8-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF ( \_ DDS)**</span><span class="sxs-lookup"><span data-stu-id="658d8-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-120">Formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="658d8-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="658d8-121">Almacena texturas, texturas de volumen y mapas de entorno cúbicos, con o sin niveles de mipmap y con o sin compresión de píxeles.</span><span class="sxs-lookup"><span data-stu-id="658d8-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="658d8-122">La extensión de archivo para este formato es. DDS.</span><span class="sxs-lookup"><span data-stu-id="658d8-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**\_TIFF IFF \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="658d8-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-124">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="658d8-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="658d8-125">Las extensiones de archivo para este formato son. tif y. tiff.</span><span class="sxs-lookup"><span data-stu-id="658d8-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**\_GIF IFF \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="658d8-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-127">Formato de intercambio de gráficos (GIF). La extensión de archivo para este formato es. gif.</span><span class="sxs-lookup"><span data-stu-id="658d8-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ el \_ WMP IFF**</span><span class="sxs-lookup"><span data-stu-id="658d8-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-129">Formato de Windows Media Photo (WMP).</span><span class="sxs-lookup"><span data-stu-id="658d8-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="658d8-130">Este formato también se conoce como HD Photo y JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="658d8-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="658d8-131">Las extensiones de archivo para este formato son. HDP,. jxr y. WDP.</span><span class="sxs-lookup"><span data-stu-id="658d8-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="658d8-132">Para que funcione correctamente, D3DX10, a la vez, **\_ \_ WMP** le requiere que inicialice com.</span><span class="sxs-lookup"><span data-stu-id="658d8-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="658d8-133">Por lo tanto, llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) en la aplicación antes de llamar a D3DX.</span><span class="sxs-lookup"><span data-stu-id="658d8-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="658d8-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="658d8-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="658d8-135">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="658d8-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="658d8-136">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="658d8-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="658d8-137">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="658d8-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="658d8-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="658d8-138">Remarks</span></span>

<span data-ttu-id="658d8-139">Vea [tipos de mapas de bits (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="658d8-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="658d8-140">D3DX10 usa el componente de creación de imágenes de Windows para implementar la mayoría de los tipos de archivo de mapa de bits admitidos.</span><span class="sxs-lookup"><span data-stu-id="658d8-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="658d8-141">Vea información [General sobre los componentes de Windows Imaging](https://msdn.microsoft.com/library/ms737408.aspx) para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="658d8-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="658d8-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="658d8-142">Requirements</span></span>



| <span data-ttu-id="658d8-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="658d8-143">Requirement</span></span> | <span data-ttu-id="658d8-144">Value</span><span class="sxs-lookup"><span data-stu-id="658d8-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="658d8-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="658d8-145">Header</span></span><br/> | <dl> <span data-ttu-id="658d8-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="658d8-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658d8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="658d8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658d8-148">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="658d8-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
