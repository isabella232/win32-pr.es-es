---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un diseño de entrada como un solo objeto adecuado para una descripción de flujo.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653270"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="d7673-104">\_Estructura de \_ \_ diseño de entrada de flujo de estado de \_ canalización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="d7673-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="d7673-105">Una estructura de aplicación auxiliar que se usa para describir un diseño de entrada como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="d7673-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7673-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7673-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="d7673-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7673-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7673-108">**\_Diseño de \_ \_ entrada de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d7673-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="d7673-109">Crea una nueva instancia no inicializada de un \_ diseño de entrada de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d7673-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="d7673-110">**\_Diseño de entrada de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (D3D12 de diseño de \_ entrada \_ \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="d7673-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="d7673-111">Crea una nueva instancia de un \_ diseño de entrada de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **\_ \_ \_ \_ tipo \_ \_ de subobjeto de estado de canalización de D3D12** y datos de subobjeto copiados de *i*, una estructura de DESC de [**diseño de entrada de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="d7673-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7673-112">**Operator = (D3D12 de diseño de entrada de la \_ \_ \_ descripción const const& i)**</span><span class="sxs-lookup"><span data-stu-id="d7673-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="d7673-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="d7673-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="d7673-114">**operador de \_ presentación de entrada D3D12 \_ \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="d7673-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="d7673-115">Conversión implícita a una [**estructura \_ \_ \_ DESC de diseño de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="d7673-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7673-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7673-116">Remarks</span></span>

<span data-ttu-id="d7673-117">\_ \_ \_ \_ \_ El diseño de entrada de flujo de estado de canalización CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d7673-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="d7673-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7673-118">Requirements</span></span>



| <span data-ttu-id="d7673-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7673-119">Requirement</span></span> | <span data-ttu-id="d7673-120">Value</span><span class="sxs-lookup"><span data-stu-id="d7673-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7673-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7673-121">Header</span></span><br/> | <dl> <span data-ttu-id="d7673-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7673-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7673-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7673-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7673-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="d7673-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d7673-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d7673-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="d7673-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d7673-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

