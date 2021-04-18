---
title: CD3DX12_BLEND_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC de D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Estructura de CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707777"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="8a111-104">CD3DX12 \_ Blend ( \_ estructura de DESC)</span><span class="sxs-lookup"><span data-stu-id="8a111-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="8a111-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESC de D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="8a111-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a111-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a111-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="8a111-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a111-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a111-108">**CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="8a111-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="8a111-109">Crea una nueva instancia no inicializada de una descripción de CD3DX12 \_ Blend \_ .</span><span class="sxs-lookup"><span data-stu-id="8a111-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="8a111-110">**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="8a111-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="8a111-111">Crea una nueva instancia de una descripción de CD3DX12 \_ Blend \_ , inicializada con el contenido de otra estructura [**\_ \_ DESC de D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="8a111-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a111-112">**CD3DX12 \_ Blend Explicit \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="8a111-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="8a111-113">Crea una nueva instancia de una descripción de CD3DX12 \_ Blend \_ , inicializada con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="8a111-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="8a111-114">Estado</span><span class="sxs-lookup"><span data-stu-id="8a111-114">State</span></span>                                   | <span data-ttu-id="8a111-115">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8a111-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="8a111-116">AlphaToCoverageEnable</span><span class="sxs-lookup"><span data-stu-id="8a111-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="8a111-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8a111-117">**FALSE**</span></span>                        |
| <span data-ttu-id="8a111-118">IndependentBlendEnable</span><span class="sxs-lookup"><span data-stu-id="8a111-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="8a111-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8a111-119">**FALSE**</span></span>                        |
| <span data-ttu-id="8a111-120">RenderTarget \[ 0 \] . BlendEnable</span><span class="sxs-lookup"><span data-stu-id="8a111-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="8a111-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8a111-121">**FALSE**</span></span>                        |
| <span data-ttu-id="8a111-122">RenderTarget \[ 0 \] . LogicOpEnable</span><span class="sxs-lookup"><span data-stu-id="8a111-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="8a111-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8a111-123">**FALSE**</span></span>                        |
| <span data-ttu-id="8a111-124">RenderTarget \[ 0 \] . SrcBlend</span><span class="sxs-lookup"><span data-stu-id="8a111-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="8a111-125">D3D12 \_ Blend \_ uno</span><span class="sxs-lookup"><span data-stu-id="8a111-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="8a111-126">RenderTarget \[ 0 \] . DestBlend</span><span class="sxs-lookup"><span data-stu-id="8a111-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="8a111-127">Cero de D3D12 \_ Blend \_</span><span class="sxs-lookup"><span data-stu-id="8a111-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="8a111-128">RenderTarget \[ 0 \] . BlendOp</span><span class="sxs-lookup"><span data-stu-id="8a111-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="8a111-129">Operación de incorporación de D3D12 \_ Blend \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a111-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="8a111-130">RenderTarget \[ 0 \] . SrcBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="8a111-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="8a111-131">D3D12 \_ Blend \_ uno</span><span class="sxs-lookup"><span data-stu-id="8a111-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="8a111-132">RenderTarget \[ 0 \] . DestBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="8a111-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="8a111-133">Cero de D3D12 \_ Blend \_</span><span class="sxs-lookup"><span data-stu-id="8a111-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="8a111-134">RenderTarget \[ 0 \] . BlendOpAlpha</span><span class="sxs-lookup"><span data-stu-id="8a111-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="8a111-135">Operación de incorporación de D3D12 \_ Blend \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a111-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="8a111-136">RenderTarget \[ 0 \] . LogicOp</span><span class="sxs-lookup"><span data-stu-id="8a111-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="8a111-137">D3D12 \_ Logical \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a111-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="8a111-138">RenderTarget \[ 0 \] . RenderTargetWriteMask</span><span class="sxs-lookup"><span data-stu-id="8a111-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="8a111-139">D3D12 \_ de \_ escritura de color \_ habilitar \_ todo</span><span class="sxs-lookup"><span data-stu-id="8a111-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="8a111-140">**~ CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="8a111-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="8a111-141">Destruye una instancia de una descripción de CD3DX12 \_ Blend \_ .</span><span class="sxs-lookup"><span data-stu-id="8a111-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="8a111-142">**Operator const D3D12 \_ Blend \_ DESC& () Const**</span><span class="sxs-lookup"><span data-stu-id="8a111-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8a111-143">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="8a111-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a111-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a111-144">Requirements</span></span>



| <span data-ttu-id="8a111-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a111-145">Requirement</span></span> | <span data-ttu-id="8a111-146">Value</span><span class="sxs-lookup"><span data-stu-id="8a111-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a111-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a111-147">Header</span></span><br/> | <dl> <span data-ttu-id="8a111-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a111-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a111-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a111-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a111-150">**D3D12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8a111-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="8a111-151">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="8a111-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





