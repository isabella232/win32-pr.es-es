---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura TABLE1 del descriptor raíz D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718494"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="4a800-104">CD3DX12 \_ \_ estructura TABLE1 del descriptor raíz \_</span><span class="sxs-lookup"><span data-stu-id="4a800-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="4a800-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ \_ TABLE1 del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="4a800-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a800-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a800-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="4a800-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a800-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a800-108">**CD3DX12 \_ root \_ descriptor \_ TABLE1 ()**</span><span class="sxs-lookup"><span data-stu-id="4a800-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="4a800-109">Crea una nueva instancia no inicializada de un \_ \_ descriptor de raíz CD3DX12 \_ TABLE1.</span><span class="sxs-lookup"><span data-stu-id="4a800-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="4a800-110">**descriptor de raíz CD3DX12 explícito \_ \_ \_ TABLE1 (const D3D12 \_ raíz \_ \_ Table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="4a800-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4a800-111">Crea una nueva instancia de un \_ \_ descriptor de raíz CD3DX12 \_ Table1, inicializada con el contenido de otra estructura [**\_ \_ \_ TABLE1 del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="4a800-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a800-112">**CD3DX12 \_ root \_ descriptor \_ TABLE1 (uint NUMDESCRIPTORRANGES, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="4a800-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4a800-113">Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12 \_ TABLE1, inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4a800-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="4a800-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4a800-115">const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="4a800-116">**Init en línea (UINT numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="4a800-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4a800-117">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a800-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4a800-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4a800-119">const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="4a800-120">**Inicial inline init (D3D12 \_ root \_ descriptor \_ TABLE1 &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="4a800-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4a800-121">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a800-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4a800-122">[**D3D12 \_ Descriptor de raíz \_ \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="4a800-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="4a800-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4a800-124">const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4a800-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a800-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a800-125">Requirements</span></span>



| <span data-ttu-id="4a800-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a800-126">Requirement</span></span> | <span data-ttu-id="4a800-127">Value</span><span class="sxs-lookup"><span data-stu-id="4a800-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a800-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a800-128">Header</span></span><br/> | <dl> <span data-ttu-id="4a800-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a800-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a800-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a800-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a800-131">**D3D12 \_ el \_ descriptor raíz \_ TABLE1**</span><span class="sxs-lookup"><span data-stu-id="4a800-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="4a800-132">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4a800-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





