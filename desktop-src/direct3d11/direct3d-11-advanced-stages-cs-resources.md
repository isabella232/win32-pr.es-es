---
title: Nuevos tipos de recursos
description: Se han agregado varios tipos de recursos nuevos en Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Búfer de direcciones de byte (Introducción)
- Búfer de lectura/escritura (Introducción)
- Búfer estructurado (información general)
- Búfer de acceso desordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421049"
---
# <a name="new-resource-types"></a><span data-ttu-id="88371-107">Nuevos tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="88371-107">New Resource Types</span></span>

<span data-ttu-id="88371-108">Se han agregado varios tipos de recursos nuevos en Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="88371-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="88371-109">Búferes y texturas de lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="88371-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="88371-110">Búfer estructurado</span><span class="sxs-lookup"><span data-stu-id="88371-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="88371-111">Búfer de direcciones de bytes</span><span class="sxs-lookup"><span data-stu-id="88371-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="88371-112">Búfer o textura de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="88371-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="88371-113">Anexar y consumir búfer</span><span class="sxs-lookup"><span data-stu-id="88371-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="88371-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88371-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="88371-115">Búferes y texturas de lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="88371-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="88371-116">Los recursos del modelo de sombreador 4 son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="88371-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="88371-117">El modelo de sombreador 5 implementa un nuevo conjunto correspondiente de recursos de lectura y escritura:</span><span class="sxs-lookup"><span data-stu-id="88371-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="88371-118">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="88371-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="88371-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="88371-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="88371-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="88371-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="88371-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="88371-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="88371-122">Estos recursos requieren una variable de recurso para tener acceso a la memoria (a través de la indización), ya que no hay ningún método para tener acceso a la memoria directamente.</span><span class="sxs-lookup"><span data-stu-id="88371-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="88371-123">Se puede utilizar una variable de recurso en los lados izquierdo y derecho de una ecuación; Si se utiliza en el lado derecho, el tipo de plantilla debe ser un único componente (float, int o uint).</span><span class="sxs-lookup"><span data-stu-id="88371-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="88371-124">Búfer estructurado</span><span class="sxs-lookup"><span data-stu-id="88371-124">Structured Buffer</span></span>

<span data-ttu-id="88371-125">Un búfer estructurado es un búfer que contiene elementos de igual tamaño.</span><span class="sxs-lookup"><span data-stu-id="88371-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="88371-126">Use una estructura con uno o varios tipos de miembro para definir un elemento.</span><span class="sxs-lookup"><span data-stu-id="88371-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="88371-127">Esta es una estructura con tres miembros.</span><span class="sxs-lookup"><span data-stu-id="88371-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="88371-128">Use esta estructura para declarar un búfer estructurado como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="88371-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="88371-129">Además de la indización, un búfer estructurado admite el acceso a un solo miembro como este:</span><span class="sxs-lookup"><span data-stu-id="88371-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="88371-130">Use los siguientes tipos de objeto para tener acceso a un búfer estructurado:</span><span class="sxs-lookup"><span data-stu-id="88371-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="88371-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) es un búfer estructurado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="88371-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="88371-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) es un búfer estructurado de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="88371-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="88371-133">[Las funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementan operaciones de interbloqueos se permiten en los elementos int y uint de un **RWStructuredBuffer**.</span><span class="sxs-lookup"><span data-stu-id="88371-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="88371-134">Búfer de direcciones de bytes</span><span class="sxs-lookup"><span data-stu-id="88371-134">Byte Address Buffer</span></span>

<span data-ttu-id="88371-135">Un búfer de direcciones de bytes es un búfer cuyo contenido es direccionable por un desplazamiento de bytes.</span><span class="sxs-lookup"><span data-stu-id="88371-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="88371-136">Normalmente, el contenido de un [búfer](overviews-direct3d-11-resources-buffers-intro.md) se indexa por elemento mediante un intervalo para cada elemento (s) y el número de elemento (N) según lo especificado por S \* N.</span><span class="sxs-lookup"><span data-stu-id="88371-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="88371-137">Un búfer de direcciones de bytes, que también se puede llamar búfer sin formato, utiliza un desplazamiento de valor de bytes desde el principio del búfer para obtener acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="88371-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="88371-138">El valor de byte debe ser un múltiplo de cuatro para que esté alineado con DWORD.</span><span class="sxs-lookup"><span data-stu-id="88371-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="88371-139">Si se proporciona cualquier otro valor, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="88371-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="88371-140">El modelo de sombreador 5 presenta objetos para obtener acceso a un [búfer de direcciones de bytes de solo lectura](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) , así como a un [búfer de direcciones de bytes de lectura y escritura](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span><span class="sxs-lookup"><span data-stu-id="88371-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="88371-141">El contenido de un búfer de direcciones de bytes está diseñado para ser un entero sin signo de 32 bits. Si el valor del búfer no es realmente un entero sin signo, use una función como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para leerlo.</span><span class="sxs-lookup"><span data-stu-id="88371-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="88371-142">Búfer o textura de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="88371-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="88371-143">Un recurso de acceso desordenado (que incluye búferes, texturas y matrices de texturas, sin muestreo múltiple), permite el acceso de lectura y escritura desordenado temporal desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="88371-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="88371-144">Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria a través del uso de [funciones atómicas](direct3d-11-advanced-stages-cs-atomic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="88371-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="88371-145">Cree un búfer de acceso desordenado o una textura llamando a una función como [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) y pasando la marca **de \_ \_ \_ acceso desordenado de D3D11 enlace** desde la enumeración de [**\_ \_ marca de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="88371-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="88371-146">Los recursos de acceso desordenados solo se pueden enlazar a los sombreadores de píxeles y los sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="88371-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="88371-147">Durante la ejecución, los sombreadores de píxeles o los sombreadores de cálculo que se ejecutan en paralelo tienen los mismos recursos de acceso desordenados enlazados.</span><span class="sxs-lookup"><span data-stu-id="88371-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="88371-148">Anexar y consumir búfer</span><span class="sxs-lookup"><span data-stu-id="88371-148">Append and Consume Buffer</span></span>

<span data-ttu-id="88371-149">Un búfer Append y consume es un tipo especial de recurso no ordenado que permite agregar y quitar valores del final de un búfer de forma similar a como funciona una pila.</span><span class="sxs-lookup"><span data-stu-id="88371-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="88371-150">Un búfer de anexión y consumo debe ser un búfer estructurado:</span><span class="sxs-lookup"><span data-stu-id="88371-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="88371-151">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="88371-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="88371-152">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="88371-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="88371-153">Usar estos recursos a través de sus métodos, estos recursos no usan variables de recursos.</span><span class="sxs-lookup"><span data-stu-id="88371-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88371-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88371-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88371-155">Información general del sombreador de cálculo</span><span class="sxs-lookup"><span data-stu-id="88371-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 