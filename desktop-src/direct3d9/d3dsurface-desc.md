---
description: Describe una superficie.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717689"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="48440-103">D3DSURFACE \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="48440-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="48440-104">Describe una superficie.</span><span class="sxs-lookup"><span data-stu-id="48440-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="48440-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48440-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="48440-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="48440-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="48440-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="48440-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="48440-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-109">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de la superficie.</span><span class="sxs-lookup"><span data-stu-id="48440-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="48440-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48440-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="48440-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-112">Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como una superficie.</span><span class="sxs-lookup"><span data-stu-id="48440-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="48440-113">**Uso**</span><span class="sxs-lookup"><span data-stu-id="48440-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="48440-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-115">Los valores D3DUSAGE \_ DEPTHSTENCIL o D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="48440-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="48440-116">Para obtener más información, vea [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="48440-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="48440-117">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="48440-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="48440-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-119">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para esta superficie.</span><span class="sxs-lookup"><span data-stu-id="48440-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="48440-120">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="48440-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="48440-121">Tipo: **[ **D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-122">Miembro del tipo enumerado de [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) , que especifica los niveles de muestreo múltiple de escena completa admitidos por la superficie.</span><span class="sxs-lookup"><span data-stu-id="48440-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="48440-123">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="48440-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="48440-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-125">Nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="48440-125">Quality level.</span></span> <span data-ttu-id="48440-126">El intervalo válido está comprendido entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="48440-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="48440-127">Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="48440-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="48440-128">Los valores MultisampleQuality de los destinos de presentación emparejados, las superficies de estarcido de profundidad y el tipo de Multimuestra deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="48440-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="48440-129">**Width**</span><span class="sxs-lookup"><span data-stu-id="48440-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="48440-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-131">Ancho de la superficie, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="48440-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="48440-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="48440-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="48440-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48440-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48440-134">Alto de la superficie, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="48440-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48440-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48440-135">Requirements</span></span>



| <span data-ttu-id="48440-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="48440-136">Requirement</span></span> | <span data-ttu-id="48440-137">Value</span><span class="sxs-lookup"><span data-stu-id="48440-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48440-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48440-138">Header</span></span><br/> | <dl> <span data-ttu-id="48440-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="48440-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48440-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="48440-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48440-141">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="48440-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="48440-142">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="48440-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="48440-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="48440-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="48440-144">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="48440-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
