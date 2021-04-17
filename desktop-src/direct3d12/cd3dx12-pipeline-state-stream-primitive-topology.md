---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la topología primitiva como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698191"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="99689-104">CD3DX12 \_ estructura de la topología de flujo de estado de canalización \_ \_ \_ primitiva \_</span><span class="sxs-lookup"><span data-stu-id="99689-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="99689-105">Una estructura de aplicación auxiliar que se usa para describir la topología primitiva como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="99689-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="99689-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99689-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="99689-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="99689-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="99689-108">**\_ \_ \_ Topología primitiva de flujo de estado \_ de canalización de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="99689-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="99689-109">Crea una nueva instancia no inicializada de una topología primitiva de \_ flujo de estado de la canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99689-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="99689-110">**\_Topología de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (tipo de \_ topología primitiva D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="99689-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="99689-111">Crea una nueva instancia de una \_ topología primitiva de secuencia de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de la **\_ \_ \_ \_ \_ \_ topología primitiva del tipo de subobjeto de estado de canalización D3D12** y datos de subobjeto copiados de *i*, una estructura de [**\_ \_ \_ tipo de topología primitiva de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="99689-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="99689-112">**operador = ( \_ tipo de topología D3D12 primitiva \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="99689-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="99689-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="99689-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="99689-114">**operador de \_ \_ topología primitiva D3D12 \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="99689-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="99689-115">Conversión implícita a una estructura de [**\_ \_ \_ tipo de topología primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="99689-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99689-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99689-116">Remarks</span></span>

<span data-ttu-id="99689-117">\_ \_ La topología de la secuencia de estado de canalización CD3DX12 \_ \_ \_ es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="99689-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="99689-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99689-118">Requirements</span></span>



| <span data-ttu-id="99689-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99689-119">Requirement</span></span> | <span data-ttu-id="99689-120">Value</span><span class="sxs-lookup"><span data-stu-id="99689-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99689-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99689-121">Header</span></span><br/> | <dl> <span data-ttu-id="99689-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="99689-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99689-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="99689-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99689-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="99689-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="99689-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99689-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="99689-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99689-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

