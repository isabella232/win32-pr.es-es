---
description: Cómo la canalización interpreta los datos de vértices que están enlazados a la fase de ensamblador de entrada. Estos valores de topología primitiva determinan cómo se representan los datos de vértices en la pantalla.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ \_ enumeración de topología primitiva
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998001"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="2a99f-104">D3D11 \_ \_ enumeración de topología primitiva</span><span class="sxs-lookup"><span data-stu-id="2a99f-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="2a99f-105">Cómo la canalización interpreta los datos de vértices que están enlazados a la fase de ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a99f-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="2a99f-106">Estos valores de topología primitiva determinan cómo se representan los datos de vértices en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2a99f-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a99f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a99f-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="2a99f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2a99f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2a99f-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topología primitiva D3D11 \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="2a99f-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-110">La fase del IA no se ha inicializado con una topología primitiva.</span><span class="sxs-lookup"><span data-stu-id="2a99f-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="2a99f-111">La fase del IA no funcionará correctamente a menos que se defina una topología primitiva.</span><span class="sxs-lookup"><span data-stu-id="2a99f-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ \_ topología primitiva \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-113">Interprete los datos de vértice como una lista de puntos.</span><span class="sxs-lookup"><span data-stu-id="2a99f-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ \_ topología primitiva \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-115">Interprete los datos de vértice como una lista de líneas.</span><span class="sxs-lookup"><span data-stu-id="2a99f-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ \_ topología primitiva \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="2a99f-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-117">Interprete los datos de vértice como una franja de líneas.</span><span class="sxs-lookup"><span data-stu-id="2a99f-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ \_ topología primitiva \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-119">Interprete los datos de vértice como una lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="2a99f-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ \_ topología primitiva \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="2a99f-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-121">Interprete los datos de vértice como una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="2a99f-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ \_ \_ LINELIST ADJ de topología \_ primitiva**</span><span class="sxs-lookup"><span data-stu-id="2a99f-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-123">Interprete los datos de vértices como una lista de líneas con datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="2a99f-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ \_ LINESTRIP ADJ de topología \_ primitiva**</span><span class="sxs-lookup"><span data-stu-id="2a99f-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-125">Interprete los datos de vértices como franja de líneas con datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="2a99f-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ \_ \_ TRIANGLELIST ADJ de topología \_ primitiva**</span><span class="sxs-lookup"><span data-stu-id="2a99f-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-127">Interprete los datos de vértices como una lista de triángulos con datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="2a99f-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ \_ TRIANGLESTRIP ADJ de topología \_ primitiva**</span><span class="sxs-lookup"><span data-stu-id="2a99f-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-129">Interprete los datos de vértices como franja de triángulo con datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="2a99f-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 1 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-131">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 2 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-133">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 3 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-135">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 4 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-137">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 5 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-139">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 6 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-141">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 7 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-143">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 8 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-145">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 9 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-147">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 10 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-149">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 11 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-151">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 12 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-153">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 13 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-155">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 14 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-157">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 15 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-159">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 16 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-161">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 17 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-163">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 18 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-165">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**Punto de control de la \_ topología primitiva de D3D11 \_ \_ 19 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-167">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 20 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-169">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 21 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-171">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-173">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 23 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-175">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 24 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-177">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 25 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-179">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 26 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-181">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 27 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-183">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 28 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-185">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-187">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 30 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-189">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-191">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2a99f-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 32 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="2a99f-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2a99f-193">Interprete los datos de vértice como una lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="2a99f-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a99f-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a99f-194">Remarks</span></span>

<span data-ttu-id="2a99f-195">La enumeración de **\_ \_ topología primitiva D3D11** es el tipo definido en el archivo de encabezado D3D11. h como una enumeración de [**\_ \_ topología de D3D primitivo**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , que está totalmente definida en el archivo de encabezado D3DCommon. h.</span><span class="sxs-lookup"><span data-stu-id="2a99f-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
