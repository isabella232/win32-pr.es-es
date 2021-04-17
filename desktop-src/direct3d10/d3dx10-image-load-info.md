---
description: Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX10 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: D3DX10_IMAGE_LOAD_INFO estructura (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718433"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="fd2c6-104">\_Estructura de \_ información de carga de imagen de D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="fd2c6-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="fd2c6-105">Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="fd2c6-106">Un valor de D3DX10 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd2c6-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="fd2c6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd2c6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd2c6-109">**Width**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-111">Ancho de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-111">The target width of the texture.</span></span> <span data-ttu-id="fd2c6-112">Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-113">**Height**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-115">Alto de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-115">The target height of the texture.</span></span> <span data-ttu-id="fd2c6-116">Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-117">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-119">Profundidad de la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-119">The depth of the texture.</span></span> <span data-ttu-id="fd2c6-120">Esto solo se aplica a las texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-121">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-123">Nivel de mipmap de resolución más alto de la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="fd2c6-124">Si es mayor que 0, después de que se cargue la textura, FirstMipLevel se asignará al nivel 0 del mipmap.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-125">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-127">Número máximo de niveles de mipmap que tendrá la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="fd2c6-128">El uso del valor predeterminado de 0 o D3DX10 hará que \_ se cree una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-129">**Uso**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-130">Tipo: **[ **\_ uso de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-131">La forma en que se va a usar el recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="fd2c6-132">Vea [**\_ uso de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-135">Fases de canalización a las que se puede enlazar la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="fd2c6-136">Vea [**D3D10 \_ BIND \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-137">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-139">Los permisos de acceso que tendrá la CPU para el recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="fd2c6-140">Consulte [**\_ marca de \_ acceso \_ de CPU de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-141">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-143">Propiedades de recursos misceláneas (consulte la [**marca D3D10 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-144">**Format**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-145">Tipo: **[ **\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-146">Formato en el que estará la textura después de cargarse.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="fd2c6-147">Consulte [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-149">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-150">Filtre la textura mediante el filtro especificado (solo cuando se remuestre).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="fd2c6-151">Vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-153">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-154">Filtre los niveles de textura de MIP mediante el filtro especificado (solo si se generan mapas MIP).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="fd2c6-155">Los valores válidos son D3DX10 \_ Filter \_ None, D3DX10 Filter \_ \_ Point, D3DX10 \_ Filter \_ linear o D3DX10 \_ Filter \_ Triangle.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="fd2c6-156">Vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd2c6-157">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="fd2c6-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="fd2c6-158">Tipo: **[ **\_ \_ información de imagen de D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd2c6-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="fd2c6-159">Información sobre la imagen original.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-159">Information about the original image.</span></span> <span data-ttu-id="fd2c6-160">Consulte [**la \_ \_ información**](d3dx10-image-info.md)de la imagen de D3DX10.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="fd2c6-161">Se puede obtener con [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)o [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd2c6-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd2c6-162">Remarks</span></span>

<span data-ttu-id="fd2c6-163">Al inicializar la estructura, puede establecer cualquier miembro en D3DX10 \_ default y D3DX lo inicializará con un valor predeterminado de la textura de origen cuando se cargue la textura.</span><span class="sxs-lookup"><span data-stu-id="fd2c6-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="fd2c6-164">Esta estructura la pueden usar las API que:</span><span class="sxs-lookup"><span data-stu-id="fd2c6-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="fd2c6-165">Cree recursos, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="fd2c6-166">Cree procesadores de datos, como [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) o [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c6-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2c6-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd2c6-167">Requirements</span></span>



| <span data-ttu-id="fd2c6-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2c6-168">Requirement</span></span> | <span data-ttu-id="fd2c6-169">Value</span><span class="sxs-lookup"><span data-stu-id="fd2c6-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2c6-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd2c6-170">Header</span></span><br/> | <dl> <span data-ttu-id="fd2c6-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd2c6-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd2c6-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd2c6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2c6-173">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="fd2c6-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
