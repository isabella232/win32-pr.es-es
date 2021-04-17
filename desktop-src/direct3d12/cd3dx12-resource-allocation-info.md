---
title: CD3DX12_RESOURCE_ALLOCATION_INFO estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de información de asignación de recursos de D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Estructura de CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717608"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="7fbc2-104">CD3DX12 \_ \_ estructura de información de asignación de recursos \_</span><span class="sxs-lookup"><span data-stu-id="7fbc2-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="7fbc2-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**información de asignación de recursos de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="7fbc2-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbc2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fbc2-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="7fbc2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fbc2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fbc2-108">**Información de asignación de recursos de CD3DX12 \_ \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="7fbc2-109">Crea una nueva instancia no inicializada de la información de asignación de recursos de CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fbc2-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="7fbc2-110">**información de \_ asignación de recursos CD3DX12 explícita \_ \_ (const D3D12 \_ información de asignación de recursos \_ \_& o)**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7fbc2-111">Crea una nueva instancia de una \_ información de asignación de recursos CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de información de [**\_ asignación de recursos \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="7fbc2-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fbc2-112">**\_ \_ \_ Información de asignación de recursos CD3DX12 (tamaño UINT64, alineación UInt64)**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="7fbc2-113">Crea una nueva instancia de una \_ información de asignación de recursos CD3DX12 \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="7fbc2-114">UINT64 size</span><span class="sxs-lookup"><span data-stu-id="7fbc2-114">UINT64 size</span></span>

<span data-ttu-id="7fbc2-115">Alineación UINT64</span><span class="sxs-lookup"><span data-stu-id="7fbc2-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="7fbc2-116">**operador const D3D12 \_ información de asignación de recursos \_ \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7fbc2-117">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="7fbc2-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fbc2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbc2-118">Requirements</span></span>



| <span data-ttu-id="7fbc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbc2-119">Requirement</span></span> | <span data-ttu-id="7fbc2-120">Value</span><span class="sxs-lookup"><span data-stu-id="7fbc2-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-121">Header</span></span><br/> | <dl> <span data-ttu-id="7fbc2-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc2-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbc2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbc2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbc2-124">**\_Información de \_ asignación de recursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="7fbc2-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="7fbc2-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





