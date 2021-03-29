---
title: 'Función WavePrefixProduct '
description: Devuelve el producto de todos los valores de las calles activas en esta ola con índices inferiores a esta calle.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct de función HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421623"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="13726-104">Función WavePrefixProduct </span><span class="sxs-lookup"><span data-stu-id="13726-104">WavePrefixProduct function</span></span>

<span data-ttu-id="13726-105">Devuelve el producto de todos los valores de las calles activas en esta ola con índices inferiores a esta calle.</span><span class="sxs-lookup"><span data-stu-id="13726-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="13726-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13726-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="13726-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13726-107">Parameters</span></span>

<span data-ttu-id="13726-108">*value*</span><span class="sxs-lookup"><span data-stu-id="13726-108">*value*</span></span> 

<span data-ttu-id="13726-109">Valor que se va a multiplicar.</span><span class="sxs-lookup"><span data-stu-id="13726-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="13726-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13726-110">Return value</span></span>

<span data-ttu-id="13726-111">Producto de todos los valores.</span><span class="sxs-lookup"><span data-stu-id="13726-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="13726-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13726-112">Remarks</span></span>

<span data-ttu-id="13726-113">No se puede garantizar el orden de las operaciones en esta rutina.</span><span class="sxs-lookup"><span data-stu-id="13726-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="13726-114">Por lo tanto, de hecho, \[ \] se omite la marca precisa dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="13726-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="13726-115">Un producto postfijo se puede calcular multiplicando el prefijo del producto por el valor de la calle actual.</span><span class="sxs-lookup"><span data-stu-id="13726-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="13726-116">Tenga en cuenta que la calle activa con el índice más bajo siempre recibirá un 1 para su producto de prefijo.</span><span class="sxs-lookup"><span data-stu-id="13726-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="13726-117">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="13726-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="13726-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="13726-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="13726-119">En una máquina con un tamaño de onda de 8 y todas las calles activas excepto las calles 0 y 4, los siguientes valores se devolverían desde WavePrefixProduct.</span><span class="sxs-lookup"><span data-stu-id="13726-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="13726-120">Índice de Lane</span><span class="sxs-lookup"><span data-stu-id="13726-120">lane index</span></span> | <span data-ttu-id="13726-121">status</span><span class="sxs-lookup"><span data-stu-id="13726-121">status</span></span>   | <span data-ttu-id="13726-122">prefixProduct</span><span class="sxs-lookup"><span data-stu-id="13726-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="13726-123">0</span><span class="sxs-lookup"><span data-stu-id="13726-123">0</span></span>          | <span data-ttu-id="13726-124">inactivo</span><span class="sxs-lookup"><span data-stu-id="13726-124">inactive</span></span> | <span data-ttu-id="13726-125">N/D</span><span class="sxs-lookup"><span data-stu-id="13726-125">n/a</span></span>           |
| <span data-ttu-id="13726-126">1</span><span class="sxs-lookup"><span data-stu-id="13726-126">1</span></span>          | <span data-ttu-id="13726-127">active</span><span class="sxs-lookup"><span data-stu-id="13726-127">active</span></span>   | <span data-ttu-id="13726-128">= 1</span><span class="sxs-lookup"><span data-stu-id="13726-128">= 1</span></span>           |
| <span data-ttu-id="13726-129">2</span><span class="sxs-lookup"><span data-stu-id="13726-129">2</span></span>          | <span data-ttu-id="13726-130">active</span><span class="sxs-lookup"><span data-stu-id="13726-130">active</span></span>   | <span data-ttu-id="13726-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="13726-131">= 1\*2</span></span>        |
| <span data-ttu-id="13726-132">3</span><span class="sxs-lookup"><span data-stu-id="13726-132">3</span></span>          | <span data-ttu-id="13726-133">active</span><span class="sxs-lookup"><span data-stu-id="13726-133">active</span></span>   | <span data-ttu-id="13726-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="13726-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="13726-135">4</span><span class="sxs-lookup"><span data-stu-id="13726-135">4</span></span>          | <span data-ttu-id="13726-136">inactivo</span><span class="sxs-lookup"><span data-stu-id="13726-136">inactive</span></span> | <span data-ttu-id="13726-137">N/D</span><span class="sxs-lookup"><span data-stu-id="13726-137">n/a</span></span>           |
| <span data-ttu-id="13726-138">5</span><span class="sxs-lookup"><span data-stu-id="13726-138">5</span></span>          | <span data-ttu-id="13726-139">active</span><span class="sxs-lookup"><span data-stu-id="13726-139">active</span></span>   | <span data-ttu-id="13726-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="13726-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="13726-141">6</span><span class="sxs-lookup"><span data-stu-id="13726-141">6</span></span>          | <span data-ttu-id="13726-142">active</span><span class="sxs-lookup"><span data-stu-id="13726-142">active</span></span>   | <span data-ttu-id="13726-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="13726-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="13726-144">7</span><span class="sxs-lookup"><span data-stu-id="13726-144">7</span></span>          | <span data-ttu-id="13726-145">active</span><span class="sxs-lookup"><span data-stu-id="13726-145">active</span></span>   | <span data-ttu-id="13726-146">= 1 \* 2 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="13726-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="13726-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="13726-147">See also</span></span>

[<span data-ttu-id="13726-148">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="13726-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="13726-149">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="13726-149">Shader Model 6</span></span>](shader-model-6-0.md)
