---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una máscara de ejemplo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698406"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a><span data-ttu-id="49940-104">CD3DX12 \_ estructura de la secuencia de estado de canalización de \_ \_ \_ ejemplo \_</span><span class="sxs-lookup"><span data-stu-id="49940-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK structure</span></span>

<span data-ttu-id="49940-105">Una estructura de aplicación auxiliar que se usa para describir una máscara de ejemplo como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="49940-105">A helper structure used to describe a sample mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="49940-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49940-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="49940-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="49940-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="49940-108">**\_Máscara de \_ \_ ejemplo de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49940-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="49940-109">Crea una instancia nueva, no inicializada, de una máscara de ejemplo de flujo de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="49940-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="49940-110">**\_Máscara de ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (uint const &i)**</span><span class="sxs-lookup"><span data-stu-id="49940-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="49940-111">Crea una nueva instancia de una \_ máscara de ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ máscara de ejemplo** y datos de subobjeto copiados de *i*, una máscara de ejemplo **uint** .</span><span class="sxs-lookup"><span data-stu-id="49940-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_MASK** and subobject data copied from *i*, a **UINT** sample mask.</span></span>

</dd> <dt>

<span data-ttu-id="49940-112">**Operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="49940-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="49940-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="49940-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="49940-114">**Operator UINT () Const**</span><span class="sxs-lookup"><span data-stu-id="49940-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="49940-115">Conversión implícita a una máscara de ejemplo **uint** .</span><span class="sxs-lookup"><span data-stu-id="49940-115">Implicit conversion to a **UINT** sample mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49940-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49940-116">Remarks</span></span>

<span data-ttu-id="49940-117">\_La CD3DX12 \_ \_ \_ de ejemplo de secuencia de estado de canalización \_ es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="49940-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="49940-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49940-118">Requirements</span></span>



| <span data-ttu-id="49940-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49940-119">Requirement</span></span> | <span data-ttu-id="49940-120">Value</span><span class="sxs-lookup"><span data-stu-id="49940-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49940-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49940-121">Header</span></span><br/> | <dl> <span data-ttu-id="49940-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="49940-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49940-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="49940-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49940-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="49940-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="49940-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49940-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="49940-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49940-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

