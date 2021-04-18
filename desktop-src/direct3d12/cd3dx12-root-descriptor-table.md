---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de tabla de descriptores raíz D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717599"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="2260f-104">CD3DX12 \_ \_ estructura de tabla del descriptor raíz \_</span><span class="sxs-lookup"><span data-stu-id="2260f-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="2260f-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ tabla de descriptores raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="2260f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2260f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2260f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="2260f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2260f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2260f-108">**CD3DX12 \_ \_ tabla de descriptor raíz \_ ()**</span><span class="sxs-lookup"><span data-stu-id="2260f-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="2260f-109">Crea una nueva instancia no inicializada de una \_ \_ tabla de descriptor raíz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="2260f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="2260f-110">**tabla de \_ \_ descriptor raíz CD3DX12 explícita \_ (const D3D12 \_ tabla de \_ descriptor raíz \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="2260f-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2260f-111">Crea una nueva instancia de una \_ tabla de \_ descriptor raíz CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ \_ tabla del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="2260f-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2260f-112">**CD3DX12 \_ \_ tabla de descriptor raíz \_ (uint NUMDESCRIPTORRANGES, const D3D12 de \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="2260f-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="2260f-113">Crea una nueva instancia de una \_ tabla de \_ descriptor raíz CD3DX12 \_ , inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="2260f-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="2260f-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="2260f-115">[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="2260f-116">**Init en línea (UINT numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="2260f-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="2260f-117">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="2260f-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2260f-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="2260f-119">[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="2260f-120">**Static inline init (D3D12 \_ root \_ descriptor \_ TABLE &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="2260f-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="2260f-121">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="2260f-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2260f-122">[**D3D12 \_ \_ \_ Tabla del descriptor raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="2260f-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="2260f-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="2260f-124">[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="2260f-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2260f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2260f-125">Requirements</span></span>



| <span data-ttu-id="2260f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2260f-126">Requirement</span></span> | <span data-ttu-id="2260f-127">Value</span><span class="sxs-lookup"><span data-stu-id="2260f-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2260f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2260f-128">Header</span></span><br/> | <dl> <span data-ttu-id="2260f-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2260f-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2260f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2260f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2260f-131">**\_Tabla del \_ descriptor raíz de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2260f-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="2260f-132">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="2260f-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





