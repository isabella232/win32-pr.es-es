---
title: CD3DX12_DESCRIPTOR_RANGE1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura RANGE1 del descriptor de D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Estructura de CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649381"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="297f5-104">CD3DX12 \_ descriptor \_ RANGE1 (estructura)</span><span class="sxs-lookup"><span data-stu-id="297f5-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="297f5-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ RANGE1 del descriptor de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="297f5-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="297f5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="297f5-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="297f5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="297f5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="297f5-108">**\_Descriptor CD3DX12 \_ RANGE1 ()**</span><span class="sxs-lookup"><span data-stu-id="297f5-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="297f5-109">Crea una nueva instancia no inicializada de un \_ descriptor CD3DX12 \_ RANGE1.</span><span class="sxs-lookup"><span data-stu-id="297f5-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="297f5-110">**descriptor de CD3DX12 explícito \_ \_ range1 (const D3D12 \_ descriptor \_ range1 &o)**</span><span class="sxs-lookup"><span data-stu-id="297f5-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="297f5-111">Crea una nueva instancia de un \_ descriptor de CD3DX12 \_ range1, inicializada con el contenido de otra estructura del [**\_ descriptor de D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="297f5-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="297f5-112">**Descriptor de CD3DX12 \_ \_ RANGE1 ( \_ tipo de intervalo de descriptores D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descriptores de intervalo Flags \_ \_ = D3D12 \_ marcador de intervalo de descriptor \_ \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de \_ desplazamiento de intervalo \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="297f5-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="297f5-113">Crea una nueva instancia de un \_ descriptor de CD3DX12 \_ RANGE1, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="297f5-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="297f5-114">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="297f5-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="297f5-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="297f5-115">UINT numDescriptors</span></span>

<span data-ttu-id="297f5-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="297f5-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="297f5-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="297f5-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="297f5-118">[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="297f5-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="297f5-119">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="297f5-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="297f5-120">**Init en línea ( \_ tipo de intervalo de descriptores \_ de D3D12 \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ descriptores de intervalo Flags \_ \_ = D3D12 \_ \_ marcador de intervalo de DEscriptor \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de \_ desplazamiento de intervalo \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="297f5-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="297f5-121">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="297f5-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="297f5-122">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="297f5-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="297f5-123">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="297f5-123">UINT numDescriptors</span></span>

<span data-ttu-id="297f5-124">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="297f5-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="297f5-125">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="297f5-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="297f5-126">[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="297f5-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="297f5-127">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="297f5-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="297f5-128">**Inicialización en línea estática ( \_ descriptor \_ de D3D12 RANGE1 &intervalo, \_ tipo de intervalo de descriptor de D3D12 de \_ \_ texto RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 descriptores de intervalo de descriptores \_ \_ \_ = D3D12 \_ marcador de intervalo de descriptor \_ \_ \_ ninguno, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ \_ desplazamiento \_ anexar)**</span><span class="sxs-lookup"><span data-stu-id="297f5-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="297f5-129">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="297f5-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="297f5-130">[**D3D12 \_ Descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &intervalo</span><span class="sxs-lookup"><span data-stu-id="297f5-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="297f5-131">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="297f5-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="297f5-132">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="297f5-132">UINT numDescriptors</span></span>

<span data-ttu-id="297f5-133">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="297f5-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="297f5-134">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="297f5-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="297f5-135">[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="297f5-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="297f5-136">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="297f5-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="297f5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="297f5-137">Requirements</span></span>



| <span data-ttu-id="297f5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="297f5-138">Requirement</span></span> | <span data-ttu-id="297f5-139">Value</span><span class="sxs-lookup"><span data-stu-id="297f5-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="297f5-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="297f5-140">Header</span></span><br/> | <dl> <span data-ttu-id="297f5-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="297f5-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297f5-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="297f5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297f5-143">**\_Descriptor D3D12 \_ RANGE1**</span><span class="sxs-lookup"><span data-stu-id="297f5-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="297f5-144">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="297f5-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





