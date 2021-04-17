---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir el valor de corte de la franja del búfer de índice como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653271"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="e7281-104">Secuencia de estado de canalización de CD3DX12 de la \_ estructura de valor de \_ \_ \_ \_ corte de franja \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7281-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="e7281-105">Una estructura de aplicación auxiliar que se usa para describir el valor de corte de la franja del búfer de índice como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e7281-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7281-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7281-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="e7281-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7281-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7281-108">**Flujo de estado de canalización de CD3DX12 de \_ Estado de canalización \_ \_ \_ IB \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7281-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="e7281-109">Crea una instancia nueva, no inicializada, de un valor de corte de la franja de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7281-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="e7281-110">**\_Valor de canalización CD3DX12 flujo de estado de canalización \_ \_ \_ IB \_ \_ \_ (D3D12 \_ valor de corte de franja de búfer de índice \_ \_ \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="e7281-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="e7281-111">Crea una nueva instancia de un valor de corte de la \_ franja de estado de la canalización de CD3DX12 \_ \_ \_ \_ \_ \_ , inicializada con un tipo de subobjeto del **\_ \_ \_ tipo de subobjeto \_ \_ \_ \_ \_ de estado de canalización** IB y datos de subobjeto copiados de *i*, una estructura de [**valor de corte de \_ franja de búfer de índice \_ \_ \_ \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="e7281-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7281-112">**Operator = (D3D12 \_ Índice de la franja de búfer de índice \_ \_ \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="e7281-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="e7281-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="e7281-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="e7281-114">**operador D3D12 \_ index de búfer de índice \_ \_ \_ \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="e7281-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="e7281-115">Conversión implícita a una estructura de [**valor de corte de franja del búfer de índice de D3D12 \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="e7281-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7281-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7281-116">Remarks</span></span>

<span data-ttu-id="e7281-117">\_La secuencia de estado de la canalización de CD3DX12 \_ \_ \_ \_ \_ \_ valor de corte de franjas de división es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e7281-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="e7281-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7281-118">Requirements</span></span>



| <span data-ttu-id="e7281-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7281-119">Requirement</span></span> | <span data-ttu-id="e7281-120">Value</span><span class="sxs-lookup"><span data-stu-id="e7281-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7281-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7281-121">Header</span></span><br/> | <dl> <span data-ttu-id="e7281-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7281-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7281-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7281-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7281-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e7281-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e7281-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7281-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="e7281-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7281-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

