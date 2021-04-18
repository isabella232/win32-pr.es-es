---
description: Define las dimensiones de la ventana de una superficie de representación-destino en la que se proyecta un volumen 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Estructura D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718312"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="c3b16-103">Estructura D3DVIEWPORT9</span><span class="sxs-lookup"><span data-stu-id="c3b16-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="c3b16-104">Define las dimensiones de la ventana de una superficie de representación-destino en la que se proyecta un volumen 3D.</span><span class="sxs-lookup"><span data-stu-id="c3b16-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3b16-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="c3b16-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3b16-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3b16-107">**X**</span><span class="sxs-lookup"><span data-stu-id="c3b16-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b16-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-109">Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c3b16-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="c3b16-110">A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="c3b16-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c3b16-111">**S**</span><span class="sxs-lookup"><span data-stu-id="c3b16-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b16-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-113">Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c3b16-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="c3b16-114">A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="c3b16-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c3b16-115">**Width**</span><span class="sxs-lookup"><span data-stu-id="c3b16-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b16-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-117">Dimensión de ancho del volumen de clip, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c3b16-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="c3b16-118">A menos que esté representando solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de ancho de la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c3b16-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="c3b16-119">**Height**</span><span class="sxs-lookup"><span data-stu-id="c3b16-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b16-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-121">Dimensión de alto del volumen de clip, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c3b16-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="c3b16-122">A menos que esté representando solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de alto de la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c3b16-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="c3b16-123">**MinZ**</span><span class="sxs-lookup"><span data-stu-id="c3b16-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c3b16-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-125">Junto con MaxZ, valor que describe el intervalo de valores de profundidad en el que se va a representar una escena, los valores mínimo y máximo del volumen de recorte.</span><span class="sxs-lookup"><span data-stu-id="c3b16-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="c3b16-126">La mayoría de las aplicaciones establecen este valor en 0,0.</span><span class="sxs-lookup"><span data-stu-id="c3b16-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="c3b16-127">El recorte se realiza después de aplicar la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="c3b16-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c3b16-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="c3b16-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="c3b16-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c3b16-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="c3b16-130">Junto con MinZ, valor que describe el intervalo de valores de profundidad en el que se va a representar una escena, los valores mínimo y máximo del volumen de recorte.</span><span class="sxs-lookup"><span data-stu-id="c3b16-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="c3b16-131">La mayoría de las aplicaciones establecen este valor en 1,0.</span><span class="sxs-lookup"><span data-stu-id="c3b16-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="c3b16-132">El recorte se realiza después de aplicar la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="c3b16-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3b16-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3b16-133">Remarks</span></span>

<span data-ttu-id="c3b16-134">Los miembros X, Y, ancho y alto describen la posición y las dimensiones de la ventanilla en la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c3b16-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="c3b16-135">Normalmente, las aplicaciones se representan en toda la superficie de destino; Cuando se representa en una superficie de 640 x 480, estos miembros deben ser 0, 0, 640 y 480, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c3b16-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="c3b16-136">MinZ y MaxZ se establecen normalmente en 0,0 y 1,0, pero se pueden establecer en otros valores para lograr efectos concretos.</span><span class="sxs-lookup"><span data-stu-id="c3b16-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="c3b16-137">Por ejemplo, puede establecer ambos en 0,0 para obligar al sistema a representar objetos en el primer plano de una escena, o ambos en 1,0 para forzar los objetos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c3b16-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="c3b16-138">Cuando los parámetros de la ventanilla para un dispositivo cambian (debido a una llamada al método [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), el controlador genera una nueva matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="c3b16-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b16-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3b16-139">Requirements</span></span>



| <span data-ttu-id="c3b16-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3b16-140">Requirement</span></span> | <span data-ttu-id="c3b16-141">Value</span><span class="sxs-lookup"><span data-stu-id="c3b16-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b16-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3b16-142">Header</span></span><br/> | <dl> <span data-ttu-id="c3b16-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3b16-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b16-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3b16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b16-145">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c3b16-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c3b16-146">**GetViewport**</span><span class="sxs-lookup"><span data-stu-id="c3b16-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="c3b16-147">**SetViewport**</span><span class="sxs-lookup"><span data-stu-id="c3b16-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
