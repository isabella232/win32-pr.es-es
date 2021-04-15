---
title: CD3DX12_PIPELINE_STATE_STREAM_DS estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de flujo.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649375"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a><span data-ttu-id="649ba-104">Estructura de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="649ba-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS structure</span></span>

<span data-ttu-id="649ba-105">Una estructura de aplicación auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="649ba-105">A helper structure used to describe a domain shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="649ba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="649ba-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="649ba-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="649ba-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="649ba-108">**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="649ba-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>
</dt> <dd>

<span data-ttu-id="649ba-109">Crea una nueva instancia no inicializada de un \_ flujo de estado de canalización de CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="649ba-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS.</span></span>

</dd> <dt>

<span data-ttu-id="649ba-110">**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ DS ( \_ código de bytes del sombreador de D3D12 \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="649ba-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="649ba-111">Crea una nueva instancia de un \_ flujo de estado de canalización CD3DX12 \_ \_ \_ DS, inicializado con un tipo de subobjeto de **D3D12 de \_ \_ \_ \_ tipo \_ de subobjeto de estado de canalización de** y datos de subobjeto copiados de *i*, una estructura de [**código de \_ \_ bytes del sombreador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="649ba-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="649ba-112">**Operator = (D3D12 de \_ código de bytes de sombreador \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="649ba-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="649ba-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="649ba-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="649ba-114">**operador D3D12 de \_ \_ código de bytes del sombreador () Const**</span><span class="sxs-lookup"><span data-stu-id="649ba-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="649ba-115">Conversión implícita a una estructura de [**\_ código de \_ bytes del sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="649ba-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="649ba-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="649ba-116">Remarks</span></span>

<span data-ttu-id="649ba-117">\_ \_ \_ La secuencia de estado \_ de la canalización CD3DX12 DS es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="649ba-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a><span data-ttu-id="649ba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="649ba-118">Requirements</span></span>



| <span data-ttu-id="649ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="649ba-119">Requirement</span></span> | <span data-ttu-id="649ba-120">Value</span><span class="sxs-lookup"><span data-stu-id="649ba-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="649ba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="649ba-121">Header</span></span><br/> | <dl> <span data-ttu-id="649ba-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="649ba-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649ba-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="649ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649ba-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="649ba-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="649ba-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="649ba-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="649ba-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="649ba-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

