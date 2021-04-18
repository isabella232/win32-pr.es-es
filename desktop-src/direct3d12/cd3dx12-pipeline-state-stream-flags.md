---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS estructura (D3dx12. h)
description: Estructura auxiliar que se usa para describir las marcas de estado de canalización como un solo objeto adecuado para una descripción de flujo.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649457"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="8a15d-104">\_Estructura de \_ \_ marcas de flujo de estado de canalización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8a15d-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="8a15d-105">Estructura auxiliar que se usa para describir las marcas de estado de canalización como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="8a15d-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a15d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a15d-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="8a15d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a15d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a15d-108">**\_Marcas de \_ flujo de estado de CANALización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a15d-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="8a15d-109">Crea una nueva instancia no inicializada de las marcas de flujo de estado de la \_ canalización CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8a15d-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="8a15d-110">**\_Marcas de flujo de estado de canalización de CD3DX12 \_ \_ \_ (marcas de estado de \_ canalización de D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="8a15d-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8a15d-111">Crea una nueva instancia de las \_ marcas de flujo de estado de canalización de CD3DX12 \_ \_ \_ , inicializadas con un tipo de subobjeto de **D3D12 de \_ \_ \_ \_ tipo \_ de subobjeto de estado de canalización de** y datos de subobjeto copiados de *i*, una estructura de marcas de [**\_ \_ estado \_ de canalización de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="8a15d-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a15d-112">**operador = ( \_ marcas de estado de canalización de D3D12 \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="8a15d-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8a15d-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="8a15d-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8a15d-114">**operador de \_ Estado de canalización D3D12 \_ \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="8a15d-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="8a15d-115">Conversión implícita a una estructura de marcas de estado de la [**\_ canalización \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="8a15d-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a15d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a15d-116">Remarks</span></span>

<span data-ttu-id="8a15d-117">\_ \_ \_ El flujo de estado de canalización CD3DX12 \_ Flags es una especialización typedef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8a15d-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="8a15d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a15d-118">Requirements</span></span>



| <span data-ttu-id="8a15d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a15d-119">Requirement</span></span> | <span data-ttu-id="8a15d-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a15d-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a15d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a15d-121">Header</span></span><br/> | <dl> <span data-ttu-id="8a15d-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a15d-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a15d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a15d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a15d-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="8a15d-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8a15d-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a15d-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8a15d-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a15d-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

