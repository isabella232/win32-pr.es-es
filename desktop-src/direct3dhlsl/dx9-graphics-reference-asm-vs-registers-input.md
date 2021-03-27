---
title: Registro de entrada
description: Registro de entrada
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994372"
---
# <a name="input-register"></a><span data-ttu-id="4906b-103">Registro de entrada</span><span class="sxs-lookup"><span data-stu-id="4906b-103">Input Register</span></span>

<span data-ttu-id="4906b-104">Registro de entrada del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="4906b-104">Vertex shader input register.</span></span>

<span data-ttu-id="4906b-105">Los datos de cada vértice (mediante uno o varios flujos de vértices de entrada) se cargan en los registros de entrada de vértices antes de que se ejecute el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="4906b-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="4906b-106">Los registros de entrada constan de vectores de punto flotante de componente 16 4, designados como V0 a través de V15.</span><span class="sxs-lookup"><span data-stu-id="4906b-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="4906b-107">Estos registros son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4906b-107">These registers are read-only.</span></span> <span data-ttu-id="4906b-108">Un registro de entrada se enlaza a los datos de vértice a través de una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="4906b-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="4906b-109">Las siguientes propiedades de registro controlan el comportamiento de cada registro:</span><span class="sxs-lookup"><span data-stu-id="4906b-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="4906b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4906b-110">Property</span></span>        | <span data-ttu-id="4906b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4906b-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4906b-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="4906b-112">Name</span></span>            | <span data-ttu-id="4906b-113">v \[ n \] -n es un número de registro opcional.</span><span class="sxs-lookup"><span data-stu-id="4906b-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="4906b-114">0 es el valor predeterminado que se usa, si se omite.</span><span class="sxs-lookup"><span data-stu-id="4906b-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="4906b-115">Count</span><span class="sxs-lookup"><span data-stu-id="4906b-115">Count</span></span>           | <span data-ttu-id="4906b-116">Un máximo de 16 registros, V0-V15.</span><span class="sxs-lookup"><span data-stu-id="4906b-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="4906b-117">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="4906b-117">I/O permissions</span></span> | <span data-ttu-id="4906b-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4906b-118">Read-only.</span></span> <span data-ttu-id="4906b-119">Este registro no se puede escribir en la API o en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4906b-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="4906b-120">Leer puertos</span><span class="sxs-lookup"><span data-stu-id="4906b-120">Read ports</span></span>      | <span data-ttu-id="4906b-121">1. este es el número de veces que se puede leer un registro dentro de una única instrucción.</span><span class="sxs-lookup"><span data-stu-id="4906b-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="4906b-122">Vea a continuación.</span><span class="sxs-lookup"><span data-stu-id="4906b-122">See below.</span></span> |



 

<span data-ttu-id="4906b-123">Cualquier instrucción única solo puede tener acceso a un registro de entrada de vértice.</span><span class="sxs-lookup"><span data-stu-id="4906b-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="4906b-124">Sin embargo, cada origen de la instrucción puede swizzle de forma independiente y negar ese vector a medida que se lee.</span><span class="sxs-lookup"><span data-stu-id="4906b-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="4906b-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4906b-125">Example</span></span>

<span data-ttu-id="4906b-126">Este es un ejemplo de uso de una declaración de vértice para enlazar datos de posición de vértice 2D para registrar v0.</span><span class="sxs-lookup"><span data-stu-id="4906b-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="4906b-127">La declaración de vértices pertenece a la aplicación:</span><span class="sxs-lookup"><span data-stu-id="4906b-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="4906b-128">Esta es la declaración del sombreador de vértices correspondiente:</span><span class="sxs-lookup"><span data-stu-id="4906b-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="4906b-129">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4906b-129">Vertex shader versions</span></span> | <span data-ttu-id="4906b-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="4906b-130">1\_1</span></span> | <span data-ttu-id="4906b-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4906b-131">2\_0</span></span> | <span data-ttu-id="4906b-132">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4906b-132">2\_sw</span></span> | <span data-ttu-id="4906b-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4906b-133">2\_x</span></span> | <span data-ttu-id="4906b-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4906b-134">3\_0</span></span> | <span data-ttu-id="4906b-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4906b-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="4906b-136">Registro de posición</span><span class="sxs-lookup"><span data-stu-id="4906b-136">Position Register</span></span>      | <span data-ttu-id="4906b-137">x</span><span class="sxs-lookup"><span data-stu-id="4906b-137">x</span></span>    | <span data-ttu-id="4906b-138">x</span><span class="sxs-lookup"><span data-stu-id="4906b-138">x</span></span>    | <span data-ttu-id="4906b-139">x</span><span class="sxs-lookup"><span data-stu-id="4906b-139">x</span></span>     | <span data-ttu-id="4906b-140">x</span><span class="sxs-lookup"><span data-stu-id="4906b-140">x</span></span>    | <span data-ttu-id="4906b-141">x</span><span class="sxs-lookup"><span data-stu-id="4906b-141">x</span></span>    | <span data-ttu-id="4906b-142">x</span><span class="sxs-lookup"><span data-stu-id="4906b-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4906b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4906b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4906b-144">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4906b-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




