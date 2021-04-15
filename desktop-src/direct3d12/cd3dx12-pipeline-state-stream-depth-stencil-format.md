---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir el formato de estarcido de profundidad como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649379"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="5004b-104">\_Estructura de flujo de estado de canalización de CD3DX12 \_ estructura de \_ \_ \_ formato de estarcido \_</span><span class="sxs-lookup"><span data-stu-id="5004b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="5004b-105">Una estructura de aplicación auxiliar que se usa para describir el formato de estarcido de profundidad como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5004b-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5004b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5004b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="5004b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5004b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5004b-108">**\_Formato de \_ \_ estarcido de profundidad de flujo de estado de \_ \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="5004b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="5004b-109">Crea una nueva instancia no inicializada de un \_ formato de estarcido de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5004b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="5004b-110">**Formato de la \_ Galería de símbolos de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ \_ (formato de DXGI \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="5004b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="5004b-111">Crea una nueva instancia de un \_ formato de estarcido de profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ \_ , inicializado con un tipo de subobjeto de **\_ \_ tipo subobjeto de estado de canalización D3D12 \_ formato de \_ \_ \_ estarcido \_ de profundidad** y datos de subobjeto copiados de *i*, una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="5004b-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="5004b-112">**Operator = (formato de DXGI \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="5004b-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="5004b-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="5004b-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="5004b-114">**Operator DXGI \_ Format () Const**</span><span class="sxs-lookup"><span data-stu-id="5004b-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="5004b-115">Conversión implícita a una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="5004b-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5004b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5004b-116">Remarks</span></span>

<span data-ttu-id="5004b-117">\_ \_ \_ \_ \_ \_ El formato de la galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 es una especialización de TYPEDEF de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define como sigue:</span><span class="sxs-lookup"><span data-stu-id="5004b-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="5004b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5004b-118">Requirements</span></span>



| <span data-ttu-id="5004b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5004b-119">Requirement</span></span> | <span data-ttu-id="5004b-120">Value</span><span class="sxs-lookup"><span data-stu-id="5004b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5004b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5004b-121">Header</span></span><br/> | <dl> <span data-ttu-id="5004b-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5004b-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5004b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5004b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5004b-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="5004b-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5004b-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5004b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="5004b-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5004b-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

