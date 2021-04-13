---
description: Define el método de declaración de vértices, que es una operación predefinida realizada por del teselador (o cualquier rutina de geometría de procedimiento en los datos de vértice durante la teselación).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumeración D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362476"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="27ced-103">Enumeración D3DDECLMETHOD</span><span class="sxs-lookup"><span data-stu-id="27ced-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="27ced-104">Define el método de declaración de vértices, que es una operación predefinida realizada por del teselador (o cualquier rutina de geometría de procedimiento en los datos de vértice durante la teselación).</span><span class="sxs-lookup"><span data-stu-id="27ced-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="27ced-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27ced-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="27ced-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="27ced-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="27ced-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**\_Valor predeterminado de D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="27ced-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-108">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27ced-108">Default value.</span></span> <span data-ttu-id="27ced-109">El del teselador copia los datos de vértice (datos de spline para las revisiones) tal cual, sin cálculos adicionales.</span><span class="sxs-lookup"><span data-stu-id="27ced-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="27ced-110">Cuando se usa del teselador, se interpola este elemento.</span><span class="sxs-lookup"><span data-stu-id="27ced-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="27ced-111">En caso contrario, los datos de vértice se copian en el registro de entrada.</span><span class="sxs-lookup"><span data-stu-id="27ced-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="27ced-112">El tipo de entrada y salida puede ser cualquier valor, pero siempre son del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="27ced-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="27ced-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**</span><span class="sxs-lookup"><span data-stu-id="27ced-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-114">Calcula la tangente en un punto de la revisión del rectángulo o del triángulo en la dirección U.</span><span class="sxs-lookup"><span data-stu-id="27ced-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="27ced-115">El tipo de entrada puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27ced-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="27ced-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="27ced-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="27ced-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="27ced-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="27ced-118">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="27ced-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="27ced-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="27ced-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="27ced-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="27ced-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="27ced-121">El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="27ced-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="27ced-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**</span><span class="sxs-lookup"><span data-stu-id="27ced-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-123">Calcula la tangente en un punto de la revisión del rectángulo o del triángulo en la dirección V.</span><span class="sxs-lookup"><span data-stu-id="27ced-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="27ced-124">El tipo de entrada puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27ced-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="27ced-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="27ced-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="27ced-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="27ced-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="27ced-127">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="27ced-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="27ced-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="27ced-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="27ced-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="27ced-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="27ced-130">El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="27ced-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="27ced-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**</span><span class="sxs-lookup"><span data-stu-id="27ced-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-132">Calcula el normal en un punto de la revisión del rectángulo o del triángulo tomando el producto cruzado de dos tangentes.</span><span class="sxs-lookup"><span data-stu-id="27ced-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="27ced-133">El tipo de entrada puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27ced-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="27ced-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="27ced-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="27ced-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="27ced-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="27ced-136">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="27ced-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="27ced-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="27ced-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="27ced-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="27ced-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="27ced-139">El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="27ced-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="27ced-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**UV de D3DDECLMETHOD \_**</span><span class="sxs-lookup"><span data-stu-id="27ced-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-141">Copie los valores de U, V en un punto de la revisión de rectángulo o triángulo.</span><span class="sxs-lookup"><span data-stu-id="27ced-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="27ced-142">Esto da como resultado un float 2D.</span><span class="sxs-lookup"><span data-stu-id="27ced-142">This results in a 2D float.</span></span> <span data-ttu-id="27ced-143">El tipo de entrada debe establecerse en D3DDECLTYPE \_ sin usar.</span><span class="sxs-lookup"><span data-stu-id="27ced-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="27ced-144">El tipo de datos de salida siempre es D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="27ced-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="27ced-145">El flujo de entrada y el desplazamiento también están sin usar (pero debe establecerse en 0).</span><span class="sxs-lookup"><span data-stu-id="27ced-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="27ced-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Búsqueda D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="27ced-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-147">Buscar un mapa de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="27ced-147">Look up a displacement map.</span></span> <span data-ttu-id="27ced-148">El tipo de entrada puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27ced-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="27ced-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="27ced-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="27ced-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="27ced-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="27ced-151">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="27ced-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="27ced-152">Solo se usan los componentes. x y. y para la búsqueda de mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="27ced-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="27ced-153">El tipo de salida siempre es D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="27ced-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="27ced-154">El dispositivo debe admitir la asignación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="27ced-154">The device must support displacement mapping.</span></span> <span data-ttu-id="27ced-155">Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="27ced-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="27ced-156">Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las revisiones N.</span><span class="sxs-lookup"><span data-stu-id="27ced-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="27ced-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**</span><span class="sxs-lookup"><span data-stu-id="27ced-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="27ced-158">Buscar un mapa de desplazamiento premuestreado.</span><span class="sxs-lookup"><span data-stu-id="27ced-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="27ced-159">El tipo de entrada debe establecerse en D3DDECLTYPE \_ sin usar; el índice de flujo y el desplazamiento de flujo deben establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="27ced-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="27ced-160">El tipo de salida de esta operación siempre es D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="27ced-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="27ced-161">El dispositivo debe admitir la asignación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="27ced-161">The device must support displacement mapping.</span></span> <span data-ttu-id="27ced-162">Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="27ced-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="27ced-163">Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las revisiones N.</span><span class="sxs-lookup"><span data-stu-id="27ced-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="27ced-164">Este método solo se puede usar con el \_ ejemplo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="27ced-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27ced-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27ced-165">Remarks</span></span>

<span data-ttu-id="27ced-166">Del teselador examina el método para determinar qué datos se deben calcular a partir de los datos de vértice durante la teselación.</span><span class="sxs-lookup"><span data-stu-id="27ced-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="27ced-167">Los datos de la malla deben usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27ced-167">Mesh data should use the default value.</span></span> <span data-ttu-id="27ced-168">Las revisiones pueden utilizar cualquiera de los otros tipos implementados.</span><span class="sxs-lookup"><span data-stu-id="27ced-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="27ced-169">Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="27ced-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="27ced-170">Cada elemento de la matriz contiene un método de declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="27ced-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="27ced-171">Además de usar \_ el valor predeterminado de D3DDECLMETHOD, una malla normal puede usar \_ los métodos D3DDECLMETHOD Lookup y D3DDECLMETHOD \_ LOOKUPPRESAMPLED cuando se habilitan N-patches.</span><span class="sxs-lookup"><span data-stu-id="27ced-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ced-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27ced-172">Requirements</span></span>



| <span data-ttu-id="27ced-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="27ced-173">Requirement</span></span> | <span data-ttu-id="27ced-174">Value</span><span class="sxs-lookup"><span data-stu-id="27ced-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27ced-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27ced-175">Header</span></span><br/> | <dl> <span data-ttu-id="27ced-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="27ced-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27ced-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="27ced-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ced-178">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="27ced-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




