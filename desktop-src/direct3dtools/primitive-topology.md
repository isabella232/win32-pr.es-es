---
description: Enumeración que se usa para indicar la topología de una malla. Vea MeshDataVertCallback.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PRIMITIVE_TOPOLOGY
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080060"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="91755-104"><span id="vspixengine.primitive_topology"></span>\_Enumeración de topología primitiva</span><span class="sxs-lookup"><span data-stu-id="91755-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="91755-105">Enumeración que se usa para indicar la topología de una malla.</span><span class="sxs-lookup"><span data-stu-id="91755-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="91755-106">Vea MeshDataVertCallback.</span><span class="sxs-lookup"><span data-stu-id="91755-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="91755-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91755-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="91755-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="91755-108">Constants</span></span>

<span data-ttu-id="91755-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**\_topología primitiva \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="91755-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="91755-110">La topología de la malla no está definida.</span><span class="sxs-lookup"><span data-stu-id="91755-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="91755-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**\_topología primitiva \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="91755-112">La topología de la malla es una lista de puntos.</span><span class="sxs-lookup"><span data-stu-id="91755-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="91755-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**\_topología primitiva \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="91755-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="91755-114">La topología de la malla es una lista de líneas.</span><span class="sxs-lookup"><span data-stu-id="91755-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="91755-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**\_topología primitiva \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="91755-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="91755-116">La topología de la malla es una franja de líneas.</span><span class="sxs-lookup"><span data-stu-id="91755-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="91755-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**\_topología primitiva \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="91755-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="91755-118">La topología de la malla es una lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="91755-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="91755-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**\_topología primitiva \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="91755-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="91755-120">La topología de la malla es una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="91755-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="91755-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**\_topología primitiva \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="91755-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="91755-122">La topología de la malla es un ventilador de triángulo.</span><span class="sxs-lookup"><span data-stu-id="91755-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="91755-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**\_LINELIST de topología \_ primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="91755-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="91755-124">La topología de la malla es una lista de líneas con adyacencias.</span><span class="sxs-lookup"><span data-stu-id="91755-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="91755-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**\_LINESTRIP de topología \_ primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="91755-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="91755-126">La topología de la malla es una franja de líneas con adyacencias.</span><span class="sxs-lookup"><span data-stu-id="91755-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="91755-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**\_TRIANGLELIST de topología \_ primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="91755-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="91755-128">La topología de la malla es una lista de triángulos con adyacencias.</span><span class="sxs-lookup"><span data-stu-id="91755-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="91755-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**\_TRIANGLESTRIP de topología \_ primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="91755-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="91755-130">La topología de la malla es una franja de triángulo con adyacencias.</span><span class="sxs-lookup"><span data-stu-id="91755-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="91755-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**Punto de control de topología de primitivo \_ \_ 1 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-132">La topología de la malla es una lista de revisiones con 1 punto de control.</span><span class="sxs-lookup"><span data-stu-id="91755-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="91755-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**\_Punto de control de topología primitiva \_ 2 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-134">La topología de la malla es una lista de revisiones con dos puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="91755-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 3 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-136">La topología de la malla es una lista de revisiones con 3 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="91755-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 4 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-138">La topología de la malla es una lista de revisiones con 4 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="91755-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 5 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-140">La topología de la malla es una lista de revisiones con 5 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="91755-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**Punto de control de topología de primitiva \_ \_ 6 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-142">La topología de la malla es una lista de revisiones con 6 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="91755-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**Punto de control de topología de primitiva \_ \_ 7 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-144">La topología de la malla es una lista de revisiones con 7 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="91755-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**\_Topología primitiva \_ 8 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-146">La topología de la malla es una lista de revisiones con 8 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="91755-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 9 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-148">La topología de la malla es una lista de revisiones con 9 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="91755-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 10 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-150">La topología de la malla es una lista de revisiones con 10 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="91755-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 11 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-152">La topología de la malla es una lista de revisiones con 11 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="91755-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**\_Topología primitiva \_ 12 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-154">La topología de la malla es una lista de revisiones con 12 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="91755-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**\_Topología primitiva \_ 13 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-156">La topología de la malla es una lista de revisiones con 13 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="91755-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**\_Topología primitiva \_ 14 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-158">La topología de la malla es una lista de revisiones con 14 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="91755-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**\_Topología primitiva \_ 15 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-160">La topología de la malla es una lista de revisiones con 15 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="91755-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**\_Topología primitiva \_ 16 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-162">La topología de la malla es una lista de revisiones con 16 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="91755-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**\_Topología primitiva \_ 17 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-164">La topología de la malla es una lista de revisiones con 17 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="91755-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**\_Topología primitiva \_ 18 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-166">La topología de la malla es una lista de revisiones con 18 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="91755-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 19 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-168">La topología de la malla es una lista de revisiones con 19 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="91755-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PATCHLIST de punto de control de topología primitiva de \_ \_ 20 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-170">La topología de la malla es una lista de revisiones con 20 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="91755-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**Punto de control de la \_ topología primitiva \_ 21 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-172">La topología de la malla es una lista de revisiones con 21 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="91755-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**Punto de control de topología de PRIMITIVOs \_ \_ 22 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-174">La topología de la malla es una lista de revisiones con 22 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="91755-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 23 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-176">La topología de la malla es una lista de revisiones con 23 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="91755-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 24 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-178">La topología de la malla es una lista de revisiones con 24 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="91755-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 25 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-180">La topología de la malla es una lista de revisiones con 25 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="91755-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 26 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-182">La topología de la malla es una lista de revisiones con 26 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="91755-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**\_Topología primitiva \_ 27 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-184">La topología de la malla es una lista de revisiones con 27 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="91755-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**\_Topología primitiva \_ 28 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-186">La topología de la malla es una lista de revisiones con 28 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="91755-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**\_Topología primitiva \_ 29 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-188">La topología de la malla es una lista de revisiones con 29 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="91755-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 30 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-190">La topología de la malla es una lista de revisiones con 30 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="91755-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**\_PATCHLIST de punto de control de topología primitiva \_ 31 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91755-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-192">La topología de la malla es una lista de revisiones con 31 puntos de control.</span><span class="sxs-lookup"><span data-stu-id="91755-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="91755-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**\_Topología primitiva \_ 32 punto de \_ control \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="91755-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="91755-194">La topología de la malla es una lista de revisiones con puntos de control de 32.</span><span class="sxs-lookup"><span data-stu-id="91755-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="91755-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91755-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="91755-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91755-196">Header</span></span></p></td><td><span data-ttu-id="91755-197">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="91755-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



