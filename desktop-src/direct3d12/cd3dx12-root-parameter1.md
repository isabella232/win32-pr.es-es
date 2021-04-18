---
title: CD3DX12_ROOT_PARAMETER1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura PARÁMETRO1 raíz D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Estructura de CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718488"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="6641e-104">CD3DX12 \_ raíz \_ parámetro1</span><span class="sxs-lookup"><span data-stu-id="6641e-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="6641e-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ parámetro1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="6641e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6641e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6641e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="6641e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6641e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6641e-108">**CD3DX12 \_ raíz \_ parámetro1 ()**</span><span class="sxs-lookup"><span data-stu-id="6641e-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-109">Crea una instancia nueva, no inicializada, de una \_ raíz CD3DX12 \_ parámetro1.</span><span class="sxs-lookup"><span data-stu-id="6641e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="6641e-110">**raíz CD3DX12 \_ explícita \_ parámetro1 (const D3D12 \_ raíz \_ parámetro1 &o)**</span><span class="sxs-lookup"><span data-stu-id="6641e-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-111">Crea una nueva instancia de la raíz de CD3DX12 \_ \_ parámetro1, inicializada con el contenido de otra estructura [**\_ \_ parámetro1 raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="6641e-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6641e-112">**Static inline InitAsDescriptorTable (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* pDescriptorRanges, D3D12 visibilidad \_ del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ All)**</span><span class="sxs-lookup"><span data-stu-id="6641e-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-113">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-114">[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="6641e-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="6641e-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="6641e-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="6641e-116">const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="6641e-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="6641e-117">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-118">**Static inline InitAsConstants (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-119">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-120">[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="6641e-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="6641e-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="6641e-121">UINT num32BitValues</span></span>

<span data-ttu-id="6641e-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-122">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-123">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-124">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-125">**Static inline InitAsConstantBufferView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**</span><span class="sxs-lookup"><span data-stu-id="6641e-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-126">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-127">[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="6641e-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="6641e-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-128">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-129">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-130">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-131">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-132">**Static inline InitAsShaderResourceView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**</span><span class="sxs-lookup"><span data-stu-id="6641e-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-133">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-134">[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="6641e-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="6641e-135">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-135">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-136">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-137">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-138">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-139">**Static inline InitAsUnorderedAccessView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**</span><span class="sxs-lookup"><span data-stu-id="6641e-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-140">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-141">[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="6641e-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="6641e-142">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-142">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-143">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-144">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-145">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-146">**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* pDescriptorRanges, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-147">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-148">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="6641e-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="6641e-149">const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="6641e-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="6641e-150">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-151">**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 visibilidad de \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-152">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-153">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="6641e-153">UINT num32BitValues</span></span>

<span data-ttu-id="6641e-154">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-154">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-155">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-156">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-157">**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-158">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-159">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-159">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-160">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-161">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-162">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-163">**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-164">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-165">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-165">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-166">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-167">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-168">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="6641e-169">**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="6641e-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="6641e-170">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6641e-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6641e-171">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6641e-171">UINT shaderRegister</span></span>

<span data-ttu-id="6641e-172">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6641e-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="6641e-173">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6641e-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="6641e-174">[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="6641e-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6641e-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6641e-175">Requirements</span></span>



| <span data-ttu-id="6641e-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="6641e-176">Requirement</span></span> | <span data-ttu-id="6641e-177">Value</span><span class="sxs-lookup"><span data-stu-id="6641e-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6641e-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6641e-178">Header</span></span><br/> | <dl> <span data-ttu-id="6641e-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6641e-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6641e-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="6641e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6641e-181">**D3D12 \_ raíz \_ parámetro1**</span><span class="sxs-lookup"><span data-stu-id="6641e-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="6641e-182">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="6641e-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





