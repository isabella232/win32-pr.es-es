---
title: D3DX11_TEXTURE_LOAD_INFO estructura (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Describe los parámetros que se usan para cargar una textura de otra textura.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998574"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="829e6-105">D3DX11 \_ \_ estructura de información de carga de textura \_</span><span class="sxs-lookup"><span data-stu-id="829e6-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="829e6-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="829e6-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="829e6-107">Describe los parámetros que se usan para cargar una textura de otra textura.</span><span class="sxs-lookup"><span data-stu-id="829e6-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="829e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="829e6-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="829e6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="829e6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="829e6-110">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="829e6-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-111">Escriba: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="829e6-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="829e6-112">Cuadro de textura de origen (vea [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="829e6-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="829e6-113">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="829e6-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-114">Escriba: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="829e6-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="829e6-115">Cuadro de textura de destino (vea [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="829e6-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="829e6-116">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="829e6-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-118">Nivel de mipmap de textura de origen, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="829e6-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-119">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="829e6-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-121">Nivel de mipmap de textura de destino, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="829e6-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-122">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="829e6-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-124">Número de niveles de mipmap en la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="829e6-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-125">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="829e6-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-127">Primer elemento de la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="829e6-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-128">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="829e6-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-130">Primer elemento de la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="829e6-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="829e6-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-133">Número de elementos que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="829e6-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="829e6-134">**Filtrar**</span><span class="sxs-lookup"><span data-stu-id="829e6-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-135">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-136">Opciones de filtrado durante el remuestreo (vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="829e6-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="829e6-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="829e6-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="829e6-138">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="829e6-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="829e6-139">Opciones de filtrado al generar niveles de MIP (vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="829e6-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="829e6-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="829e6-140">Remarks</span></span>

<span data-ttu-id="829e6-141">Esta estructura se usa en una llamada a [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="829e6-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="829e6-142">Los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="829e6-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="829e6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="829e6-143">Requirements</span></span>



| <span data-ttu-id="829e6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="829e6-144">Requirement</span></span> | <span data-ttu-id="829e6-145">Value</span><span class="sxs-lookup"><span data-stu-id="829e6-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="829e6-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="829e6-146">Header</span></span><br/> | <dl> <span data-ttu-id="829e6-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="829e6-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829e6-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="829e6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829e6-149">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="829e6-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

