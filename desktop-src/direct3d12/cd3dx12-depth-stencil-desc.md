---
title: CD3DX12_DEPTH_STENCIL_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de descripción de la galería de símbolos de profundidad de D3D12 \_ \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Estructura de CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649386"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="ac5d7-104">CD3DX12 \_ Descripción de la galería de símbolos de profundidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac5d7-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="ac5d7-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de descripción de la [**Galería de símbolos de profundidad de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="ac5d7-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5d7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac5d7-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="ac5d7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac5d7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac5d7-108">**CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-109">Crea una instancia nueva, no inicializada, de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ac5d7-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ac5d7-110">**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC (const D3D12 \_ Depth \_ estarcido \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-111">Crea una nueva instancia de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de la [**Galería de \_ símbolos de profundidad \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="ac5d7-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ac5d7-112">**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-113">Crea una nueva instancia de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ , inicializada con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ac5d7-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="ac5d7-114">**CD3DX12 de la \_ Galería de símbolos de profundidad de profundidad explícita \_ \_ (bool depthEnable, D3D12 \_ profundidad de escritura de profundidad \_ \_ depthWriteMask, D3D12 \_ Comparison \_ FUNC DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ ESTÉNCIL \_ OP frontStencilFailOp, D3D12 stencil OP frontStencilDepthFailOp, D3D12 ESTÉNCIL OP frontStencilPassOp, D3D12 Comparison \_ \_ \_ \_ \_ \_ frontStencilFunc, D3D12 \_ \_ , \_ \_ \_ \_ \_ \_ backStencilFailOp**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-115">Crea una nueva instancia de una \_ Descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="ac5d7-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="ac5d7-116">BOOL depthEnable</span><span class="sxs-lookup"><span data-stu-id="ac5d7-116">BOOL depthEnable</span></span>

<span data-ttu-id="ac5d7-117">[**D3D12 \_ \_ \_ Máscara de escritura de profundidad**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span><span class="sxs-lookup"><span data-stu-id="ac5d7-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="ac5d7-118">[**D3D12 \_ DepthFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación</span><span class="sxs-lookup"><span data-stu-id="ac5d7-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="ac5d7-119">BOOL stencilEnable</span><span class="sxs-lookup"><span data-stu-id="ac5d7-119">BOOL stencilEnable</span></span>

<span data-ttu-id="ac5d7-120">UINT8 stencilReadMask</span><span class="sxs-lookup"><span data-stu-id="ac5d7-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="ac5d7-121">UINT8 stencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="ac5d7-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="ac5d7-122">[**D3D12 \_ FrontStencilFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="ac5d7-123">[**D3D12 \_ FrontStencilDepthFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="ac5d7-124">[**D3D12 \_ FrontStencilPassOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="ac5d7-125">[**D3D12 \_ FrontStencilFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación</span><span class="sxs-lookup"><span data-stu-id="ac5d7-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="ac5d7-126">[**D3D12 \_ BackStencilFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="ac5d7-127">[**D3D12 \_ BackStencilDepthFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="ac5d7-128">[**D3D12 \_ BackStencilPassOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido</span><span class="sxs-lookup"><span data-stu-id="ac5d7-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="ac5d7-129">[**D3D12 \_ BackStencilFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación</span><span class="sxs-lookup"><span data-stu-id="ac5d7-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="ac5d7-130">**~ CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-131">Destruye una instancia de una descripción de la galería de símbolos de profundidad de CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ac5d7-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ac5d7-132">**operador const D3D12 \_ Depth \_ estarcido \_ DESC& () Const**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="ac5d7-133">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="ac5d7-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac5d7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac5d7-134">Requirements</span></span>



| <span data-ttu-id="ac5d7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac5d7-135">Requirement</span></span> | <span data-ttu-id="ac5d7-136">Value</span><span class="sxs-lookup"><span data-stu-id="ac5d7-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5d7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac5d7-137">Header</span></span><br/> | <dl> <span data-ttu-id="ac5d7-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5d7-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac5d7-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac5d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5d7-140">**D3D12 de la \_ Galería de símbolos de profundidad \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ac5d7-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="ac5d7-141">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="ac5d7-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





