---
title: CD3DX12_ROOT_SIGNATURE_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de DESC de la firma raíz de D3D12 \_ \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Estructura de CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718487"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="e6c80-104">CD3DX12 \_ \_ \_ estructura DESC de la firma raíz</span><span class="sxs-lookup"><span data-stu-id="e6c80-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="e6c80-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de DESC de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="e6c80-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c80-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6c80-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="e6c80-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6c80-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6c80-108">**CD3DX12 \_ raíz de la \_ firma raíz \_ ()**</span><span class="sxs-lookup"><span data-stu-id="e6c80-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-109">Crea una nueva instancia no inicializada de una descripción de la \_ firma raíz CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e6c80-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="e6c80-110">**firma de raíz de CD3DX12 explícita \_ \_ \_ DESC (const D3D12 raíz de la \_ \_ firma raíz \_ &)**</span><span class="sxs-lookup"><span data-stu-id="e6c80-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-111">Crea una nueva instancia de una descripción de la \_ firma raíz de CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de DESC de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="e6c80-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6c80-112">**CD3DX12 \_ root \_ Signature \_ DESC (uint NUMPARAMETERS, const D3D12 \_ raíz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ PSTATICSAMPLERS = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature Flag \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="e6c80-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-113">Crea una nueva instancia de una \_ Descripción de \_ la firma raíz de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="e6c80-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="e6c80-114">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-114">UINT numParameters</span></span>

<span data-ttu-id="e6c80-115">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="e6c80-116">rechace UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="e6c80-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="e6c80-117">rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="e6c80-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="e6c80-118">rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="e6c80-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="e6c80-119">**CD3DX12 \_ raíz de la \_ firma raíz \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="e6c80-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-120">Crea una nueva instancia de una descripción de la \_ firma raíz de CD3DX12 \_ \_ , inicializada con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="e6c80-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="e6c80-121">**Init en línea (UINT numParameters, const D3D12 \_ raíz \_ parámetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ pStaticSamplers = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ \_ marca de firma raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="e6c80-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-122">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6c80-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e6c80-123">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-123">UINT numParameters</span></span>

<span data-ttu-id="e6c80-124">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="e6c80-125">rechace UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="e6c80-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="e6c80-126">rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="e6c80-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="e6c80-127">rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="e6c80-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="e6c80-128">**Static inline init (D3D12 \_ root \_ SIGNATURE \_ DESC &DESC, uint NUMPARAMETERS, const D3D12 \_ raíz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ DESC \* \_ PSTATICSAMPLERS = null, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ \_ Flag no)**</span><span class="sxs-lookup"><span data-stu-id="e6c80-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="e6c80-129">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6c80-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="e6c80-130">[**D3D12 \_ &de la \_ firma raíz \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)</span><span class="sxs-lookup"><span data-stu-id="e6c80-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="e6c80-131">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-131">UINT numParameters</span></span>

<span data-ttu-id="e6c80-132">[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="e6c80-133">rechace UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="e6c80-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="e6c80-134">rechace [**D3D12 \_ \_Muestra estática \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="e6c80-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="e6c80-135">rechace [**D3D12 \_ Marcas \_ de \_ firma raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) marcas = \_ D3D12 \_ marca de firma raíz \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="e6c80-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6c80-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6c80-136">Requirements</span></span>



| <span data-ttu-id="e6c80-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c80-137">Requirement</span></span> | <span data-ttu-id="e6c80-138">Value</span><span class="sxs-lookup"><span data-stu-id="e6c80-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c80-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6c80-139">Header</span></span><br/> | <dl> <span data-ttu-id="e6c80-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c80-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c80-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6c80-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c80-142">**Descripción de la \_ firma raíz de D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6c80-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="e6c80-143">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e6c80-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





