---
title: D3DX11_STATE_BLOCK_MASK estructura (D3dx11effect. h)
description: Indica el estado del dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362671"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="d2341-104">\_Estructura de \_ máscara de bloque de estado D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="d2341-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="d2341-105">Indica el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2341-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2341-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2341-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="d2341-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2341-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2341-108">**VIRTUAL**</span><span class="sxs-lookup"><span data-stu-id="d2341-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-109">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-110">Valor booleano que indica si se debe guardar el estado del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-111">**VSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-112">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-113">Matriz de muestreadores de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="d2341-114">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-115">**VSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-116">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-117">Matriz de recursos del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="d2341-118">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-119">**VSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-120">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-121">Matriz de búferes de constantes de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="d2341-122">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.</span><span class="sxs-lookup"><span data-stu-id="d2341-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-123">**VSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-124">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-125">Matriz de interfaces del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="d2341-126">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-127">**!**</span><span class="sxs-lookup"><span data-stu-id="d2341-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-128">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-129">Valor booleano que indica si se debe guardar el estado del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d2341-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-130">**HSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-131">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-132">Matriz de muestreadores de sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d2341-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="d2341-133">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-134">**HSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-135">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-136">Matriz de recursos del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d2341-136">Array of hull-shader resources.</span></span> <span data-ttu-id="d2341-137">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-138">**HSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-139">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-140">Matriz de búferes de constantes de sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d2341-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="d2341-141">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.</span><span class="sxs-lookup"><span data-stu-id="d2341-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-142">**HSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-143">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-144">Matriz de interfaces de sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d2341-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="d2341-145">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-146">**DIRECTORIO**</span><span class="sxs-lookup"><span data-stu-id="d2341-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-147">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-148">Valor booleano que indica si se debe guardar el estado del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2341-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-149">**DSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-150">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-151">Matriz de muestreadores de sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2341-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="d2341-152">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-153">**DSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-154">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-155">Matriz de recursos del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2341-155">Array of domain-shader resources.</span></span> <span data-ttu-id="d2341-156">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-157">**DSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-158">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-159">Matriz de búferes de constantes de sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2341-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="d2341-160">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer.</span><span class="sxs-lookup"><span data-stu-id="d2341-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-161">**DSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-162">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-163">Matriz de interfaces de sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2341-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="d2341-164">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="d2341-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-166">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-167">Valor booleano que indica si se debe guardar el estado del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d2341-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-168">**GSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-169">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-170">Matriz de muestreadores de sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d2341-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="d2341-171">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-172">**GSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-173">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-174">Matriz de recursos del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d2341-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="d2341-175">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-176">**GSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-177">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-178">Matriz de búferes de constantes de sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d2341-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="d2341-179">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer.</span><span class="sxs-lookup"><span data-stu-id="d2341-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-180">**GSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-181">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-182">Matriz de interfaces de sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d2341-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="d2341-183">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-184">**PS**</span><span class="sxs-lookup"><span data-stu-id="d2341-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-185">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-186">Valor booleano que indica si se debe guardar el estado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-187">**PSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-188">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-189">Matriz de muestreadores de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="d2341-190">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-191">**PSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-192">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-193">Matriz de recursos del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="d2341-194">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-195">**PSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-196">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-197">Matriz de búferes de constantes de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="d2341-198">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.</span><span class="sxs-lookup"><span data-stu-id="d2341-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-199">**PSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-200">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-201">Matriz de interfaces de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="d2341-202">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-203">**PSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="d2341-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-204">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-205">Valor booleano que indica si se van a guardar las vistas de acceso desordenado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d2341-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="d2341-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-207">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-208">Valor booleano que indica si se debe guardar el estado del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d2341-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-209">**CSSamplers**</span><span class="sxs-lookup"><span data-stu-id="d2341-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-210">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-211">Matriz de muestreadores de sombreador de proceso.</span><span class="sxs-lookup"><span data-stu-id="d2341-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="d2341-212">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de muestra.</span><span class="sxs-lookup"><span data-stu-id="d2341-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-213">**CSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="d2341-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-214">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-215">Matriz de recursos del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d2341-215">Array of compute-shader resources.</span></span> <span data-ttu-id="d2341-216">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-217">**CSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-218">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-219">Matriz de búferes de constantes de sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d2341-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="d2341-220">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de búfer constante.</span><span class="sxs-lookup"><span data-stu-id="d2341-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-221">**CSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d2341-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-222">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-223">Matriz de interfaces de sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d2341-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="d2341-224">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2341-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-225">**CSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="d2341-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-226">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-227">Valor booleano que indica si se van a guardar las vistas de acceso desordenado del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d2341-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-228">**IAVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-229">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-230">Matriz de búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="d2341-230">Array of vertex buffers.</span></span> <span data-ttu-id="d2341-231">La matriz es una máscara de bits de varios bytes donde cada bit representa una ranura de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2341-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-232">**IAIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="d2341-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-233">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-234">Valor booleano que indica si se debe guardar el estado del búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="d2341-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-235">**IAInputLayout**</span><span class="sxs-lookup"><span data-stu-id="d2341-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-236">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-237">Valor booleano que indica si se va a guardar el estado de diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="d2341-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-238">**IAPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="d2341-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-239">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-240">Valor booleano que indica si se va a guardar el estado de la topología primitiva.</span><span class="sxs-lookup"><span data-stu-id="d2341-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-241">**OMRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="d2341-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-242">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-243">Valor booleano que indica si se deben guardar los Estados de destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="d2341-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-244">**OMDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="d2341-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-245">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-246">Valor booleano que indica si se va a guardar el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="d2341-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-247">**OMBlendState**</span><span class="sxs-lookup"><span data-stu-id="d2341-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-248">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-249">Valor booleano que indica si se va a guardar el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="d2341-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-250">**RSViewports**</span><span class="sxs-lookup"><span data-stu-id="d2341-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-251">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-252">Valor booleano que indica si se van a guardar los Estados de las ventanillas.</span><span class="sxs-lookup"><span data-stu-id="d2341-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-253">**RSScissorRects**</span><span class="sxs-lookup"><span data-stu-id="d2341-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-254">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-255">Valor booleano que indica si se deben guardar los Estados de rectángulos en tijera.</span><span class="sxs-lookup"><span data-stu-id="d2341-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-256">**RSRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="d2341-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-257">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-258">Valor booleano que indica si se debe guardar el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d2341-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-259">**SOBuffers**</span><span class="sxs-lookup"><span data-stu-id="d2341-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-260">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-261">Valor booleano que indica si se van a guardar los Estados de los búferes de flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="d2341-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="d2341-262">**Predicación**</span><span class="sxs-lookup"><span data-stu-id="d2341-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="d2341-263">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2341-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d2341-264">Valor booleano que indica si se va a guardar el estado de predication.</span><span class="sxs-lookup"><span data-stu-id="d2341-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2341-265">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2341-265">Remarks</span></span>

<span data-ttu-id="d2341-266">Una máscara de bloque de estado indica el dispositivo que cambia un paso o una técnica.</span><span class="sxs-lookup"><span data-stu-id="d2341-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2341-267">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2341-267">Requirements</span></span>



| <span data-ttu-id="d2341-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2341-268">Requirement</span></span> | <span data-ttu-id="d2341-269">Value</span><span class="sxs-lookup"><span data-stu-id="d2341-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2341-270">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2341-270">Header</span></span><br/> | <dl> <span data-ttu-id="d2341-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2341-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2341-272">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2341-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2341-273">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="d2341-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

