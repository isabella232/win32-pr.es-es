---
title: CD3DX12_RECT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura Rect de D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Estructura de CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717609"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="e5c2e-104">CD3DX12 \_ Rect (estructura)</span><span class="sxs-lookup"><span data-stu-id="e5c2e-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="e5c2e-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ Rect de D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c2e-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c2e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5c2e-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="e5c2e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5c2e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5c2e-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="e5c2e-109">Crea una nueva instancia no inicializada de un CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="e5c2e-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="e5c2e-110">**CD3DX12 \_ Rect explícito (const D3D12 \_ Rect& o)**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="e5c2e-111">Crea una nueva instancia de un CD3DX12 \_ Rect, inicializada con el contenido de otra [**estructura \_ Rect de D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c2e-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5c2e-112">**CD3DX12 \_ rectángulo explícito (largo izquierdo, largo superior, largo derecho, largo inferior)**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="e5c2e-113">Crea una nueva instancia de un CD3DX12 \_ Rect, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="e5c2e-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="e5c2e-114">LARGA izquierda</span><span class="sxs-lookup"><span data-stu-id="e5c2e-114">LONG Left</span></span>

<span data-ttu-id="e5c2e-115">Superior larga</span><span class="sxs-lookup"><span data-stu-id="e5c2e-115">LONG Top</span></span>

<span data-ttu-id="e5c2e-116">LARGA a la derecha</span><span class="sxs-lookup"><span data-stu-id="e5c2e-116">LONG Right</span></span>

<span data-ttu-id="e5c2e-117">Inferior largo</span><span class="sxs-lookup"><span data-stu-id="e5c2e-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="e5c2e-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="e5c2e-119">Destruye una instancia de un CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="e5c2e-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="e5c2e-120">**Operator const D3D12 \_ RECT& () Const**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e5c2e-121">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="e5c2e-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5c2e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5c2e-122">Requirements</span></span>



| <span data-ttu-id="e5c2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c2e-123">Requirement</span></span> | <span data-ttu-id="e5c2e-124">Value</span><span class="sxs-lookup"><span data-stu-id="e5c2e-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c2e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5c2e-125">Header</span></span><br/> | <dl> <span data-ttu-id="e5c2e-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c2e-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c2e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5c2e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c2e-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="e5c2e-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="e5c2e-129">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e5c2e-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





