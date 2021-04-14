---
description: Especifica las propiedades del material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estructura D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424424"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="cec97-103">Estructura D3DMATERIAL9</span><span class="sxs-lookup"><span data-stu-id="cec97-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="cec97-104">Especifica las propiedades del material.</span><span class="sxs-lookup"><span data-stu-id="cec97-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cec97-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="cec97-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cec97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cec97-107">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="cec97-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="cec97-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="cec97-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cec97-109">Valor que especifica el color difuso del material.</span><span class="sxs-lookup"><span data-stu-id="cec97-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="cec97-110">Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec97-111">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="cec97-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="cec97-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="cec97-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cec97-113">Valor que especifica el color ambiente del material.</span><span class="sxs-lookup"><span data-stu-id="cec97-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="cec97-114">Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec97-115">**Especular**</span><span class="sxs-lookup"><span data-stu-id="cec97-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="cec97-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="cec97-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cec97-117">Valor que especifica el color especular del material.</span><span class="sxs-lookup"><span data-stu-id="cec97-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="cec97-118">Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec97-119">**Emisor de luz**</span><span class="sxs-lookup"><span data-stu-id="cec97-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="cec97-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="cec97-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cec97-121">Valor que especifica el color de emisor del material.</span><span class="sxs-lookup"><span data-stu-id="cec97-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="cec97-122">Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec97-123">**Power**</span><span class="sxs-lookup"><span data-stu-id="cec97-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="cec97-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cec97-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="cec97-125">Valor de punto flotante que especifica la nitidez de los reflejos especulares.</span><span class="sxs-lookup"><span data-stu-id="cec97-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="cec97-126">Cuanto mayor sea el valor, más nítido será el resaltado.</span><span class="sxs-lookup"><span data-stu-id="cec97-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cec97-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cec97-127">Remarks</span></span>

<span data-ttu-id="cec97-128">Para desactivar las iluminaciones especulares, establezca D3DRS \_ SPECULARENABLE en **false**, con [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="cec97-129">Esta es la opción más rápida porque no se calcularán los reflejos especulares.</span><span class="sxs-lookup"><span data-stu-id="cec97-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="cec97-130">Para obtener más información sobre el uso del motor de iluminación para calcular la iluminación especular, vea [iluminación especular (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="cec97-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cec97-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cec97-131">Requirements</span></span>



| <span data-ttu-id="cec97-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec97-132">Requirement</span></span> | <span data-ttu-id="cec97-133">Value</span><span class="sxs-lookup"><span data-stu-id="cec97-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cec97-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cec97-134">Header</span></span><br/> | <dl> <span data-ttu-id="cec97-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec97-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec97-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cec97-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec97-137">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="cec97-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="cec97-138">**IDirect3DDevice9::GetMaterial**</span><span class="sxs-lookup"><span data-stu-id="cec97-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="cec97-139">**IDirect3DDevice9::SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="cec97-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
