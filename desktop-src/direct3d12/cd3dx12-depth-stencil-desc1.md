---
title: CD3DX12_DEPTH_STENCIL_DESC1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC1 de D3D12 Depth \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Estructura de CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649383"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="03f00-104">CD3DX12 de estarcido de profundidad de la \_ \_ \_ estructura DESC1</span><span class="sxs-lookup"><span data-stu-id="03f00-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="03f00-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ \_ DESC1 de D3D12 Depth**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="03f00-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f00-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03f00-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="03f00-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="03f00-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="03f00-108">**CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="03f00-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-109">Crea una instancia nueva, no inicializada, de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="03f00-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-110">**Galería de \_ símbolos de profundidad CD3DX12 explícita \_ \_ DESC1 (const D3D12 \_ Depth \_ estarcido \_ DESC1&)**</span><span class="sxs-lookup"><span data-stu-id="03f00-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-111">Crea una nueva instancia de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1, inicializada con los valores copiados de una estructura de [**estarcido de \_ profundidad D3D12 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="03f00-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-112">**Galería de \_ símbolos de profundidad CD3DX12 explícita \_ \_ DESC1 (const D3D12 \_ Depth \_ estarcido \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="03f00-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-113">Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores copiados de una estructura de descripción de la [**Galería de \_ \_ símbolos \_ D3D12 Depth**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="03f00-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="03f00-114">y el miembro **DepthBoundsTestEnable** adicional establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="03f00-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-115">**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC1 ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="03f00-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-116">Crea una nueva instancia de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1, inicializada con el estado predeterminado indicado por D3DX12:</span><span class="sxs-lookup"><span data-stu-id="03f00-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="03f00-117">**\_ \_ Galería de símbolos de profundidad de CD3DX12 explícita \_ DESC1 (bool depthEnable, D3D12 \_ Depth \_ \_ Mask Mask depthWriteMask, D3D12 \_ Comparison \_ FUNC DEPTHFUNC, bool STENCILENABLE, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ stencil OP frontStencilFailOp, \_ D3D12 \_ cliché \_ OP frontStencilDepthFailOp, D3D12 stencil \_ OP \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilPassOp, D3D12 Comparison frontStencilFunc, D3D12, backStencilFailOp, D3D12, backStencilDepthFailOp de estarcido OP D3D12)**</span><span class="sxs-lookup"><span data-stu-id="03f00-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-118">Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="03f00-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-119">**~ CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="03f00-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-120">Destruye una instancia de una galería de \_ símbolos de profundidad de D3DX12 \_ \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="03f00-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-121">**operador const D3D12 \_ Depth \_ esténcil \_ DESC1& () Const**</span><span class="sxs-lookup"><span data-stu-id="03f00-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-122">Conversión implícita a una \_ estructura DESC1 de D3D12 Depth \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="03f00-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="03f00-123">Dado que \_ \_ la Galería \_ de símbolos de profundidad de D3D12 DESC1 es el tipo subyacente de la \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, el objeto simplemente se devuelve como una \_ \_ \_ referencia de D3D12 de estarcido de profundidad const DESC1.</span><span class="sxs-lookup"><span data-stu-id="03f00-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="03f00-124">**operador const D3D12 \_ Depth \_ estarcido \_ DESC () Const**</span><span class="sxs-lookup"><span data-stu-id="03f00-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="03f00-125">Conversión implícita a un \_ valor de \_ estructura DESC de estarcido D3D12 Depth \_ .</span><span class="sxs-lookup"><span data-stu-id="03f00-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="03f00-126">Dado \_ que D3D12 Depth \_ stencil \_ no es el tipo subyacente de CD3DX12 \_ Depth \_ stencil \_ DESC1, se crea una nueva instancia de la galería de símbolos de profundidad D3D12 \_ \_ \_ y se devuelve por valor.</span><span class="sxs-lookup"><span data-stu-id="03f00-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="03f00-127">Tenga en cuenta \_ que \_ la descripción de la galería de símbolos de profundidad \_ de D3D12 no incluye el miembro **DepthBoundsTestEnable** , por lo que este valor se pierde en la conversión.</span><span class="sxs-lookup"><span data-stu-id="03f00-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03f00-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f00-128">Requirements</span></span>



| <span data-ttu-id="03f00-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f00-129">Requirement</span></span> | <span data-ttu-id="03f00-130">Value</span><span class="sxs-lookup"><span data-stu-id="03f00-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03f00-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03f00-131">Header</span></span><br/> | <dl> <span data-ttu-id="03f00-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f00-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f00-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="03f00-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f00-134">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="03f00-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="03f00-135">**Galería de símbolos de profundidad de D3D12 \_ \_ \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="03f00-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="03f00-136">**D3D12 de la \_ Galería de símbolos de profundidad \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03f00-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





