---
description: Devuelve una descripción del contenido original de un archivo de imagen.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO estructura (D3DX10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362487"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="18254-103">Estructura de información de \_ imagen de D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="18254-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="18254-104">Devuelve una descripción del contenido original de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="18254-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="18254-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18254-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="18254-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="18254-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18254-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="18254-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="18254-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-109">Ancho de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="18254-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18254-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="18254-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="18254-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-112">Alto de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="18254-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18254-113">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="18254-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="18254-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-115">Profundidad de la imagen original en píxeles.</span><span class="sxs-lookup"><span data-stu-id="18254-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18254-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="18254-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="18254-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-118">Tamaño de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="18254-118">Size of the texture array.</span></span> <span data-ttu-id="18254-119">*Tamaño* será 1 para una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="18254-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="18254-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="18254-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="18254-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-122">Número de niveles de mipmap en la imagen original.</span><span class="sxs-lookup"><span data-stu-id="18254-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="18254-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="18254-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="18254-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-125">Propiedades de recursos misceláneas (consulte la [**marca D3D10 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="18254-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="18254-126">**Format**</span><span class="sxs-lookup"><span data-stu-id="18254-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="18254-127">Tipo: **[ **\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="18254-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-128">Un valor del tipo [**de \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerado que describe mejor los datos de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="18254-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="18254-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="18254-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="18254-130">Tipo: **[ **\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="18254-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-131">Representa el tipo de la textura almacenada en el archivo.</span><span class="sxs-lookup"><span data-stu-id="18254-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="18254-132">Consulte [**\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="18254-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="18254-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="18254-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="18254-134">Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="18254-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18254-135">Representa el formato del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="18254-135">Represents the format of the image file.</span></span> <span data-ttu-id="18254-136">Consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="18254-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18254-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18254-137">Requirements</span></span>



| <span data-ttu-id="18254-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="18254-138">Requirement</span></span> | <span data-ttu-id="18254-139">Value</span><span class="sxs-lookup"><span data-stu-id="18254-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18254-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18254-140">Header</span></span><br/> | <dl> <span data-ttu-id="18254-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="18254-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18254-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="18254-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18254-143">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="18254-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
