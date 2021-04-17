---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una descripción de ejemplo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698407"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="ca996-104">\_Estructura de \_ \_ ejemplo de flujo de estado de canalización CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ca996-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="ca996-105">Una estructura de aplicación auxiliar que se usa para describir una descripción de ejemplo como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="ca996-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca996-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca996-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="ca996-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca996-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca996-108">**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="ca996-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="ca996-109">Crea una instancia nueva, no inicializada, de una \_ secuencia de estado de canalización de CD3DX12 \_ \_ \_ ejemplo \_ desc.</span><span class="sxs-lookup"><span data-stu-id="ca996-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ca996-110">**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC (ejemplo de DXGI, \_ \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="ca996-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="ca996-111">Crea una nueva instancia de una \_ secuencia de estado de canalización de CD3DX12 \_ \_ \_ ejemplo \_ DESC, inicializada con un tipo de subobjeto de **Estado de canalización D3D12 de \_ \_ \_ \_ \_ ejemplo \_ DESC** y datos de subobjeto copiados de *i*, una estructura de [**\_ \_ DESC de ejemplo de DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="ca996-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ca996-112">**Operator = (ejemplo de DXGI \_ \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="ca996-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="ca996-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="ca996-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="ca996-114">**Operator DXGI \_ Sample \_ DESC () Const**</span><span class="sxs-lookup"><span data-stu-id="ca996-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="ca996-115">Conversión implícita a una [**estructura \_ \_ DESC de ejemplo de DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="ca996-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca996-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca996-116">Remarks</span></span>

<span data-ttu-id="ca996-117">\_ \_ \_ El flujo de ejemplo de estado de canalización CD3DX12 \_ \_ DESC es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca996-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="ca996-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca996-118">Requirements</span></span>



| <span data-ttu-id="ca996-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca996-119">Requirement</span></span> | <span data-ttu-id="ca996-120">Value</span><span class="sxs-lookup"><span data-stu-id="ca996-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca996-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca996-121">Header</span></span><br/> | <dl> <span data-ttu-id="ca996-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca996-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca996-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca996-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca996-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="ca996-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ca996-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ca996-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="ca996-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ca996-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

