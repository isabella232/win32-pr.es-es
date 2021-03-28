---
title: Tipo de búfer
description: Use la siguiente sintaxis para declarar una variable de búfer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo de búfer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077952"
---
# <a name="buffer-type"></a><span data-ttu-id="85191-104">Tipo de búfer</span><span class="sxs-lookup"><span data-stu-id="85191-104">Buffer Type</span></span>

<span data-ttu-id="85191-105">Use la siguiente sintaxis para declarar una variable de búfer.</span><span class="sxs-lookup"><span data-stu-id="85191-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="85191-106">Nombre de *tipo* de<de búfer >  ;</span><span class="sxs-lookup"><span data-stu-id="85191-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="85191-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85191-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85191-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Búfer**</span><span class="sxs-lookup"><span data-stu-id="85191-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="85191-109">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="85191-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="85191-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Automáticamente*</span><span class="sxs-lookup"><span data-stu-id="85191-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="85191-111">Uno de los tipos de tipo HLSL [escalar](dx-graphics-hlsl-scalar.md), [Vector](dx-graphics-hlsl-vector.md)y some [Matrix](dx-graphics-hlsl-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="85191-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="85191-112">Puede declarar una variable de búfer con una matriz siempre y cuando quepa en cantidades de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85191-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="85191-113">Por lo tanto, puede escribir `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="85191-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="85191-114">Pero `Buffer<float4x4>` es demasiado grande y el compilador generará un error.</span><span class="sxs-lookup"><span data-stu-id="85191-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="85191-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="85191-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="85191-116">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="85191-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="85191-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85191-117">Example</span></span>

<span data-ttu-id="85191-118">Este es un ejemplo de una declaración de búfer del archivo PipesGS. FX en el [ejemplo PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="85191-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="85191-119">Los datos se leen desde un búfer mediante una versión sobrecargada de la función de [**carga**](dx-graphics-hlsl-to-load.md) intrínseca de HLSL que toma un parámetro de entrada (un índice de entero).</span><span class="sxs-lookup"><span data-stu-id="85191-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="85191-120">Se tiene acceso a un búfer como una matriz de elementos; por lo tanto, en este ejemplo se lee el segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="85191-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="85191-121">Use la [fase Stream-Output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) para enviar datos a un búfer.</span><span class="sxs-lookup"><span data-stu-id="85191-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="85191-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="85191-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85191-123">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85191-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 