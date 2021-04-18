---
title: CD3DX12_RANGE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de intervalo de D3D12 \_ .
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Estructura de CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718500"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="e7ac2-104">Estructura de intervalo de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="e7ac2-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="e7ac2-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="e7ac2-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ac2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7ac2-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="e7ac2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7ac2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7ac2-108">**\_Intervalo CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="e7ac2-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="e7ac2-109">Crea una nueva instancia no inicializada de un intervalo de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e7ac2-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="e7ac2-110">**intervalo de CD3DX12 explícito \_ (const D3D12 \_ Range &o)**</span><span class="sxs-lookup"><span data-stu-id="e7ac2-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e7ac2-111">Crea una nueva instancia de un intervalo de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="e7ac2-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7ac2-112">**\_Intervalo CD3DX12 (tamaño \_ t inicio, tamaño \_ t final)**</span><span class="sxs-lookup"><span data-stu-id="e7ac2-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="e7ac2-113">Crea una nueva instancia de un intervalo de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="e7ac2-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="e7ac2-114">TAMAÑO \_ T Inicio</span><span class="sxs-lookup"><span data-stu-id="e7ac2-114">SIZE\_T begin</span></span>

<span data-ttu-id="e7ac2-115">TAMAÑO \_ T final</span><span class="sxs-lookup"><span data-stu-id="e7ac2-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="e7ac2-116">**Operator const D3D12 \_ RANGE& () Const**</span><span class="sxs-lookup"><span data-stu-id="e7ac2-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e7ac2-117">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="e7ac2-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7ac2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ac2-118">Requirements</span></span>



| <span data-ttu-id="e7ac2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ac2-119">Requirement</span></span> | <span data-ttu-id="e7ac2-120">Value</span><span class="sxs-lookup"><span data-stu-id="e7ac2-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ac2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7ac2-121">Header</span></span><br/> | <dl> <span data-ttu-id="e7ac2-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ac2-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ac2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7ac2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ac2-124">**\_Intervalo D3D12**</span><span class="sxs-lookup"><span data-stu-id="e7ac2-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="e7ac2-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e7ac2-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





