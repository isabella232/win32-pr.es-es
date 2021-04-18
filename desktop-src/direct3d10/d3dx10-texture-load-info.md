---
description: Describe los parámetros que se usan para cargar una textura de otra textura.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO estructura (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721483"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="82dc5-103">D3DX10 \_ \_ estructura de información de carga de textura \_</span><span class="sxs-lookup"><span data-stu-id="82dc5-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="82dc5-104">Describe los parámetros que se usan para cargar una textura de otra textura.</span><span class="sxs-lookup"><span data-stu-id="82dc5-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dc5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82dc5-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="82dc5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="82dc5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82dc5-107">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="82dc5-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-108">Escriba: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="82dc5-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-109">Cuadro de textura de origen (vea [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="82dc5-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-110">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="82dc5-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-111">Escriba: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="82dc5-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-112">Cuadro de textura de destino (vea [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="82dc5-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-113">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="82dc5-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-115">Nivel de mipmap de textura de origen, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="82dc5-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-116">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="82dc5-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-118">Nivel de mipmap de textura de destino, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="82dc5-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-119">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="82dc5-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-121">Número de niveles de mipmap en la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="82dc5-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-122">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="82dc5-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-124">Primer elemento de la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="82dc5-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-125">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="82dc5-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-127">Primer elemento de la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="82dc5-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="82dc5-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-130">Número de elementos que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="82dc5-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="82dc5-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-133">Opciones de filtrado durante el remuestreo (vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="82dc5-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="82dc5-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="82dc5-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="82dc5-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82dc5-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82dc5-136">Opciones de filtrado al generar niveles de MIP (vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="82dc5-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82dc5-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82dc5-137">Remarks</span></span>

<span data-ttu-id="82dc5-138">Esta estructura se usa en una llamada a [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="82dc5-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82dc5-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82dc5-139">Requirements</span></span>



| <span data-ttu-id="82dc5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="82dc5-140">Requirement</span></span> | <span data-ttu-id="82dc5-141">Value</span><span class="sxs-lookup"><span data-stu-id="82dc5-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82dc5-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82dc5-142">Header</span></span><br/> | <dl> <span data-ttu-id="82dc5-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="82dc5-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82dc5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="82dc5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82dc5-145">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="82dc5-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
