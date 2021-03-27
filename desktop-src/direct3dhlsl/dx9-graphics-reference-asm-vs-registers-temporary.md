---
title: Registro temporal (HLSL VS Reference)
description: Un registro temporal del sombreador de vértices se usa para almacenar resultados intermedios.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358526"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="2196f-103">Registro temporal (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="2196f-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="2196f-104">Un registro temporal del sombreador de vértices se usa para almacenar resultados intermedios.</span><span class="sxs-lookup"><span data-stu-id="2196f-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="2196f-105">Un registro temporal debe inicializarse antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="2196f-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="2196f-106">Cada registro temporal tiene acceso de una sola escritura y de lectura triple.</span><span class="sxs-lookup"><span data-stu-id="2196f-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="2196f-107">Esto significa que una sola instrucción del sombreador puede utilizar hasta tres registros temporales como entradas.</span><span class="sxs-lookup"><span data-stu-id="2196f-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="2196f-108">No se pueden usar los valores de un registro temporal que permanecen desde las invocaciones anteriores del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="2196f-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="2196f-109">Un registro consta de propiedades que determinan el comportamiento de cada registro.</span><span class="sxs-lookup"><span data-stu-id="2196f-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="2196f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2196f-110">Property</span></span>        | <span data-ttu-id="2196f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2196f-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2196f-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="2196f-112">Name</span></span>            | <span data-ttu-id="2196f-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="2196f-113">r\[n\].</span></span> <span data-ttu-id="2196f-114">n es un número de registro opcional.</span><span class="sxs-lookup"><span data-stu-id="2196f-114">n is an optional register number.</span></span> <span data-ttu-id="2196f-115">El valor predeterminado es 0 y es el valor que se usa si no se especifica ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2196f-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="2196f-116">Count</span><span class="sxs-lookup"><span data-stu-id="2196f-116">Count</span></span>           | <span data-ttu-id="2196f-117">Un máximo de 12 registros.</span><span class="sxs-lookup"><span data-stu-id="2196f-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="2196f-118">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="2196f-118">I/O permissions</span></span> | <span data-ttu-id="2196f-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2196f-119">Read/write.</span></span> <span data-ttu-id="2196f-120">Este registro puede ser leído o escrito por la API o por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="2196f-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="2196f-121">Leer puertos</span><span class="sxs-lookup"><span data-stu-id="2196f-121">Read ports</span></span>      | <span data-ttu-id="2196f-122">El número de veces que un registro se puede leer en una sola instrucción es 3.</span><span class="sxs-lookup"><span data-stu-id="2196f-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="2196f-123">Un registro temporal es el único registro que se puede leer y escribir más de una vez en una sola instrucción.</span><span class="sxs-lookup"><span data-stu-id="2196f-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="2196f-124">Cada registro temporal tiene acceso de una sola escritura y de lectura triple.</span><span class="sxs-lookup"><span data-stu-id="2196f-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="2196f-125">Por lo tanto, una instrucción puede tener hasta tres registros temporales en su conjunto de operandos de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="2196f-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="2196f-126">No se puede usar ningún valor en un registro temporal que permanezca de las invocaciones anteriores del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="2196f-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="2196f-127">Los sombreadores de vértices que leen un valor de un registro temporal antes de escribir en él producirán un error en la llamada a la API de Direct3D para crear el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="2196f-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="2196f-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2196f-128">Example</span></span>

<span data-ttu-id="2196f-129">Este es un ejemplo de uso de un registro temporal:</span><span class="sxs-lookup"><span data-stu-id="2196f-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="2196f-130">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2196f-130">Vertex shader versions</span></span> | <span data-ttu-id="2196f-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="2196f-131">1\_1</span></span> | <span data-ttu-id="2196f-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2196f-132">2\_0</span></span> | <span data-ttu-id="2196f-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2196f-133">2\_sw</span></span> | <span data-ttu-id="2196f-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2196f-134">2\_x</span></span> | <span data-ttu-id="2196f-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2196f-135">3\_0</span></span> | <span data-ttu-id="2196f-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2196f-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="2196f-137">Registro temporal</span><span class="sxs-lookup"><span data-stu-id="2196f-137">Temporary Register</span></span>     | <span data-ttu-id="2196f-138">x</span><span class="sxs-lookup"><span data-stu-id="2196f-138">x</span></span>    | <span data-ttu-id="2196f-139">x</span><span class="sxs-lookup"><span data-stu-id="2196f-139">x</span></span>    | <span data-ttu-id="2196f-140">x</span><span class="sxs-lookup"><span data-stu-id="2196f-140">x</span></span>     | <span data-ttu-id="2196f-141">x</span><span class="sxs-lookup"><span data-stu-id="2196f-141">x</span></span>    | <span data-ttu-id="2196f-142">x</span><span class="sxs-lookup"><span data-stu-id="2196f-142">x</span></span>    | <span data-ttu-id="2196f-143">x</span><span class="sxs-lookup"><span data-stu-id="2196f-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="2196f-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2196f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2196f-145">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2196f-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




