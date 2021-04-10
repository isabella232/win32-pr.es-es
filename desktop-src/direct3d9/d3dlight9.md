---
description: Define un conjunto de propiedades de iluminación.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Estructura D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280375"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="f0e61-103">Estructura D3DLIGHT9</span><span class="sxs-lookup"><span data-stu-id="f0e61-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="f0e61-104">Define un conjunto de propiedades de iluminación.</span><span class="sxs-lookup"><span data-stu-id="f0e61-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0e61-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="f0e61-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0e61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0e61-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0e61-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-108">Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-109">Tipo de la fuente de luz.</span><span class="sxs-lookup"><span data-stu-id="f0e61-109">Type of the light source.</span></span> <span data-ttu-id="f0e61-110">Este valor es uno de los miembros del tipo enumerado [**D3DLIGHTTYPE**](./d3dlighttype.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-111">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="f0e61-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-113">Color difuso emitido por la luz.</span><span class="sxs-lookup"><span data-stu-id="f0e61-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="f0e61-114">Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-115">**Especular**</span><span class="sxs-lookup"><span data-stu-id="f0e61-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-117">Color especular emitido por la luz.</span><span class="sxs-lookup"><span data-stu-id="f0e61-117">Specular color emitted by the light.</span></span> <span data-ttu-id="f0e61-118">Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-119">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="f0e61-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-121">Color ambiente emitido por la luz.</span><span class="sxs-lookup"><span data-stu-id="f0e61-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="f0e61-122">Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-123">**Position**</span><span class="sxs-lookup"><span data-stu-id="f0e61-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-124">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-125">Posición de la luz en el espacio universal, especificada por una estructura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="f0e61-126">Este miembro no tiene ningún significado para las luces direccionales y se omite en ese caso.</span><span class="sxs-lookup"><span data-stu-id="f0e61-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-127">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="f0e61-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-128">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="f0e61-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-129">Dirección en la que apunta la luz en el espacio universal, especificado por una estructura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e61-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="f0e61-130">Este miembro solo tiene significado para direccional y Spotlight.</span><span class="sxs-lookup"><span data-stu-id="f0e61-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="f0e61-131">No es necesario normalizar este vector, pero debe tener una longitud que no sea cero.</span><span class="sxs-lookup"><span data-stu-id="f0e61-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-132">**Range**</span><span class="sxs-lookup"><span data-stu-id="f0e61-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-134">Distancia más allá de la cual la luz no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="f0e61-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="f0e61-135">El valor máximo permitido para este miembro es la raíz cuadrada de FLT \_ máx.</span><span class="sxs-lookup"><span data-stu-id="f0e61-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="f0e61-136">Este miembro no afecta a las luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="f0e61-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-137">**Disminución**</span><span class="sxs-lookup"><span data-stu-id="f0e61-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-139">Disminuya la iluminación entre el cono interior de un foco (el ángulo especificado por Theta) y el borde exterior del cono exterior (el ángulo especificado por la PHI).</span><span class="sxs-lookup"><span data-stu-id="f0e61-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="f0e61-140">El efecto de la caída en la iluminación es sutil.</span><span class="sxs-lookup"><span data-stu-id="f0e61-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="f0e61-141">Además, se incurre en una pequeña reducción del rendimiento dando forma a la curva de difuminación.</span><span class="sxs-lookup"><span data-stu-id="f0e61-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="f0e61-142">Por estos motivos, la mayoría de los desarrolladores establecen este valor en 1,0.</span><span class="sxs-lookup"><span data-stu-id="f0e61-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="f0e61-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-145">Valor que especifica cómo cambia la intensidad de la luz con la distancia.</span><span class="sxs-lookup"><span data-stu-id="f0e61-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="f0e61-146">Los valores de atenuación se omiten para las luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="f0e61-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="f0e61-147">Este miembro representa una constante de atenuación.</span><span class="sxs-lookup"><span data-stu-id="f0e61-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="f0e61-148">Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f0e61-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="f0e61-149">Valores válidos para este intervalo de miembros de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="f0e61-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="f0e61-150">En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0e61-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="f0e61-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-152">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-153">Valor que especifica cómo cambia la intensidad de la luz con la distancia.</span><span class="sxs-lookup"><span data-stu-id="f0e61-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="f0e61-154">Los valores de atenuación se omiten para las luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="f0e61-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="f0e61-155">Este miembro representa una constante de atenuación.</span><span class="sxs-lookup"><span data-stu-id="f0e61-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="f0e61-156">Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f0e61-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="f0e61-157">Valores válidos para este intervalo de miembros de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="f0e61-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="f0e61-158">En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0e61-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="f0e61-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-160">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-161">Valor que especifica cómo cambia la intensidad de la luz con la distancia.</span><span class="sxs-lookup"><span data-stu-id="f0e61-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="f0e61-162">Los valores de atenuación se omiten para las luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="f0e61-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="f0e61-163">Este miembro representa una constante de atenuación.</span><span class="sxs-lookup"><span data-stu-id="f0e61-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="f0e61-164">Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f0e61-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="f0e61-165">Valores válidos para este intervalo de miembros de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="f0e61-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="f0e61-166">En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0e61-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-167">**Zeta**</span><span class="sxs-lookup"><span data-stu-id="f0e61-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-168">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-169">Ángulo, en radianes, del cono interior de un foco, es decir, el cono de foco de luz completamente iluminado.</span><span class="sxs-lookup"><span data-stu-id="f0e61-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="f0e61-170">Este valor debe estar en el intervalo comprendido entre 0 y el valor especificado por Phi.</span><span class="sxs-lookup"><span data-stu-id="f0e61-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="f0e61-171">**Su**</span><span class="sxs-lookup"><span data-stu-id="f0e61-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="f0e61-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f0e61-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="f0e61-173">Ángulo, en radianes, que define el borde exterior del cono exterior del foco.</span><span class="sxs-lookup"><span data-stu-id="f0e61-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="f0e61-174">Los puntos fuera de este cono no están iluminados por el foco.</span><span class="sxs-lookup"><span data-stu-id="f0e61-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="f0e61-175">Este valor debe estar comprendido entre 0 y PI.</span><span class="sxs-lookup"><span data-stu-id="f0e61-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0e61-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0e61-176">Requirements</span></span>



| <span data-ttu-id="f0e61-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0e61-177">Requirement</span></span> | <span data-ttu-id="f0e61-178">Value</span><span class="sxs-lookup"><span data-stu-id="f0e61-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e61-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0e61-179">Header</span></span><br/> | <dl> <span data-ttu-id="f0e61-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e61-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e61-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0e61-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e61-182">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="f0e61-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f0e61-183">**GetLight**</span><span class="sxs-lookup"><span data-stu-id="f0e61-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="f0e61-184">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="f0e61-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
