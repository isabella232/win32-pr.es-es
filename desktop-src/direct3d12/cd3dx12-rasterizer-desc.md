---
title: CD3DX12_RASTERIZER_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC de rasterizador D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Estructura de CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717610"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="6ccce-104">CD3DX12 ( \_ estructura de Descripción del rasterizador) \_</span><span class="sxs-lookup"><span data-stu-id="6ccce-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="6ccce-105">Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESC de rasterizador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="6ccce-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccce-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ccce-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="6ccce-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ccce-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ccce-108">**CD3DX12 \_ rasterizador \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6ccce-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-109">Crea una nueva instancia no inicializada de una \_ Descripción de rasterizador CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6ccce-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6ccce-110">**CD3DX12 de \_ rasterizador explícito \_ (const D3D12 de \_ rasterización de la \_&)**</span><span class="sxs-lookup"><span data-stu-id="6ccce-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-111">Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , que se inicializa con el contenido de otra estructura de [**\_ \_ DESC del rasterizador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="6ccce-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ccce-112">**CD3DX12 de \_ rasterizador explícito \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="6ccce-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-113">Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , inicializada con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="6ccce-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="6ccce-114">**CD3DX12 de \_ rasterización Explicit \_ ( \_ \_ modo de relleno D3D12 fillMode, \_ D3D12 \_ modo de reselección CullMode, bool FrontCounterClockwise, int DepthBias, Float DepthBiasClamp, Float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 el \_ modo de \_ rasterización conservador \_ conservativeRaster)**</span><span class="sxs-lookup"><span data-stu-id="6ccce-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-115">Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="6ccce-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="6ccce-116">[**D3D12 \_ \_Modo de relleno**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span><span class="sxs-lookup"><span data-stu-id="6ccce-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="6ccce-117">[**D3D12 \_ \_Modo de selección**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span><span class="sxs-lookup"><span data-stu-id="6ccce-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="6ccce-118">BOOL frontCounterClockwise</span><span class="sxs-lookup"><span data-stu-id="6ccce-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="6ccce-119">INT depthBias</span><span class="sxs-lookup"><span data-stu-id="6ccce-119">INT depthBias</span></span>

<span data-ttu-id="6ccce-120">FLOAT depthBiasClamp</span><span class="sxs-lookup"><span data-stu-id="6ccce-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="6ccce-121">FLOAT slopeScaledDepthBias</span><span class="sxs-lookup"><span data-stu-id="6ccce-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="6ccce-122">BOOL depthClipEnable</span><span class="sxs-lookup"><span data-stu-id="6ccce-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="6ccce-123">BOOL multisampleEnable</span><span class="sxs-lookup"><span data-stu-id="6ccce-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="6ccce-124">BOOL antialiasedLineEnable</span><span class="sxs-lookup"><span data-stu-id="6ccce-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="6ccce-125">UINT forcedSampleCount</span><span class="sxs-lookup"><span data-stu-id="6ccce-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="6ccce-126">[**D3D12 \_ \_ \_ Modo de rasterización conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span><span class="sxs-lookup"><span data-stu-id="6ccce-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="6ccce-127">**~ CD3DX12 \_ rasterizador \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="6ccce-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-128">Destruye una instancia de una descripción de CD3DX12 de \_ rasterizador \_ .</span><span class="sxs-lookup"><span data-stu-id="6ccce-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6ccce-129">**Operator const D3D12 \_ rasterizador \_ DESC& () Const**</span><span class="sxs-lookup"><span data-stu-id="6ccce-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6ccce-130">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="6ccce-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ccce-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccce-131">Requirements</span></span>



| <span data-ttu-id="6ccce-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccce-132">Requirement</span></span> | <span data-ttu-id="6ccce-133">Value</span><span class="sxs-lookup"><span data-stu-id="6ccce-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccce-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ccce-134">Header</span></span><br/> | <dl> <span data-ttu-id="6ccce-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccce-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ccce-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ccce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccce-137">**Descripción de D3D12 \_ rasterizador \_**</span><span class="sxs-lookup"><span data-stu-id="6ccce-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="6ccce-138">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="6ccce-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





