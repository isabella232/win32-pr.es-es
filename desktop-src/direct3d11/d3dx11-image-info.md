---
title: D3DX11_IMAGE_INFO estructura (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_INFO estructura (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO estructura de Direct3D 11
- Puntero de estructura de LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987210"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="85b0e-107">Estructura de información de \_ imagen de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="85b0e-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="85b0e-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="85b0e-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="85b0e-109">Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas.</span><span class="sxs-lookup"><span data-stu-id="85b0e-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="85b0e-110">Un valor de D3DX11 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="85b0e-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85b0e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85b0e-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="85b0e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="85b0e-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="85b0e-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="85b0e-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-115">Ancho de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="85b0e-115">The target width of the texture.</span></span> <span data-ttu-id="85b0e-116">Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.</span><span class="sxs-lookup"><span data-stu-id="85b0e-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="85b0e-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-119">Alto de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="85b0e-119">The target height of the texture.</span></span> <span data-ttu-id="85b0e-120">Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.</span><span class="sxs-lookup"><span data-stu-id="85b0e-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-121">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="85b0e-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-123">Profundidad de la textura.</span><span class="sxs-lookup"><span data-stu-id="85b0e-123">The depth of the texture.</span></span> <span data-ttu-id="85b0e-124">Esto solo se aplica a las texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="85b0e-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="85b0e-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-127">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="85b0e-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-128">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="85b0e-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-130">Número máximo de niveles de mipmap en la textura.</span><span class="sxs-lookup"><span data-stu-id="85b0e-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="85b0e-131">Vea los comentarios de [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="85b0e-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="85b0e-132">El uso del valor predeterminado de 0 o D3DX11 hará que \_ se cree una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="85b0e-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-133">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="85b0e-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-135">Propiedades de recursos variadas especificadas con una marca de [**\_ \_ \_ marca de varios recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="85b0e-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="85b0e-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-137">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-138">Una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que especifica el formato en el que estará la textura después de cargarse.</span><span class="sxs-lookup"><span data-stu-id="85b0e-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-139">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="85b0e-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-140">Tipo: **[ **\_ \_ dimensión de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-141">Un valor de [**\_ \_ dimensión de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , que identifica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="85b0e-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="85b0e-142">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="85b0e-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="85b0e-143">Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="85b0e-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="85b0e-144">Un valor de [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md) , que identifica el formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="85b0e-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85b0e-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85b0e-145">Remarks</span></span>

<span data-ttu-id="85b0e-146">Esta estructura la usan métodos como: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="85b0e-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85b0e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85b0e-147">Requirements</span></span>



| <span data-ttu-id="85b0e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b0e-148">Requirement</span></span> | <span data-ttu-id="85b0e-149">Value</span><span class="sxs-lookup"><span data-stu-id="85b0e-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85b0e-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85b0e-150">Header</span></span><br/> | <dl> <span data-ttu-id="85b0e-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="85b0e-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b0e-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="85b0e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b0e-153">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="85b0e-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

