---
title: CD3DX12_ROOT_PARAMETER estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de parámetros raíz D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Estructura de CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717598"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="def1b-104">\_Estructura del \_ parámetro raíz CD3DX12</span><span class="sxs-lookup"><span data-stu-id="def1b-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="def1b-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ parámetros raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="def1b-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="def1b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="def1b-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="def1b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="def1b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="def1b-108">**\_Parámetro raíz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="def1b-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-109">Crea una nueva instancia no inicializada de un \_ parámetro raíz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="def1b-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="def1b-110">**\_parámetro raíz CD3DX12 explícito \_ ( \_ parámetro raíz const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="def1b-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-111">Crea una nueva instancia de un \_ parámetro raíz CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ parámetros raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="def1b-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="def1b-112">**Static inline InitAsDescriptorTable ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* pDescriptorRanges, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-113">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-114">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="def1b-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="def1b-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="def1b-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="def1b-116">[**D3D12 \_ \_Rango de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="def1b-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="def1b-117">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-118">**Static inline InitAsConstants ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-119">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-120">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="def1b-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="def1b-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="def1b-121">UINT num32BitValues</span></span>

<span data-ttu-id="def1b-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-122">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-123">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-124">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-125">**Static inline InitAsConstantBufferView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-126">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-127">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="def1b-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="def1b-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-128">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-129">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-130">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-131">**Static inline InitAsShaderResourceView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-132">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-133">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="def1b-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="def1b-134">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-134">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-135">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-136">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-137">**Static inline InitAsUnorderedAccessView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-138">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-139">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="def1b-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="def1b-140">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-140">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-141">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-142">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-143">**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* pDescriptorRanges, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-144">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-145">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="def1b-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="def1b-146">[**D3D12 \_ \_Rango de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="def1b-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="def1b-147">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-148">**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 visibilidad de \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="def1b-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-149">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-150">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="def1b-150">UINT num32BitValues</span></span>

<span data-ttu-id="def1b-151">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-151">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-152">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-153">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-154">**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**</span><span class="sxs-lookup"><span data-stu-id="def1b-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-155">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-156">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-156">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-157">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-158">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-159">**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**</span><span class="sxs-lookup"><span data-stu-id="def1b-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-160">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-161">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-161">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-162">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-163">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="def1b-164">**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**</span><span class="sxs-lookup"><span data-stu-id="def1b-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="def1b-165">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="def1b-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="def1b-166">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="def1b-166">UINT shaderRegister</span></span>

<span data-ttu-id="def1b-167">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="def1b-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="def1b-168">rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="def1b-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="def1b-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def1b-169">Requirements</span></span>



| <span data-ttu-id="def1b-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="def1b-170">Requirement</span></span> | <span data-ttu-id="def1b-171">Value</span><span class="sxs-lookup"><span data-stu-id="def1b-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="def1b-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="def1b-172">Header</span></span><br/> | <dl> <span data-ttu-id="def1b-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="def1b-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def1b-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="def1b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def1b-175">**\_Parámetro raíz \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="def1b-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="def1b-176">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="def1b-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





