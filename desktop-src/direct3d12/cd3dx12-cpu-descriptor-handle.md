---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de identificador de descriptor de CPU de D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Estructura de CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649388"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a><span data-ttu-id="c464b-104">CD3DX12 \_ \_ estructura de identificador de descriptor de CPU \_</span><span class="sxs-lookup"><span data-stu-id="c464b-104">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="c464b-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ identificador de descriptor de CPU de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="c464b-105">A helper structure to enable easy initialization of a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c464b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c464b-106">Syntax</span></span>


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="c464b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c464b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c464b-108">**\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c464b-108">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-109">Crea una nueva instancia no inicializada de un \_ \_ identificador de descriptor de CPU de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-109">Creates a new, uninitialized, instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-110">**identificador de \_ descriptor de CPU de CD3DX12 explícito \_ \_ (const D3D12 \_ \_ identificador del descriptor de CPU \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="c464b-110">**explicit CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-111">Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializado con el contenido de otra estructura de [**\_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="c464b-111">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-112">**\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ( \_ valor predeterminado de CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="c464b-112">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-113">Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializado con los parámetros predeterminados (puntero establecido en cero).</span><span class="sxs-lookup"><span data-stu-id="c464b-113">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (pointer set to zero).</span></span>

</dd> <dt>

<span data-ttu-id="c464b-114">**\_ \_ Identificador de descriptor de CPU de CD3DX12 \_ ( \_ \_ identificador de descriptor de CPU const D3D12 \_ &otro, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-114">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-115">Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-115">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="c464b-116">D3D12 \_ \_ identificador de descriptor de CPU \_ &otro</span><span class="sxs-lookup"><span data-stu-id="c464b-116">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="c464b-117">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-118">**\_ \_ Identificador de descriptor de CPU de CD3DX12 \_ ( \_ \_ identificador de descriptor de CPU const D3D12 \_ &otro, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-118">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-119">Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-119">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="c464b-120">D3D12 \_ \_ identificador de descriptor de CPU \_ &otro</span><span class="sxs-lookup"><span data-stu-id="c464b-120">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="c464b-121">INT offsetInDescriptors: número de descriptores por los que se va a incrementar.</span><span class="sxs-lookup"><span data-stu-id="c464b-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="c464b-122">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="c464b-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-124">Establece el desplazamiento en función del número especificado de descriptores y la cantidad de incremento para cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="c464b-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="c464b-125">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-125">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-126">INT offsetInDescriptors: número de descriptores por los que se va a incrementar.</span><span class="sxs-lookup"><span data-stu-id="c464b-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="c464b-127">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="c464b-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-129">Establece el desplazamiento en función del número de incrementos especificado.</span><span class="sxs-lookup"><span data-stu-id="c464b-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="c464b-130">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-130">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-131">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-132">**operador = = ( \_ en el \_ \_ identificador de descriptor de CPU const D3D12 \_ \_& otros) Const**</span><span class="sxs-lookup"><span data-stu-id="c464b-132">**operator==( \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-133">Comprueba la igualdad entre el identificador del \_ descriptor de la CPU de CD3DX12 actual \_ y el identificador de \_ descriptor de CPU D3D12 especificado o el identificador del descriptor \_ \_ \_ de \_ CPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-133">Tests for equality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-134">**operador! = ( \_ en el \_ \_ identificador de descriptor de CPU const D3D12 \_ \_& otros) Const**</span><span class="sxs-lookup"><span data-stu-id="c464b-134">**operator!=(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-135">Comprueba la desigualdad entre el identificador del descriptor de la CPU de CD3DX12 actual \_ \_ \_ y el identificador del descriptor de CPU de D3D12 o el identificador del descriptor de la \_ \_ \_ \_ CPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-135">Tests for inequality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-136">**Operator = (const D3D12 \_ \_ identificador del descriptor de CPU \_ &otro)**</span><span class="sxs-lookup"><span data-stu-id="c464b-136">**operator=(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-137">Establece el identificador del \_ descriptor de la CPU de CD3DX12 actual \_ \_ en los mismos valores que el identificador de descriptor de CPU D3D12 especificado o el identificador del descriptor \_ \_ \_ de \_ CPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-137">Sets the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-138">**InitOffsetted en línea ( \_ en \_ const D3D12 \_ \_ identificador del descriptor de CPU \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-138">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-139">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con el número de elementos especificado.</span><span class="sxs-lookup"><span data-stu-id="c464b-139">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="c464b-140">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-140">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-141">\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-141">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="c464b-142">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-143">**InitOffsetted en línea ( \_ en \_ const D3D12 \_ \_ identificador del descriptor de CPU \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-143">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-144">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="c464b-144">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="c464b-145">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-145">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-146">\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-146">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="c464b-147">INT offsetInDescriptors: número de descriptores por los que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="c464b-148">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="c464b-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-149">**Static inline InitOffsetted ( \_ salida \_ D3D12 \_ identificador \_ de descriptor \_ de CPU &identificador, \_ en \_ const D3D12 \_ CPU \_ \_ handler &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-149">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-150">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="c464b-150">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="c464b-151">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-151">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-152">\_Out \_ \_ &identificador \_ de descriptor de CPU D3D12 \_ : genera \_ el \_ identificador de descriptor de CPU D3D12 resultante \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-152">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="c464b-153">\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-153">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="c464b-154">INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="c464b-155">**Static inline InitOffsetted ( \_ salida \_ D3D12 \_ identificador \_ de descriptor \_ de CPU &identificador, \_ en \_ const D3D12 \_ CPU \_ \_ handler &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="c464b-155">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="c464b-156">Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado.</span><span class="sxs-lookup"><span data-stu-id="c464b-156">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="c464b-157">Usa los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c464b-157">Uses the following parameters:</span></span>

<span data-ttu-id="c464b-158">\_Out \_ \_ &identificador \_ de descriptor de CPU D3D12 \_ : genera \_ el \_ identificador de descriptor de CPU D3D12 resultante \_ .</span><span class="sxs-lookup"><span data-stu-id="c464b-158">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="c464b-159">\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-159">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="c464b-160">INT offsetInDescriptors: número de descriptores por los que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="c464b-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="c464b-161">UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.</span><span class="sxs-lookup"><span data-stu-id="c464b-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c464b-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c464b-162">Requirements</span></span>



| <span data-ttu-id="c464b-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="c464b-163">Requirement</span></span> | <span data-ttu-id="c464b-164">Value</span><span class="sxs-lookup"><span data-stu-id="c464b-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c464b-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c464b-165">Header</span></span><br/> | <dl> <span data-ttu-id="c464b-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c464b-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c464b-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="c464b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c464b-168">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="c464b-168">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





