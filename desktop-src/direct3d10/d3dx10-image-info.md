---
description: 'D3DX10_IMAGE_INFO estructura: devuelve una descripción del contenido original de un archivo de imagen.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105483"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="ab6e7-103">Estructura DE INFORMACIÓN DE IMAGEN de D3DX10 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab6e7-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="ab6e7-104">Devuelve una descripción del contenido original de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab6e7-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="ab6e7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab6e7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab6e7-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-109">Ancho de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-112">Alto de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-113">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-115">Profundidad de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-118">Tamaño de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-118">Size of the texture array.</span></span> <span data-ttu-id="ab6e7-119">*ArraySize* será 1 para una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-121">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-122">Número de niveles de mapa mip en la imagen original.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-124">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-125">Propiedades de recursos varios (vea [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="ab6e7-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-126">**Format**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-127">Tipo: **[ **DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-128">Valor del tipo [**enumerado DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que describe más de cerca los datos de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-130">Tipo: **[ **DIMENSIÓN DE \_ RECURSOS \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-131">Representa el tipo de la textura almacenada en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="ab6e7-132">Consulte [**DIMENSIÓN DE RECURSOS D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="ab6e7-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="ab6e7-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ab6e7-134">Tipo: FORMATO DE ARCHIVO DE **[ **\_ IMAGEN \_ \_ D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="ab6e7-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ab6e7-135">Representa el formato del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ab6e7-135">Represents the format of the image file.</span></span> <span data-ttu-id="ab6e7-136">Vea FORMATO DE ARCHIVO DE [**IMAGEN D3DX10 \_ \_ \_**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="ab6e7-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab6e7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab6e7-137">Requirements</span></span>



| <span data-ttu-id="ab6e7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6e7-138">Requirement</span></span> | <span data-ttu-id="ab6e7-139">Value</span><span class="sxs-lookup"><span data-stu-id="ab6e7-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6e7-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab6e7-140">Header</span></span><br/> | <dl> <span data-ttu-id="ab6e7-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6e7-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6e7-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab6e7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6e7-143">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="ab6e7-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
