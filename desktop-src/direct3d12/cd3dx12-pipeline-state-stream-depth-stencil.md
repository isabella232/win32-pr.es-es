---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12. h)
description: Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678773"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a><span data-ttu-id="933ab-105">\_Estructura de \_ \_ estarcido de profundidad de flujo de estado de \_ canalización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="933ab-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL structure</span></span>

<span data-ttu-id="933ab-106">Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="933ab-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="933ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="933ab-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="933ab-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="933ab-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="933ab-109">**\_Galería de \_ \_ símbolos de profundidad de flujo de estado de \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="933ab-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>
</dt> <dd>

<span data-ttu-id="933ab-110">Crea una nueva instancia no inicializada de una \_ Galería de símbolos de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="933ab-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL.</span></span>

</dd> <dt>

<span data-ttu-id="933ab-111">**Estarcido de profundidad de flujo de estado de canalización de CD3DX12 (Galería de \_ símbolos de \_ \_ \_ \_ \_ profundidad CD3DX12 \_ \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="933ab-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL(CD3DX12\_DEPTH\_STENCIL\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="933ab-112">Crea una nueva instancia de una \_ Galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de la galería de símbolos de  **profundidad de \_ \_ \_ tipo de subobjeto \_ \_ \_ de estado de canalización de D3D12** y datos de subobjeto copiados de i, una estructura de [**\_ \_ \_ Descripción de estarcido**](cd3dx12-depth-stencil-desc.md) de</span><span class="sxs-lookup"><span data-stu-id="933ab-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="933ab-113">**Operator = (CD3DX12 \_ Depth \_ estarcido \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="933ab-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="933ab-114">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="933ab-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="933ab-115">**CD3DX12 de la \_ Galería de símbolos de profundidad del operador \_ \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="933ab-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="933ab-116">Conversión implícita a una [**estructura \_ \_ \_ DESC de estarcido de profundidad de CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="933ab-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="933ab-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="933ab-117">Remarks</span></span>

<span data-ttu-id="933ab-118">\_ \_ \_ \_ \_ La galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="933ab-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a><span data-ttu-id="933ab-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="933ab-119">Requirements</span></span>



| <span data-ttu-id="933ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="933ab-120">Requirement</span></span> | <span data-ttu-id="933ab-121">Value</span><span class="sxs-lookup"><span data-stu-id="933ab-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="933ab-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="933ab-122">Header</span></span><br/> | <dl> <span data-ttu-id="933ab-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="933ab-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933ab-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="933ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933ab-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="933ab-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="933ab-126">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="933ab-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="933ab-127">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="933ab-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

