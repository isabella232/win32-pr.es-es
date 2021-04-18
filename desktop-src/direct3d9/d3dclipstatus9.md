---
description: Describe el estado actual del recorte.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Estructura D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717669"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="46860-103">Estructura D3DCLIPSTATUS9</span><span class="sxs-lookup"><span data-stu-id="46860-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="46860-104">Describe el estado actual del recorte.</span><span class="sxs-lookup"><span data-stu-id="46860-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="46860-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46860-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="46860-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="46860-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46860-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="46860-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="46860-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46860-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46860-109">Marcas de clip Union que describen el estado de recorte actual.</span><span class="sxs-lookup"><span data-stu-id="46860-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="46860-110">Este miembro puede ser una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="46860-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="46860-111">Value</span><span class="sxs-lookup"><span data-stu-id="46860-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="46860-112">Significado</span><span class="sxs-lookup"><span data-stu-id="46860-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="46860-113"><dt>**D3DCS \_ todo**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="46860-114">Combinación de todas las marcas de recorte.</span><span class="sxs-lookup"><span data-stu-id="46860-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="46860-115"><dt>**D3DCS a la \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="46860-116">Todos los vértices se recortan por el plano izquierdo del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="46860-117"><dt>**D3DCS \_ derecha**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="46860-118">Todos los vértices se recortan por el plano derecho del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="46860-119"><dt>**D3DCS \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="46860-120">Todos los vértices se recortan por el plano superior del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="46860-121"><dt>**D3DCS \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="46860-122">Todos los vértices se recortan por el plano inferior del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="46860-123"><dt>**D3DCS \_ Front**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="46860-124">Todos los vértices se recortan por el plano frontal del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="46860-125"><dt>**D3DCS \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="46860-126">Todos los vértices se recortan por el plano posterior del frustum de visualización.</span><span class="sxs-lookup"><span data-stu-id="46860-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="46860-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="46860-128">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="46860-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="46860-130">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="46860-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="46860-132">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="46860-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="46860-134">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="46860-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="46860-136">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="46860-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="46860-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="46860-138">Planos de recorte definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46860-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="46860-139">**ClipIntersection**</span><span class="sxs-lookup"><span data-stu-id="46860-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="46860-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46860-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46860-141">Marcas de intersección de recorte que describen el estado de recorte actual.</span><span class="sxs-lookup"><span data-stu-id="46860-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="46860-142">Este miembro puede tomar las mismas marcas que ClipUnion.</span><span class="sxs-lookup"><span data-stu-id="46860-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46860-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46860-143">Remarks</span></span>

<span data-ttu-id="46860-144">Cuando se habilita el recorte durante el procesamiento de vértices (por [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)u otras funciones de dibujo), Direct3D calcula un código de recorte para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="46860-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="46860-145">El código de recorte es una combinación de \_ \* bits D3DCS.</span><span class="sxs-lookup"><span data-stu-id="46860-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="46860-146">Cuando un vértice está fuera de un plano de recorte determinado, se establece el bit correspondiente en el código de recorte.</span><span class="sxs-lookup"><span data-stu-id="46860-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="46860-147">Direct3D mantiene el estado del recorte con **D3DCLIPSTATUS9**, que tiene los miembros ClipUnion y ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="46860-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="46860-148">ClipUnion es una operación OR bit a bit de todos los códigos de clips de vértices y ClipIntersection es una operación and bit a bit de todos los códigos de clips de vértices.</span><span class="sxs-lookup"><span data-stu-id="46860-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="46860-149">Los valores iniciales son cero para ClipUnion y 0xFFFFFFFF para ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="46860-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="46860-150">Cuando \_ recorte D3DRS se establece en **false**, ClipUnion y ClipIntersection se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="46860-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="46860-151">Direct3D actualiza el estado del recorte durante las llamadas de dibujo.</span><span class="sxs-lookup"><span data-stu-id="46860-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="46860-152">Para calcular el estado del clip para un objeto determinado, establezca ClipUnion y ClipIntersection en su valor inicial y continúe con el dibujo.</span><span class="sxs-lookup"><span data-stu-id="46860-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="46860-153">[**DrawRectPatch**](/windows/desktop/api) y [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) no actualizan el estado del recorte porque no hay ninguna emulación de software para ellos.</span><span class="sxs-lookup"><span data-stu-id="46860-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="46860-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46860-154">Requirements</span></span>



| <span data-ttu-id="46860-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="46860-155">Requirement</span></span> | <span data-ttu-id="46860-156">Value</span><span class="sxs-lookup"><span data-stu-id="46860-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46860-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46860-157">Header</span></span><br/> | <dl> <span data-ttu-id="46860-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="46860-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46860-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="46860-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46860-160">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="46860-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="46860-161">**GetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="46860-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="46860-162">**SetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="46860-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
