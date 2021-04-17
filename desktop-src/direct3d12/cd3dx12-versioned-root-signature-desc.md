---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de \_ DESC de la firma raíz de D3D12 \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Estructura de CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717590"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="65229-104">CD3DX12 \_ estructura de \_ \_ DESC de firma raíz con versión \_</span><span class="sxs-lookup"><span data-stu-id="65229-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="65229-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de DESC de la [**\_ \_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="65229-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65229-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65229-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="65229-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="65229-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="65229-108">**CD3DX12 de \_ firma raíz con control de versiones \_ \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="65229-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="65229-109">Crea una instancia nueva, no inicializada, de una descripción de la \_ firma raíz con versión CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="65229-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="65229-110">**CD3DX12 de \_ firma raíz de versión explícita de la \_ firma de raíz \_ \_ (const D3D12 con \_ versión de \_ firma raíz con \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="65229-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-111">Crea una nueva instancia de una \_ Descripción de la \_ firma raíz con versión CD3DX12 \_ \_ , inicializada con el contenido de una estructura de DESC de la [**\_ \_ \_ firma \_ raíz con versión D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="65229-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65229-112">**Descripción de la firma raíz de CD3DX12 explícita con \_ versión \_ \_ \_ (const D3D12 raíz de la \_ \_ &firma raíz \_ )**</span><span class="sxs-lookup"><span data-stu-id="65229-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-113">Crea una nueva instancia de una \_ Descripción de la \_ firma raíz con versión CD3DX12 \_ \_ , inicializada con el contenido de una estructura de DESC de la [**\_ \_ firma \_ raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="65229-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65229-114">**CD3DX12 de \_ firma raíz explícita con versión de \_ \_ \_ (const D3D12 \_ raíz \_ signatura \_ DESC1 &)**</span><span class="sxs-lookup"><span data-stu-id="65229-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-115">Crea una nueva instancia de una CD3DX12 de \_ \_ firma raíz con control de versiones \_ \_ , inicializada con el contenido de una estructura DESC1 de la [**\_ \_ firma \_ raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .</span><span class="sxs-lookup"><span data-stu-id="65229-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65229-116">**CD3DX12 \_ \_ de firma raíz con control \_ de versiones \_ (uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-117">Crea una nueva instancia de una \_ \_ Descripción de la firma raíz CD3DX12 con versión \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="65229-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="65229-118">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-118">UINT numParameters</span></span>

<span data-ttu-id="65229-119">[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="65229-120">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-121">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-122">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-123">**CD3DX12 \_ \_ de firma raíz con control \_ de versiones \_ (uint numParameters, const D3D12 \_ raíz \_ parámetro1 \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-124">Crea una nueva instancia de una \_ \_ Descripción de la firma raíz CD3DX12 con versión \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="65229-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="65229-125">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-125">UINT numParameters</span></span>

<span data-ttu-id="65229-126">const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="65229-127">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-128">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-129">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-130">**CD3DX12 de \_ firma raíz con versiones de \_ \_ \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="65229-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-131">Crea una nueva instancia de una \_ \_ Descripción de la firma raíz con versión CD3DX12 \_ \_ , inicializada con los parámetros predeterminados:</span><span class="sxs-lookup"><span data-stu-id="65229-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="65229-132">UINT numParameters = 0</span><span class="sxs-lookup"><span data-stu-id="65229-132">UINT numParameters = 0</span></span>

<span data-ttu-id="65229-133">const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null</span><span class="sxs-lookup"><span data-stu-id="65229-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="65229-134">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-135">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-136">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-137">**Inicialización en línea \_ 1 \_ 0 (uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 marca de \_ firma raíz \_ \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-138">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="65229-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65229-139">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-139">UINT numParameters</span></span>

<span data-ttu-id="65229-140">[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="65229-141">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-142">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-143">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-144">**Static inline init \_ 1 \_ 0 (D3D12 con \_ versiones \_ \_ de la firma raíz \_ DESC &DESC, uint numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de firma raíz \_ \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-145">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="65229-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65229-146">[**D3D12 \_ Descripción de \_ la \_ firma \_ raíz con versión**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="65229-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="65229-147">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-147">UINT numParameters</span></span>

<span data-ttu-id="65229-148">[**\_ \_ parámetro raíz const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="65229-149">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-150">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-151">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-152">**Inicialización en línea \_ 1 \_ (uint numParameters, const D3D12 \_ raíz \_ Parámetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de firma raíz \_ \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-153">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="65229-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65229-154">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-154">UINT numParameters</span></span>

<span data-ttu-id="65229-155">const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="65229-156">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-157">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-158">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="65229-159">**Inicial de inline init \_ 1 \_ 1 (D3D12 de \_ firma raíz con versiones de \_ \_ \_ &DESC, uint numParameters, const D3D12 \_ raíz \_ parámetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ marca de \_ firma raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="65229-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="65229-160">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="65229-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="65229-161">[**D3D12 \_ Descripción de \_ la \_ firma \_ raíz con versión**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="65229-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="65229-162">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="65229-162">UINT numParameters</span></span>

<span data-ttu-id="65229-163">const [**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="65229-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="65229-164">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="65229-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="65229-165">const [**D3D12 \_ static \_ Sample \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="65229-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="65229-166">[**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="65229-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65229-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65229-167">Requirements</span></span>



| <span data-ttu-id="65229-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="65229-168">Requirement</span></span> | <span data-ttu-id="65229-169">Value</span><span class="sxs-lookup"><span data-stu-id="65229-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65229-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65229-170">Header</span></span><br/> | <dl> <span data-ttu-id="65229-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="65229-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65229-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="65229-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65229-173">**\_Descripción de la \_ \_ firma raíz \_ de D3D12 con versiones**</span><span class="sxs-lookup"><span data-stu-id="65229-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="65229-174">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="65229-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





