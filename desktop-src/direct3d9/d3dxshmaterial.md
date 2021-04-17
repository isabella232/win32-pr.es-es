---
description: Características del material de la transferencia Radiance (PRT) precalculada del armónico (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estructura D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717739"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="820c5-103">Estructura D3DXSHMATERIAL</span><span class="sxs-lookup"><span data-stu-id="820c5-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="820c5-104">Características del material de la transferencia Radiance (PRT) precalculada del armónico (SH).</span><span class="sxs-lookup"><span data-stu-id="820c5-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="820c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="820c5-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="820c5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="820c5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="820c5-107">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="820c5-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-109">Difusión albedo de la superficie.</span><span class="sxs-lookup"><span data-stu-id="820c5-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="820c5-110">Este valor se omite si el objeto es un reflejo.</span><span class="sxs-lookup"><span data-stu-id="820c5-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="820c5-111">**bMirror**</span><span class="sxs-lookup"><span data-stu-id="820c5-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-113">Debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="820c5-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="820c5-114">**bSubSurf**</span><span class="sxs-lookup"><span data-stu-id="820c5-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-116">Establézcalo en **true** para habilitar la dispersión de subsuperficies; cualquier objeto que realiza la dispersión de subsuperficies no puede ser un reflejo.</span><span class="sxs-lookup"><span data-stu-id="820c5-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="820c5-117">**RelativeIndexOfRefraction**</span><span class="sxs-lookup"><span data-stu-id="820c5-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-119">El Índice relativo de la refracción es la proporción entre dos índices absolutos de la refracción.</span><span class="sxs-lookup"><span data-stu-id="820c5-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="820c5-120">Un índice de refracción es la proporción entre el seno del ángulo de la incidencia y el seno del ángulo de la refracción.</span><span class="sxs-lookup"><span data-stu-id="820c5-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="820c5-121">**Absorbe**</span><span class="sxs-lookup"><span data-stu-id="820c5-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-122">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-123">El coeficiente de absorción es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación ligera en un medio participante.</span><span class="sxs-lookup"><span data-stu-id="820c5-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="820c5-124">**ReducedScattering**</span><span class="sxs-lookup"><span data-stu-id="820c5-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="820c5-125">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="820c5-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="820c5-126">El coeficiente de dispersión reducido es un parámetro de la ecuación de representación del volumen que se usa para modelar la propagación ligera en un medio participante.</span><span class="sxs-lookup"><span data-stu-id="820c5-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="820c5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="820c5-127">Remarks</span></span>

<span data-ttu-id="820c5-128">Las escenas no espectrales usan el canal rojo de los materiales en lugar del valor de luminancia.</span><span class="sxs-lookup"><span data-stu-id="820c5-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="820c5-129">Para obtener más información acerca de PRT, consulte:</span><span class="sxs-lookup"><span data-stu-id="820c5-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="820c5-130">Jensen, Henrik Wann, et al. SIGGRAPH: un modelo práctico para el transporte de luz de subsuperficie, 2001.</span><span class="sxs-lookup"><span data-stu-id="820c5-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="820c5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820c5-131">Requirements</span></span>



| <span data-ttu-id="820c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="820c5-132">Requirement</span></span> | <span data-ttu-id="820c5-133">Value</span><span class="sxs-lookup"><span data-stu-id="820c5-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="820c5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="820c5-134">Header</span></span><br/> | <dl> <span data-ttu-id="820c5-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="820c5-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="820c5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="820c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820c5-137">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="820c5-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
