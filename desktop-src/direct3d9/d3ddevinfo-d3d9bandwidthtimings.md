---
description: Métricas de rendimiento para ayudarle a comprender el rendimiento de una aplicación.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280279"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="91f91-103">D3DDEVINFO \_ estructura D3D9BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="91f91-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="91f91-104">Métricas de rendimiento para ayudarle a comprender el rendimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="91f91-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91f91-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="91f91-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="91f91-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="91f91-107">**MaxBandwidthUtilized**</span><span class="sxs-lookup"><span data-stu-id="91f91-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="91f91-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91f91-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="91f91-109">El ancho de banda o la velocidad de transferencia de datos máxima de la CPU del host a la GPU.</span><span class="sxs-lookup"><span data-stu-id="91f91-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="91f91-110">Suele ser el ancho de banda del bus PCI o AGP que conecta la CPU y la GPU.</span><span class="sxs-lookup"><span data-stu-id="91f91-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="91f91-111">**FrontEndUploadMemoryUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="91f91-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="91f91-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91f91-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="91f91-113">Porcentaje de uso de memoria al cargar datos desde la CPU del host a la GPU.</span><span class="sxs-lookup"><span data-stu-id="91f91-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="91f91-114">**VertexRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="91f91-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="91f91-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91f91-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="91f91-116">Porcentaje de rendimiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="91f91-116">Vertex throughput percentage.</span></span> <span data-ttu-id="91f91-117">Es el número de vértices procesados en comparación con la velocidad máxima de procesamiento de vértices teóricos.</span><span class="sxs-lookup"><span data-stu-id="91f91-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="91f91-118">**TriangleSetupRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="91f91-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="91f91-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91f91-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="91f91-120">Porcentaje de rendimiento de configuración de triángulo.</span><span class="sxs-lookup"><span data-stu-id="91f91-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="91f91-121">Es el número de triángulos que se configuran para la rasterización en comparación con la tasa de configuración del triángulo máximo teórico.</span><span class="sxs-lookup"><span data-stu-id="91f91-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="91f91-122">**FillRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="91f91-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="91f91-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91f91-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="91f91-124">Porcentaje de rendimiento de relleno de píxeles.</span><span class="sxs-lookup"><span data-stu-id="91f91-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="91f91-125">Es el número de píxeles que se rellenan en comparación con el relleno de píxeles teórico.</span><span class="sxs-lookup"><span data-stu-id="91f91-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91f91-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91f91-126">Requirements</span></span>



| <span data-ttu-id="91f91-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="91f91-127">Requirement</span></span> | <span data-ttu-id="91f91-128">Value</span><span class="sxs-lookup"><span data-stu-id="91f91-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91f91-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91f91-129">Header</span></span><br/> | <dl> <span data-ttu-id="91f91-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f91-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f91-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="91f91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f91-132">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="91f91-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="91f91-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="91f91-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
