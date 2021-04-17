---
title: CD3DX12_BOX estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de cuadro de D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Estructura de CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698204"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="c5691-104">Estructura del cuadro de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="c5691-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="c5691-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ cuadro de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="c5691-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5691-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5691-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="c5691-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5691-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5691-108">**Cuadro de CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c5691-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-109">Crea una nueva instancia no inicializada de un \_ cuadro CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="c5691-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="c5691-110">**cuadro CD3DX12 explícito \_ (const D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="c5691-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-111">Crea una nueva instancia de un \_ cuadro CD3DX12, inicializada con el contenido de otra estructura de [**\_ cuadros de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="c5691-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c5691-112">**cuadro CD3DX12 explícito \_ (largo izquierdo, largo derecho)**</span><span class="sxs-lookup"><span data-stu-id="c5691-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-113">Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c5691-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="c5691-114">LARGA izquierda</span><span class="sxs-lookup"><span data-stu-id="c5691-114">LONG Left</span></span>

<span data-ttu-id="c5691-115">LARGA a la derecha</span><span class="sxs-lookup"><span data-stu-id="c5691-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="c5691-116">**cuadro CD3DX12 explícito \_ (largo izquierdo, largo superior, largo derecho, largo inferior)**</span><span class="sxs-lookup"><span data-stu-id="c5691-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-117">Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c5691-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="c5691-118">LARGA izquierda</span><span class="sxs-lookup"><span data-stu-id="c5691-118">LONG Left</span></span>

<span data-ttu-id="c5691-119">Superior larga</span><span class="sxs-lookup"><span data-stu-id="c5691-119">LONG Top</span></span>

<span data-ttu-id="c5691-120">LARGA a la derecha</span><span class="sxs-lookup"><span data-stu-id="c5691-120">LONG Right</span></span>

<span data-ttu-id="c5691-121">Inferior largo</span><span class="sxs-lookup"><span data-stu-id="c5691-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="c5691-122">**cuadro CD3DX12 explícito \_ (Long Left, Long Top, Long Front, Long Right, Long Bottom, Long back)**</span><span class="sxs-lookup"><span data-stu-id="c5691-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-123">Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c5691-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="c5691-124">LARGA izquierda</span><span class="sxs-lookup"><span data-stu-id="c5691-124">LONG Left</span></span>

<span data-ttu-id="c5691-125">Superior larga</span><span class="sxs-lookup"><span data-stu-id="c5691-125">LONG Top</span></span>

<span data-ttu-id="c5691-126">Inicial larga</span><span class="sxs-lookup"><span data-stu-id="c5691-126">LONG Front</span></span>

<span data-ttu-id="c5691-127">LARGA a la derecha</span><span class="sxs-lookup"><span data-stu-id="c5691-127">LONG Right</span></span>

<span data-ttu-id="c5691-128">Inferior largo</span><span class="sxs-lookup"><span data-stu-id="c5691-128">LONG Bottom</span></span>

<span data-ttu-id="c5691-129">LARGA</span><span class="sxs-lookup"><span data-stu-id="c5691-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="c5691-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="c5691-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-131">Destruye una instancia de un cuadro de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c5691-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="c5691-132">**Operator const D3D12 \_ BOX& () Const**</span><span class="sxs-lookup"><span data-stu-id="c5691-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c5691-133">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="c5691-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5691-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5691-134">Requirements</span></span>



| <span data-ttu-id="c5691-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5691-135">Requirement</span></span> | <span data-ttu-id="c5691-136">Value</span><span class="sxs-lookup"><span data-stu-id="c5691-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5691-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5691-137">Header</span></span><br/> | <dl> <span data-ttu-id="c5691-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5691-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5691-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5691-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5691-140">**Cuadro de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="c5691-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="c5691-141">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="c5691-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





