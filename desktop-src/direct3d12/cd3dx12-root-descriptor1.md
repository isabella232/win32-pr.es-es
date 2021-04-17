---
title: CD3DX12_ROOT_DESCRIPTOR1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura DESCRIPTOR1 raíz D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718489"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="6f5c1-104">CD3DX12 \_ raíz \_ DESCRIPTOR1 estructura</span><span class="sxs-lookup"><span data-stu-id="6f5c1-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="6f5c1-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESCRIPTOR1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="6f5c1-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5c1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f5c1-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="6f5c1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f5c1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f5c1-108">**\_DESCRIPTOR1 raíz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="6f5c1-109">Crea una nueva instancia no inicializada de un \_ DESCRIPTOR1 raíz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6f5c1-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="6f5c1-110">**CD3DX12 \_ raíz explícita \_ DESCRIPTOR1 (const D3D12 \_ raíz \_ DESCRIPTOR1 &)**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6f5c1-111">Crea una nueva instancia de un \_ DESCRIPTOR1 raíz CD3DX12 \_ , inicializada con el contenido de otra [**estructura \_ \_ DESCRIPTOR1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="6f5c1-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f5c1-112">**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6f5c1-113">Crea una nueva instancia de un \_ DESCRIPTOR1 raíz CD3DX12 \_ , inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f5c1-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="6f5c1-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6f5c1-114">UINT shaderRegister</span></span>

<span data-ttu-id="6f5c1-115">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6f5c1-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="6f5c1-116">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6f5c1-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="6f5c1-117">**Inicialización en línea (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ raíz \_ descriptor marcas \_ Flags = D3D12 \_ marcador de \_ descriptor raíz \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6f5c1-118">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f5c1-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6f5c1-119">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6f5c1-119">UINT shaderRegister</span></span>

<span data-ttu-id="6f5c1-120">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6f5c1-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="6f5c1-121">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6f5c1-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="6f5c1-122">**Static inline init (D3D12 \_ raíz \_ DESCRIPTOR1 &Table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6f5c1-123">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f5c1-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6f5c1-124">[**D3D12 \_ Tabla de &raíz \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)</span><span class="sxs-lookup"><span data-stu-id="6f5c1-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="6f5c1-125">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6f5c1-125">UINT shaderRegister</span></span>

<span data-ttu-id="6f5c1-126">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6f5c1-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="6f5c1-127">[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="6f5c1-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f5c1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f5c1-128">Requirements</span></span>



| <span data-ttu-id="6f5c1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5c1-129">Requirement</span></span> | <span data-ttu-id="6f5c1-130">Value</span><span class="sxs-lookup"><span data-stu-id="6f5c1-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c1-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f5c1-131">Header</span></span><br/> | <dl> <span data-ttu-id="6f5c1-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c1-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5c1-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f5c1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5c1-134">**\_DESCRIPTOR1 raíz \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="6f5c1-135">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="6f5c1-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





