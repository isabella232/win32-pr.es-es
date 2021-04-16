---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12. h)
description: Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649376"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="e09c1-105">CD3DX12 \_ profundidad de flujo de estado de canalización \_ \_ \_ \_ STENCIL1 estructura</span><span class="sxs-lookup"><span data-stu-id="e09c1-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="e09c1-106">Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e09c1-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09c1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e09c1-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="e09c1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e09c1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e09c1-109">**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="e09c1-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="e09c1-110">Crea una instancia nueva, no inicializada, de una \_ profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1.</span><span class="sxs-lookup"><span data-stu-id="e09c1-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="e09c1-111">**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1 (CD3DX12 de \_ estarcido de profundidad \_ \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="e09c1-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="e09c1-112">Crea una nueva instancia de una \_ profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1, inicializada con un tipo de subobjeto de **\_ \_ tipo subobjeto de estado de canalización de D3D12 \_ \_ \_ profundidad \_ STENCIL1** y datos de subobjeto copiados de *i*, una estructura CD3DX12 de [**\_ \_ estarcido \_ de profundidad**](cd3dx12-depth-stencil-desc1.md) DESC1.</span><span class="sxs-lookup"><span data-stu-id="e09c1-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e09c1-113">**Operator = (CD3DX12 \_ Depth \_ stencil \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="e09c1-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="e09c1-114">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="e09c1-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="e09c1-115">**Galería de símbolos de profundidad de CD3DX12 de operador \_ \_ \_ DESC1 () Const**</span><span class="sxs-lookup"><span data-stu-id="e09c1-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="e09c1-116">Conversión implícita a una [**estructura \_ \_ \_ DESC1 de CD3DX12 Depth**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="e09c1-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e09c1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e09c1-117">Remarks</span></span>

<span data-ttu-id="e09c1-118">\_ \_ \_ \_ La profundidad de flujo de estado de canalización \_ de CD3DX12 STENCIL1 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e09c1-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="e09c1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e09c1-119">Requirements</span></span>



| <span data-ttu-id="e09c1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e09c1-120">Requirement</span></span> | <span data-ttu-id="e09c1-121">Value</span><span class="sxs-lookup"><span data-stu-id="e09c1-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e09c1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e09c1-122">Header</span></span><br/> | <dl> <span data-ttu-id="e09c1-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e09c1-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09c1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e09c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09c1-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e09c1-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e09c1-126">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e09c1-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="e09c1-127">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e09c1-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

