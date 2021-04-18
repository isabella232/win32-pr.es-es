---
title: CD3DX12_GPU_DESCRIPTOR_HANDLE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de identificador de descriptor de GPU de D3D12 \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Estructura de CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707773"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a><span data-ttu-id="1484e-104">CD3DX12 \_ \_ estructura de identificador del descriptor de GPU \_</span><span class="sxs-lookup"><span data-stu-id="1484e-104">CD3DX12\_GPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="1484e-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ identificador de descriptor de GPU de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="1484e-105">A helper structure to enable easy initialization of a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1484e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1484e-106">Syntax</span></span>


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="1484e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1484e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1484e-108">**\_Identificador de \_ descriptor de GPU CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="1484e-108">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-109">Crea una nueva instancia no inicializada de un \_ \_ identificador de descriptor de GPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-109">Creates a new, uninitialized, instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-110">**identificador de \_ descriptor de GPU de CD3DX12 explícito \_ \_ ( \_ identificador de descriptor de GPU const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="1484e-110">**explicit CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-111">Crea una nueva instancia de un \_ identificador de \_ descriptor de GPU de CD3DX12 \_ , que se inicializa con el contenido de otra estructura de [**\_ \_ \_ identificador de descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="1484e-111">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-112">**\_Identificador de \_ descriptor de GPU de CD3DX12 \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="1484e-112">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-113">Crea una nueva instancia de un \_ identificador de \_ descriptor de GPU CD3DX12 \_ , inicializado con los parámetros predeterminados (establece el puntero en cero).</span><span class="sxs-lookup"><span data-stu-id="1484e-113">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (sets the pointer to zero).</span></span>

</dd> <dt>

<span data-ttu-id="1484e-114">**\_ \_ Identificador de descriptor de GPU \_ de CD3DX12 ( \_ \_ identificador de descriptor de GPU const D3D12 \_ &otro, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-114">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-115">Crea una nueva instancia de un \_ identificador de \_ descriptor de GPU CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-115">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="1484e-116">\_Identificador de \_ descriptor de GPU D3D12 \_ &otro</span><span class="sxs-lookup"><span data-stu-id="1484e-116">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="1484e-117">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-118">**\_ \_ Identificador de descriptor de GPU \_ de CD3DX12 ( \_ \_ identificador de descriptor de GPU const D3D12 \_ &otro, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-118">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-119">Crea una nueva instancia de un \_ identificador de \_ descriptor de GPU CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-119">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="1484e-120">\_Identificador de \_ descriptor de GPU D3D12 \_ &otro</span><span class="sxs-lookup"><span data-stu-id="1484e-120">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="1484e-121">INT offsetInDescriptors: número de descriptores por los que se va a incrementar.</span><span class="sxs-lookup"><span data-stu-id="1484e-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="1484e-122">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="1484e-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-124">Establece el desplazamiento en función del número especificado de descriptores y la cantidad de incremento para cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="1484e-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="1484e-125">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-125">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-126">INT offsetInDescriptors: número de descriptores por los que se va a incrementar.</span><span class="sxs-lookup"><span data-stu-id="1484e-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="1484e-127">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="1484e-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-129">Establece el desplazamiento en función del número de incrementos especificado.</span><span class="sxs-lookup"><span data-stu-id="1484e-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="1484e-130">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-130">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-131">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-132">**operador en línea = = ( \_ en el \_ \_ identificador de descriptor de GPU const D3D12 \_ \_& otros) Const**</span><span class="sxs-lookup"><span data-stu-id="1484e-132">**inline operator==( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-133">Comprueba la igualdad entre el identificador de descriptor de GPU de CD3DX12 actual y el identificador de descriptor de GPU de \_ \_ \_ D3D12 \_ \_ o de \_ CD3DX12 GPU especificado \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-133">Tests for equality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-134">**operador insertado! = ( \_ en el \_ \_ identificador de descriptor de GPU const D3D12 \_ \_& otros) Const**</span><span class="sxs-lookup"><span data-stu-id="1484e-134">**inline operator!=( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-135">Comprueba la desigualdad entre el identificador de descriptor de GPU de CD3DX12 actual y el identificador de descriptor de GPU de \_ \_ \_ D3D12 o el identificador de \_ \_ \_ \_ \_ descriptor de GPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-135">Tests for inequality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-136">**operador = (identificador de \_ descriptor de GPU D3D12 de const \_ \_ &otro)**</span><span class="sxs-lookup"><span data-stu-id="1484e-136">**operator=(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-137">Establece el identificador del \_ descriptor de GPU de CD3DX12 actual en los mismos valores que el identificador de descriptor de GPU \_ \_ D3D12 \_ o el identificador de \_ \_ \_ \_ descriptor de GPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-137">Sets the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-138">**InitOffsetted insertado ( \_ en el \_ \_ identificador de descriptor de GPU const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-138">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-139">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con el número de elementos especificado.</span><span class="sxs-lookup"><span data-stu-id="1484e-139">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="1484e-140">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-140">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-141">\_En \_ const D3D12 \_ GPU \_ identificador de descriptor \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-141">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="1484e-142">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-143">**InitOffsetted insertado ( \_ en el \_ \_ identificador de descriptor de GPU const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-143">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-144">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="1484e-144">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="1484e-145">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-145">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-146">\_En \_ const D3D12 \_ GPU \_ identificador de descriptor \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-146">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="1484e-147">INT offsetInDescriptors: número de descriptores por los que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="1484e-148">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="1484e-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-149">**Static inline InitOffsetted ( \_ out \_ D3D12 \_ de la GPU de salida identificador \_ &identificador \_ , \_ en el \_ identificador de \_ descriptor de GPU const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-149">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-150">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="1484e-150">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="1484e-151">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-151">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-152">\_\_D3D12 identificador \_ \_ \_ de de&Scriptor de GPU de salida de salida: genera el \_ identificador de descriptor de GPU D3D12 resultante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-152">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="1484e-153">\_En \_ const D3D12 \_ GPU \_ identificador de descriptor \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-153">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="1484e-154">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="1484e-155">**Static inline InitOffsetted ( \_ out \_ D3D12 \_ GPU \_ \_ identificador &Handle, \_ in \_ const D3D12 \_ GPU \_ descriptor \_ Handle &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="1484e-155">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="1484e-156">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="1484e-156">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="1484e-157">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1484e-157">Uses the following parameters:</span></span>

<span data-ttu-id="1484e-158">\_\_D3D12 identificador \_ \_ \_ de de&Scriptor de GPU de salida de salida: genera el \_ identificador de descriptor de GPU D3D12 resultante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1484e-158">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="1484e-159">\_En \_ const D3D12 \_ GPU \_ identificador de descriptor \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-159">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="1484e-160">INT offsetInDescriptors: número de descriptores por los que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="1484e-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="1484e-161">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="1484e-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1484e-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1484e-162">Requirements</span></span>



| <span data-ttu-id="1484e-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="1484e-163">Requirement</span></span> | <span data-ttu-id="1484e-164">Value</span><span class="sxs-lookup"><span data-stu-id="1484e-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1484e-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1484e-165">Header</span></span><br/> | <dl> <span data-ttu-id="1484e-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1484e-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1484e-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="1484e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1484e-168">**\_Identificador de \_ descriptor de GPU de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1484e-168">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[<span data-ttu-id="1484e-169">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="1484e-169">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





