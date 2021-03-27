---
title: Tipos escalares
description: Tipos escalares
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipos escalares HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "103820882"
---
# <a name="scalar-types"></a><span data-ttu-id="8eaaa-104">Tipos escalares</span><span class="sxs-lookup"><span data-stu-id="8eaaa-104">Scalar Types</span></span>


<span data-ttu-id="8eaaa-105">HLSL admite varios tipos de datos escalares:</span><span class="sxs-lookup"><span data-stu-id="8eaaa-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="8eaaa-106">**booleano** : true o false.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="8eaaa-107">entero de bits con signo **int** -32.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="8eaaa-108">entero de tipo **uint** -32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="8eaaa-109">**DWORD** : entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="8eaaa-110">valor de punto flotante de **16 bits.**</span><span class="sxs-lookup"><span data-stu-id="8eaaa-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="8eaaa-111">Este tipo de datos solo se proporciona para la compatibilidad de lenguajes.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="8eaaa-112">Los destinos del sombreador de Direct3D 10 asignan a los tipos de datos float todos los tipos de datos de medio.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="8eaaa-113">No se puede usar un tipo de medio de datos en una variable global uniforme (use la marca/GEC si se desea esta funcionalidad).</span><span class="sxs-lookup"><span data-stu-id="8eaaa-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="8eaaa-114">valor de punto flotante de **tipo float** -32 bits.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="8eaaa-115">valor de punto flotante de **doble** 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="8eaaa-116">No se pueden usar valores de precisión doble como entradas y salidas de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="8eaaa-117">Para pasar valores de precisión doble entre los sombreadores, declare cada **Double** como un par de tipos de datos **uint** .</span><span class="sxs-lookup"><span data-stu-id="8eaaa-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="8eaaa-118">A continuación, utilice la función [**asuint**](asuint.md) para empaquetar cada **Double** en el par de **uint** s y la función [**asdouble**](asdouble.md) para desempaquetar de nuevo el par de **uint** s en el **Double**.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="8eaaa-119">A partir de Windows 8 HLSL también se admiten los tipos de datos escalares de precisión mínima.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="8eaaa-120">Los controladores de gráficos pueden implementar tipos de datos escalares de precisión mínima usando cualquier precisión mayor o igual que la precisión de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="8eaaa-121">Se recomienda no confiar en el comportamiento de compresión o ajuste que depende de la precisión subyacente específica.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="8eaaa-122">Por ejemplo, el controlador de gráficos puede ejecutar aritmética en un valor **min16float** con una precisión completa de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="8eaaa-123">**min16float** : valor de punto flotante de 16 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="8eaaa-124">**min10float** : valor de punto flotante de 10 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="8eaaa-125">**min16int** : entero de 16 bits con signo como mínimo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="8eaaa-126">**min12int** : entero de 12 bits con signo como mínimo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="8eaaa-127">**min16uint** : entero de 16 bits sin signo mínimo.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="8eaaa-128">Para obtener más información acerca de los literales escalares, vea [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="8eaaa-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8eaaa-129">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="8eaaa-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="8eaaa-130">En Direct3D 10, los siguientes tipos son modificadores para el tipo float.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="8eaaa-131"><strong>snorm Float</strong> - IEEE 32-bit signed: Float normalizado en el intervalo de 1 a 1, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="8eaaa-132"><strong>unorm Float</strong> - IEEE 32 bits sin signo: valor Float normalizado en el intervalo comprendido entre 0 y 1, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="8eaaa-133">Por ejemplo, a continuación se muestra una declaración de variable Float normalizada con signo de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="8eaaa-134">Tipo de cadena</span><span class="sxs-lookup"><span data-stu-id="8eaaa-134">String Type</span></span>

<span data-ttu-id="8eaaa-135">HLSL también admite un tipo de **cadena** , que es una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="8eaaa-136">No hay operaciones ni Estados que acepten cadenas, pero los efectos pueden consultar los parámetros de cadena y las anotaciones.</span><span class="sxs-lookup"><span data-stu-id="8eaaa-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="8eaaa-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8eaaa-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="8eaaa-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8eaaa-138">See also</span></span>



* [<span data-ttu-id="8eaaa-139">Declarar tipos escalares</span><span class="sxs-lookup"><span data-stu-id="8eaaa-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="8eaaa-140">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8eaaa-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)