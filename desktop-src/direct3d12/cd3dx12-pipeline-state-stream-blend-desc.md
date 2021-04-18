---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una descripción de Blend como un solo objeto adecuado para una descripción de flujo.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698197"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="9cb6a-104">CD3DX12 de \_ canalización de estado de canalización de flujo de la \_ \_ \_ \_ estructura DESC</span><span class="sxs-lookup"><span data-stu-id="9cb6a-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="9cb6a-105">Una estructura de aplicación auxiliar que se usa para describir una descripción de Blend como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="9cb6a-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb6a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cb6a-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="9cb6a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9cb6a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9cb6a-108">**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="9cb6a-109">Crea una instancia nueva, sin inicializar, de una \_ Descripción de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9cb6a-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="9cb6a-110">**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC (CD3DX12 \_ Blend \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="9cb6a-111">Crea una nueva instancia de un \_ flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC, inicializada con un tipo de subobjeto de **D3D12 de tipo de \_ \_ subobjeto de estado de canalización de \_ \_ \_ mezcla** y datos de subobjeto copiados de *i*, una estructura de [**DESC de CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb6a-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9cb6a-112">**Operator = (CD3DX12 \_ Blend \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="9cb6a-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="9cb6a-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="9cb6a-114">**Operator CD3DX12 \_ Blend \_ DESC () Const**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="9cb6a-115">Conversión implícita a una [**estructura \_ \_ DESC de CD3DX12 Blend**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb6a-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cb6a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cb6a-116">Remarks</span></span>

<span data-ttu-id="9cb6a-117">\_ \_ La secuencia de estado de canalización CD3DX12 \_ \_ Blend \_ es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9cb6a-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="9cb6a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cb6a-118">Requirements</span></span>



| <span data-ttu-id="9cb6a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cb6a-119">Requirement</span></span> | <span data-ttu-id="9cb6a-120">Value</span><span class="sxs-lookup"><span data-stu-id="9cb6a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb6a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cb6a-121">Header</span></span><br/> | <dl> <span data-ttu-id="9cb6a-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cb6a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cb6a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cb6a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb6a-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="9cb6a-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9cb6a-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="9cb6a-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cb6a-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

