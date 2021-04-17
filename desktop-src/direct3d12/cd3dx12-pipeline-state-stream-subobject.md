---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT estructura (D3dx12. h)
description: Estructura de aplicación auxiliar con plantilla utilizada para encapsular los pares de datos de tipo de subobjeto y subobjeto como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718502"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="098ed-104">\_Estructura de \_ \_ subobjeto de flujo de estado de canalización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="098ed-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="098ed-105">Estructura de aplicación auxiliar con plantilla utilizada para encapsular los pares de datos de tipo de subobjeto y subobjeto como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="098ed-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="098ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="098ed-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="098ed-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="098ed-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="098ed-108">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="098ed-109">Crea una nueva instancia no inicializada de un subobjeto de \_ flujo de estado de la canalización CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="098ed-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="098ed-110">**CD3DX12 \_ Subobjeto de flujo de estado de CANALización \_ \_ \_ (** InnerStructType \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="098ed-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="098ed-111">Crea una nueva \_ \_ \_ \_ instancia de plantilla de subobjeto de flujo de estado de canalización CD3DX12, inicializada con un tipo de subobjeto de [**\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) y datos de subobjeto copiados de *i*.</span><span class="sxs-lookup"><span data-stu-id="098ed-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="098ed-112">Tanto el tipo de subobjeto como el tipo de datos del subobjeto se proporcionan como parámetros de plantilla, **Type** y **InnerStructType**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="098ed-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="098ed-113">Para obtener más información, vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="098ed-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="098ed-114">**Operator = (** InnerStructType \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="098ed-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="098ed-115">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="098ed-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="098ed-116">**operador **InnerStructType**() Const**</span><span class="sxs-lookup"><span data-stu-id="098ed-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="098ed-117">Conversión implícita al tipo de datos de subobjeto proporcionado por el parámetro de plantilla **InnerStructType** .</span><span class="sxs-lookup"><span data-stu-id="098ed-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="098ed-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="098ed-118">Remarks</span></span>

<span data-ttu-id="098ed-119">\_ \_ \_ El subobjeto de flujo de estado de canalización CD3DX12 \_ es una plantilla definida como sigue:</span><span class="sxs-lookup"><span data-stu-id="098ed-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



<span data-ttu-id="098ed-120">El parámetro de plantilla **InnerStructType** especifica el tipo de datos del subobjeto; es decir, los detalles del subobjeto que se van a codificar en un flujo.</span><span class="sxs-lookup"><span data-stu-id="098ed-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="098ed-121">El **tipo** de parámetro de plantilla especifica el tipo de subobjeto; es decir, el tipo de la estructura especificada por el parámetro de plantilla **InnerStructType**.</span><span class="sxs-lookup"><span data-stu-id="098ed-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="098ed-122">El parámetro de plantilla **defaultarg (** especifica un valor opcional en el que se inicializarán los datos del subobjeto cuando una instancia de la creación de instancias de plantilla correspondiente esté construida de forma predeterminada; por ejemplo, para construir el valor predeterminado de una [**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) inicializada con los valores predeterminados de estado de combinación comunes mediante [**CD3DX12 \_ predeterminado**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="098ed-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="098ed-123">Estas son las instancias de plantilla definidas:</span><span class="sxs-lookup"><span data-stu-id="098ed-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="098ed-124">**\_Marcas de \_ flujo de estado de CANALización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="098ed-125">**CD3DX12 \_ \_ máscara de \_ nodo de flujo de estado de \_ canalización \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="098ed-126">**\_ \_ \_ \_ Firma raíz de la secuencia de estado de canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="098ed-127">**\_Diseño de \_ \_ entrada de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="098ed-128">**Flujo de estado de canalización de CD3DX12 de \_ Estado de canalización \_ \_ \_ IB \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="098ed-129">**\_ \_ \_ Topología primitiva de flujo de estado \_ de canalización de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="098ed-130">**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ frente a**</span><span class="sxs-lookup"><span data-stu-id="098ed-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="098ed-131">**\_Flujo de estado de canalización \_ \_ \_ GS de CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="098ed-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="098ed-132">**\_Salida de \_ \_ flujo de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="098ed-133">**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ hs**</span><span class="sxs-lookup"><span data-stu-id="098ed-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="098ed-134">**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="098ed-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="098ed-135">**\_Flujo de estado de canalización CD3DX12 \_ \_ \_ PS**</span><span class="sxs-lookup"><span data-stu-id="098ed-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="098ed-136">**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ CS**</span><span class="sxs-lookup"><span data-stu-id="098ed-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="098ed-137">**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="098ed-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="098ed-138">**\_Galería de \_ \_ símbolos de profundidad de flujo de estado de \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="098ed-139">**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="098ed-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="098ed-140">**\_Formato de \_ \_ estarcido de profundidad de flujo de estado de \_ \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="098ed-141">**\_ \_ \_ Rasterizador de flujo de estado de CANALización de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="098ed-142">**\_Formatos de \_ \_ destino de representación de secuencia de estado de \_ \_ canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="098ed-143">**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="098ed-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="098ed-144">**\_Máscara de \_ \_ ejemplo de flujo de estado de canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="098ed-145">**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO**</span><span class="sxs-lookup"><span data-stu-id="098ed-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="098ed-146">Las estructuras de flujo de estado de canalización de CD3DX12 de la secuencia de estado de canalización de CD3DX12, la de profundidad de flujo de estado de canalización de CD3DX12 y de canalización de flujo se definen para inicializar sus datos de subobjeto con valores predeterminados comunes mediante el [**\_ valor predeterminado de CD3DX12**](cd3dx12-default.md). [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-blend-desc.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**\_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md) [**\_ \_ \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md)</span><span class="sxs-lookup"><span data-stu-id="098ed-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="098ed-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="098ed-147">Requirements</span></span>



| <span data-ttu-id="098ed-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="098ed-148">Requirement</span></span> | <span data-ttu-id="098ed-149">Value</span><span class="sxs-lookup"><span data-stu-id="098ed-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="098ed-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="098ed-150">Header</span></span><br/> | <dl> <span data-ttu-id="098ed-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="098ed-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098ed-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="098ed-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098ed-153">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="098ed-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="098ed-154">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098ed-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

