---
title: CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir los formatos de destino de representación como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698186"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="8f1f7-104">Estructura de los \_ formatos de destino de representación de secuencia de estado de canalización CD3DX12 \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8f1f7-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="8f1f7-105">Una estructura de aplicación auxiliar que se usa para describir los formatos de destino de representación como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="8f1f7-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f1f7-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="8f1f7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f1f7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f1f7-108">**\_Formatos de \_ \_ destino de representación de secuencia de estado de \_ \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="8f1f7-109">Crea una nueva instancia no inicializada de los formatos de destino de representación de secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8f1f7-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="8f1f7-110">**\_Formatos de destino de representación de secuencia de estado de canalización CD3DX12 \_ \_ \_ \_ \_ (D3D12 \_ RT \_ format \_ array const &i)**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8f1f7-111">Crea una nueva instancia de los \_ formatos de destino de representación de secuencia de estado de canalización de CD3DX12 \_ \_ \_ \_ \_ , inicializado con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 formatos de \_ \_ \_ \_ destino \_ de representación** y datos de subobjeto copiados de *i*, una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="8f1f7-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8f1f7-112">**Operator = (D3D12 \_ RT \_ format \_ array const& i)**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8f1f7-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="8f1f7-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8f1f7-114">**Operator D3D12 \_ RT \_ format \_ array () Const**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="8f1f7-115">Conversión implícita a una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="8f1f7-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f1f7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f1f7-116">Remarks</span></span>

<span data-ttu-id="8f1f7-117">\_ \_ \_ \_ \_ \_ El formato de destino de representación de flujo de estado de canalización CD3DX12 es una especialización de TYPEDEF de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8f1f7-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="8f1f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f1f7-118">Requirements</span></span>



| <span data-ttu-id="8f1f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f1f7-119">Requirement</span></span> | <span data-ttu-id="8f1f7-120">Value</span><span class="sxs-lookup"><span data-stu-id="8f1f7-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1f7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f1f7-121">Header</span></span><br/> | <dl> <span data-ttu-id="8f1f7-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f1f7-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f1f7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f1f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1f7-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="8f1f7-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8f1f7-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8f1f7-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f1f7-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

