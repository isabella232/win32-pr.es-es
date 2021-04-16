---
title: CD3DX12_DESCRIPTOR_RANGE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de intervalo de descriptores de D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Estructura de CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649382"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="e104e-104">CD3DX12 \_ estructura de intervalo de descriptores \_</span><span class="sxs-lookup"><span data-stu-id="e104e-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="e104e-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ intervalo de descriptores de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="e104e-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e104e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e104e-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="e104e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e104e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e104e-108">**\_Intervalo del descriptor de CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="e104e-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="e104e-109">Crea una nueva instancia no inicializada de un \_ intervalo de descriptor D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e104e-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="e104e-110">**intervalo de \_ descriptor de CD3DX12 explícito \_ (const D3D12 \_ \_ Range &o)**</span><span class="sxs-lookup"><span data-stu-id="e104e-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e104e-111">Crea una nueva instancia de un \_ intervalo de descriptor de D3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ intervalo de descriptores de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="e104e-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e104e-112">**Intervalo de descriptor de CD3DX12 (tipo de intervalo de descriptores \_ \_ D3D12 \_ \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ desplazamiento de intervalo \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="e104e-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="e104e-113">Crea una nueva instancia de un \_ intervalo de descriptor de D3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="e104e-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="e104e-114">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="e104e-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="e104e-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="e104e-115">UINT numDescriptors</span></span>

<span data-ttu-id="e104e-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="e104e-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="e104e-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e104e-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="e104e-118">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="e104e-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="e104e-119">**Init en línea ( \_ tipo de intervalo de descriptor D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de desplazamiento de intervalo de descriptor \_ \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="e104e-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="e104e-120">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="e104e-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e104e-121">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="e104e-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="e104e-122">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="e104e-122">UINT numDescriptors</span></span>

<span data-ttu-id="e104e-123">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="e104e-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="e104e-124">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e104e-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="e104e-125">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="e104e-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="e104e-126">**Init en línea estático ( \_ intervalo de descriptor \_ de D3D12 &intervalo, \_ tipo de intervalo de descriptor D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ desplazamiento de intervalo \_ \_ anexar)**</span><span class="sxs-lookup"><span data-stu-id="e104e-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="e104e-127">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="e104e-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e104e-128">[**D3D12 \_ Rango \_ de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &intervalo</span><span class="sxs-lookup"><span data-stu-id="e104e-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="e104e-129">[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="e104e-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="e104e-130">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="e104e-130">UINT numDescriptors</span></span>

<span data-ttu-id="e104e-131">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="e104e-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="e104e-132">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="e104e-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="e104e-133">UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_</span><span class="sxs-lookup"><span data-stu-id="e104e-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e104e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e104e-134">Requirements</span></span>



| <span data-ttu-id="e104e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e104e-135">Requirement</span></span> | <span data-ttu-id="e104e-136">Value</span><span class="sxs-lookup"><span data-stu-id="e104e-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e104e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e104e-137">Header</span></span><br/> | <dl> <span data-ttu-id="e104e-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e104e-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e104e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e104e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e104e-140">**\_Intervalo de descriptor de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e104e-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="e104e-141">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e104e-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





