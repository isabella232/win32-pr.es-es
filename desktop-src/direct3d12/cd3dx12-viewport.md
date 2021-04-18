---
title: CD3DX12_VIEWPORT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de la ventanilla de D3D12 \_ .
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Estructura de CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718485"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="4e297-104">CD3DX12 (estructura de la \_ ventanilla)</span><span class="sxs-lookup"><span data-stu-id="4e297-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="4e297-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="4e297-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4e297-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="4e297-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4e297-107">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de la [**\_ ventanilla de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .</span><span class="sxs-lookup"><span data-stu-id="4e297-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e297-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e297-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="4e297-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e297-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e297-110">**CD3DX12 \_ ventanilla ()**</span><span class="sxs-lookup"><span data-stu-id="4e297-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-111">Crea una nueva instancia no inicializada de una \_ ventanilla CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="4e297-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="4e297-112">**ventanilla CD3DX12 explícita \_ (const D3D12 \_ viewport& o)**</span><span class="sxs-lookup"><span data-stu-id="4e297-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-113">Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4e297-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4e297-114">const D3D12 \_ VIEWPORT& o</span><span class="sxs-lookup"><span data-stu-id="4e297-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="4e297-115">**CD3DX12 \_ de ventanilla explícita (float topLeftX, Float Lefty, Float width, Float height, Float minDepth = D3D12 \_ min \_ Depth, Float maxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="4e297-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-116">Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4e297-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4e297-117">FLOAT topLeftX</span><span class="sxs-lookup"><span data-stu-id="4e297-117">FLOAT topLeftX</span></span>

<span data-ttu-id="4e297-118">FLOAT izquierda</span><span class="sxs-lookup"><span data-stu-id="4e297-118">FLOAT topLeftY</span></span>

<span data-ttu-id="4e297-119">Ancho flotante</span><span class="sxs-lookup"><span data-stu-id="4e297-119">FLOAT width</span></span>

<span data-ttu-id="4e297-120">Alto de FLOAT</span><span class="sxs-lookup"><span data-stu-id="4e297-120">FLOAT height</span></span>

<span data-ttu-id="4e297-121">FLOAT minDepth = D3D12 \_ min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4e297-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="4e297-122">FLOAT maxDepth = D3D12 \_ Max \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4e297-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="4e297-123">**CD3DX12 \_ de ventanilla explícita (ID3D12Resource \* PreSource, uint mipSlice = 0, Float topLeftX = 0.0 f, Float Lefty = 0.0 f, Float MINDEPTH = D3D12 \_ min \_ Depth, Float maxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="4e297-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-124">Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4e297-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4e297-125">\*Código fuente de ID3D12Resource</span><span class="sxs-lookup"><span data-stu-id="4e297-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="4e297-126">UINT mipSlice = 0</span><span class="sxs-lookup"><span data-stu-id="4e297-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="4e297-127">FLOAT topLeftX = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="4e297-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="4e297-128">FLOAT izquierda = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="4e297-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="4e297-129">FLOAT minDepth = D3D12 \_ min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4e297-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="4e297-130">FLOAT maxDepth = D3D12 \_ Max \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4e297-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="4e297-131">**~ CD3DX12 \_ ventanilla ()**</span><span class="sxs-lookup"><span data-stu-id="4e297-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-132">Destruye una instancia de una ventanilla de D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="4e297-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="4e297-133">**Operator const D3D12 \_ VIEWPORT& () Const**</span><span class="sxs-lookup"><span data-stu-id="4e297-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4e297-134">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="4e297-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e297-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e297-135">Requirements</span></span>



| <span data-ttu-id="4e297-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e297-136">Requirement</span></span> | <span data-ttu-id="4e297-137">Value</span><span class="sxs-lookup"><span data-stu-id="4e297-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e297-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e297-138">Header</span></span><br/> | <dl> <span data-ttu-id="4e297-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e297-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e297-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e297-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e297-141">**Ventanilla de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4e297-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="4e297-142">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4e297-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





