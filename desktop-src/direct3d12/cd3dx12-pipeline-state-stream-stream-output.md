---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la descripción de salida de flujo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717615"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="5ea52-104">Estructura de la secuencia de salida de flujo de \_ Estado de canalización CD3DX12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ea52-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="5ea52-105">Una estructura de aplicación auxiliar que se usa para describir la descripción de salida de flujo como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="5ea52-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea52-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea52-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="5ea52-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ea52-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ea52-108">**\_Salida de \_ \_ flujo de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ea52-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="5ea52-109">Crea una nueva instancia no inicializada de una \_ salida de flujo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5ea52-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="5ea52-110">**\_Salida de flujo de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ (DESC de salida de secuencia de D3D12 de \_ \_ salida \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="5ea52-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="5ea52-111">Crea una nueva instancia de una \_ salida de flujo de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ salida de flujo** y datos de subobjeto copiados de *i*, una estructura de DESC de [**salida de flujo de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="5ea52-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ea52-112">**Operator = (D3D12 \_ Stream \_ Output \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="5ea52-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="5ea52-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="5ea52-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="5ea52-114">**Operator D3D12 \_ Stream \_ Output \_ DESC () Const**</span><span class="sxs-lookup"><span data-stu-id="5ea52-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="5ea52-115">Conversión implícita a una [**estructura \_ \_ \_ DESC de salida de secuencia D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="5ea52-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ea52-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea52-116">Remarks</span></span>

<span data-ttu-id="5ea52-117">\_ \_ \_ \_ \_ La salida de flujo de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5ea52-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="5ea52-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea52-118">Requirements</span></span>



| <span data-ttu-id="5ea52-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea52-119">Requirement</span></span> | <span data-ttu-id="5ea52-120">Value</span><span class="sxs-lookup"><span data-stu-id="5ea52-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea52-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea52-121">Header</span></span><br/> | <dl> <span data-ttu-id="5ea52-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea52-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea52-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea52-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="5ea52-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5ea52-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ea52-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="5ea52-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ea52-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

