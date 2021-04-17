---
title: CD3DX12_ROOT_DESCRIPTOR estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de descriptor raíz D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718492"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="50134-104">CD3DX12 \_ \_ estructura de descriptor raíz</span><span class="sxs-lookup"><span data-stu-id="50134-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="50134-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="50134-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="50134-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50134-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="50134-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="50134-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="50134-108">**\_Descriptor raíz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="50134-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="50134-109">Crea una nueva instancia no inicializada de un \_ \_ descriptor raíz CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="50134-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="50134-110">**descriptor de raíz de CD3DX12 explícito \_ \_ ( \_ \_ &o descriptor de raíz const D3D12)**</span><span class="sxs-lookup"><span data-stu-id="50134-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="50134-111">Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12, inicializada con el contenido de otra estructura de [**\_ \_ descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="50134-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50134-112">**\_ \_ Descriptor raíz de CD3DX12 (uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="50134-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="50134-113">Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12, inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="50134-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="50134-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="50134-114">UINT shaderRegister</span></span>

<span data-ttu-id="50134-115">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="50134-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="50134-116">**Init en línea (UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="50134-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="50134-117">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="50134-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="50134-118">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="50134-118">UINT shaderRegister</span></span>

<span data-ttu-id="50134-119">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="50134-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="50134-120">**Init inline init (D3D12 \_ root \_ descriptor &Table, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="50134-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="50134-121">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="50134-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="50134-122">[**D3D12 \_ Tabla de &de \_ descriptor raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)</span><span class="sxs-lookup"><span data-stu-id="50134-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="50134-123">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="50134-123">UINT shaderRegister</span></span>

<span data-ttu-id="50134-124">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="50134-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50134-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50134-125">Requirements</span></span>



| <span data-ttu-id="50134-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="50134-126">Requirement</span></span> | <span data-ttu-id="50134-127">Value</span><span class="sxs-lookup"><span data-stu-id="50134-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50134-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50134-128">Header</span></span><br/> | <dl> <span data-ttu-id="50134-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="50134-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50134-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="50134-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50134-131">**\_Descriptor raíz de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="50134-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="50134-132">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="50134-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





