---
title: CD3DX12_RESOURCE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de DESC de recursos D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Estructura de CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718495"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="40fd6-104">CD3DX12 \_ estructura de DESC de recursos \_</span><span class="sxs-lookup"><span data-stu-id="40fd6-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="40fd6-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ DESC de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="40fd6-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fd6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40fd6-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="40fd6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="40fd6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="40fd6-108">**\_ \_ Descripción del recurso CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="40fd6-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-109">Crea una nueva instancia no inicializada de una \_ Descripción de recurso CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="40fd6-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-110">**\_Descripción del recurso CD3DX12 explícito \_ (const \_ D3D12 \_& desc.**</span><span class="sxs-lookup"><span data-stu-id="40fd6-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-111">Crea una nueva instancia de una \_ Descripción de recurso CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ DESC de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="40fd6-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-112">**\_Descripción del recurso CD3DX12 \_ ( \_ \_ dimensión de dimensión de recursos D3D12, alineación UInt64, ancho UInt64, uint alto, Uint16 depthOrArraySize, UInt16 mipLevels, \_ formato de formato de DXGI, uint sampleCount, uint sampleQuality, \_ \_ diseño de diseño de textura de D3D12, marcas de marcas de recursos de D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="40fd6-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-113">Crea una nueva instancia de una \_ Descripción de recurso CD3DX12 \_ , inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="40fd6-114">[**D3D12 \_ Dimensión de \_ dimensión de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="40fd6-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="40fd6-115">Alineación UINT64</span><span class="sxs-lookup"><span data-stu-id="40fd6-115">UINT64 alignment</span></span>

<span data-ttu-id="40fd6-116">UINT64 (ancho)</span><span class="sxs-lookup"><span data-stu-id="40fd6-116">UINT64 width</span></span>

<span data-ttu-id="40fd6-117">Alto de UINT</span><span class="sxs-lookup"><span data-stu-id="40fd6-117">UINT height</span></span>

<span data-ttu-id="40fd6-118">UINT16 depthOrArraySize</span><span class="sxs-lookup"><span data-stu-id="40fd6-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="40fd6-119">UINT16 mipLevels</span><span class="sxs-lookup"><span data-stu-id="40fd6-119">UINT16 mipLevels</span></span>

<span data-ttu-id="40fd6-120">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="40fd6-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="40fd6-121">UINT sampleCount</span><span class="sxs-lookup"><span data-stu-id="40fd6-121">UINT sampleCount</span></span>

<span data-ttu-id="40fd6-122">UINT sampleQuality</span><span class="sxs-lookup"><span data-stu-id="40fd6-122">UINT sampleQuality</span></span>

<span data-ttu-id="40fd6-123">[**D3D12 \_ Diseño \_ de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)</span><span class="sxs-lookup"><span data-stu-id="40fd6-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="40fd6-124">[**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)</span><span class="sxs-lookup"><span data-stu-id="40fd6-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-125">**Búfer alineado estático ( \_ \_ \_ información de asignación de recursos de const D3D12& resAllocInfo, D3D12 marcas de \_ recursos marcadores \_ = D3D12 \_ marca de recurso \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-126">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="40fd6-127">[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="40fd6-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="40fd6-128">rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="40fd6-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-129">**Búfer alineado estático (UINT64 width, D3D12 \_ Resource \_ Flag Flags = \_ D3D12 \_ marcador \_ de recurso None, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-130">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="40fd6-131">UINT64 (ancho)</span><span class="sxs-lookup"><span data-stu-id="40fd6-131">UINT64 width</span></span>

<span data-ttu-id="40fd6-132">rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="40fd6-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="40fd6-133">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-134">**Static inline Tex1D ( \_ formato de formato de DXGI, UINT64 width, Uint16 tamaño = 1, Uint16 mipLevels = 0, D3D12 Flag Flag \_ \_ Flags = D3D12 \_ \_ marcador \_ de recurso None, D3D12 \_ diseño de textura \_ layout = D3D12 \_ diseño de textura \_ \_ desconocido, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-135">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="40fd6-136">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="40fd6-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="40fd6-137">UINT64 (ancho)</span><span class="sxs-lookup"><span data-stu-id="40fd6-137">UINT64 width</span></span>

<span data-ttu-id="40fd6-138">rechace UINT16 tamaño = 1</span><span class="sxs-lookup"><span data-stu-id="40fd6-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="40fd6-139">rechace UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="40fd6-140">rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="40fd6-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="40fd6-141">rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="40fd6-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="40fd6-142">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-143">**Static inline Tex2D ( \_ formato de formato de DXGI, UINT64 width, uint height, Uint16 tamaño = 1, Uint16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 marcadores de \_ recursos \_ Flags = D3D12 \_ \_ marcador \_ de recurso None, D3D12 diseño de textura de la textura \_ \_ = D3D12 \_ \_ diseño de textura \_ desconocido, UINT64 Alignment = 0)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-144">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="40fd6-145">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="40fd6-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="40fd6-146">UINT64 (ancho)</span><span class="sxs-lookup"><span data-stu-id="40fd6-146">UINT64 width</span></span>

<span data-ttu-id="40fd6-147">Alto de UINT</span><span class="sxs-lookup"><span data-stu-id="40fd6-147">UINT height</span></span>

<span data-ttu-id="40fd6-148">rechace UINT16 tamaño = 1</span><span class="sxs-lookup"><span data-stu-id="40fd6-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="40fd6-149">rechace UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="40fd6-150">rechace UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="40fd6-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="40fd6-151">rechace UINT sampleQuality = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="40fd6-152">rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="40fd6-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="40fd6-153">rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="40fd6-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="40fd6-154">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-155">**Static inline Tex3D ( \_ formato de formato de DXGI, UINT64 width, uint height, UInt16 Depth, UINT16 mipLevels = 0, D3D12 \_ indicadores de marcadores de recursos \_ = D3D12 \_ \_ marca de recurso \_ None, D3D12 diseño de \_ textura \_ layout = D3D12 \_ diseño de textura \_ \_ desconocido, alineación UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-156">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="40fd6-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="40fd6-157">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="40fd6-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="40fd6-158">UINT64 (ancho)</span><span class="sxs-lookup"><span data-stu-id="40fd6-158">UINT64 width</span></span>

<span data-ttu-id="40fd6-159">Alto de UINT</span><span class="sxs-lookup"><span data-stu-id="40fd6-159">UINT height</span></span>

<span data-ttu-id="40fd6-160">Profundidad UINT16</span><span class="sxs-lookup"><span data-stu-id="40fd6-160">UINT16 depth</span></span>

<span data-ttu-id="40fd6-161">rechace UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="40fd6-162">rechace [**D3D12 \_ Marcas de \_ marcadores de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = marca de recurso D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="40fd6-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="40fd6-163">rechace [**D3D12 \_ Distribución de \_ diseño de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = Diseño de textura D3D12 \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="40fd6-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="40fd6-164">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="40fd6-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-165">**Profundidad en línea () Const**</span><span class="sxs-lookup"><span data-stu-id="40fd6-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-166">Si Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, devuelve DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="40fd6-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="40fd6-167">Si Dimension! = D3D12 \_ \_ de la dimensión \_ de recursos TEXTURE3D, devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="40fd6-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-168">**Inline tamaño () Const**</span><span class="sxs-lookup"><span data-stu-id="40fd6-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-169">Si Dimension! = D3D12 \_ \_ de la dimensión \_ de recursos TEXTURE3D, devuelve DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="40fd6-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="40fd6-170">Si Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="40fd6-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="40fd6-171">Consulte [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="40fd6-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-172">**Inline PlaneCount (ID3D12Device \* pDevice) Const**</span><span class="sxs-lookup"><span data-stu-id="40fd6-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-173">Devuelve D3D12GetFormatPlaneCount (pDevice, Format).</span><span class="sxs-lookup"><span data-stu-id="40fd6-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="40fd6-174">Vea [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) y [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="40fd6-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-175">**Subrecursos insertados (ID3D12Device \* pDevice) Const**</span><span class="sxs-lookup"><span data-stu-id="40fd6-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-176">Devuelve el número de Subrecursos, calculado como MipLevels \* tamaño () \* PlaneCount (pDevice).</span><span class="sxs-lookup"><span data-stu-id="40fd6-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-177">**Inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-178">Calcula un índice de Subrecursos mediante [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span><span class="sxs-lookup"><span data-stu-id="40fd6-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-179">**Operator const D3D12 \_ \_ DESC& () Const**</span><span class="sxs-lookup"><span data-stu-id="40fd6-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-180">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="40fd6-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-181">**operador = = (const D3D12 \_ \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-182">Devuelve true si todos los miembros de cada estructura son idénticos.</span><span class="sxs-lookup"><span data-stu-id="40fd6-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="40fd6-183">**Operator! = (const D3D12 \_ Resource \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**</span><span class="sxs-lookup"><span data-stu-id="40fd6-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="40fd6-184">Devuelve false si todos los miembros de cada estructura son idénticos.</span><span class="sxs-lookup"><span data-stu-id="40fd6-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40fd6-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40fd6-185">Requirements</span></span>



| <span data-ttu-id="40fd6-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="40fd6-186">Requirement</span></span> | <span data-ttu-id="40fd6-187">Value</span><span class="sxs-lookup"><span data-stu-id="40fd6-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40fd6-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40fd6-188">Header</span></span><br/> | <dl> <span data-ttu-id="40fd6-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="40fd6-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40fd6-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="40fd6-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fd6-191">**\_Descripción del recurso D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="40fd6-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="40fd6-192">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="40fd6-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

