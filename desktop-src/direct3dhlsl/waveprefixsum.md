---
title: 'Función WavePrefixSum '
description: Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum de función HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/31/2021
ms.locfileid: "104986151"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="efaa6-104">Función WavePrefixSum </span><span class="sxs-lookup"><span data-stu-id="efaa6-104">WavePrefixSum function</span></span>

<span data-ttu-id="efaa6-105">Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este.</span><span class="sxs-lookup"><span data-stu-id="efaa6-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="efaa6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efaa6-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="efaa6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efaa6-107">Parameters</span></span>

<span data-ttu-id="efaa6-108">*value*</span><span class="sxs-lookup"><span data-stu-id="efaa6-108">*value*</span></span> 

<span data-ttu-id="efaa6-109">Valor que se va a sumar.</span><span class="sxs-lookup"><span data-stu-id="efaa6-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="efaa6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efaa6-110">Return value</span></span>

<span data-ttu-id="efaa6-111">Suma de los valores de.</span><span class="sxs-lookup"><span data-stu-id="efaa6-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="efaa6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efaa6-112">Remarks</span></span>

<span data-ttu-id="efaa6-113">No se puede garantizar el orden de las operaciones en esta rutina.</span><span class="sxs-lookup"><span data-stu-id="efaa6-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="efaa6-114">Por lo tanto, de hecho, \[ \] se omite la marca precisa dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="efaa6-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="efaa6-115">Una suma de postfijo se puede calcular agregando la suma del prefijo al valor de la calle actual.</span><span class="sxs-lookup"><span data-stu-id="efaa6-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="efaa6-116">Tenga en cuenta que la calle activa con el índice más bajo siempre recibirá un 0 para su suma de prefijo.</span><span class="sxs-lookup"><span data-stu-id="efaa6-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="efaa6-117">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="efaa6-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="efaa6-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="efaa6-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="efaa6-119">En una máquina con un tamaño de onda de 8 y todas las calles activas excepto las calles 0 y 4, los siguientes valores se devolverían desde WavePrefixSum.</span><span class="sxs-lookup"><span data-stu-id="efaa6-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="efaa6-120">Índice de Lane</span><span class="sxs-lookup"><span data-stu-id="efaa6-120">lane index</span></span> | <span data-ttu-id="efaa6-121">status</span><span class="sxs-lookup"><span data-stu-id="efaa6-121">status</span></span>   | <span data-ttu-id="efaa6-122">prefixSum</span><span class="sxs-lookup"><span data-stu-id="efaa6-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="efaa6-123">0</span><span class="sxs-lookup"><span data-stu-id="efaa6-123">0</span></span>          | <span data-ttu-id="efaa6-124">inactivo</span><span class="sxs-lookup"><span data-stu-id="efaa6-124">inactive</span></span> | <span data-ttu-id="efaa6-125">N/D</span><span class="sxs-lookup"><span data-stu-id="efaa6-125">n/a</span></span>           |
| <span data-ttu-id="efaa6-126">1</span><span class="sxs-lookup"><span data-stu-id="efaa6-126">1</span></span>          | <span data-ttu-id="efaa6-127">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-127">active</span></span>   | <span data-ttu-id="efaa6-128">= 0</span><span class="sxs-lookup"><span data-stu-id="efaa6-128">= 0</span></span>           |
| <span data-ttu-id="efaa6-129">2</span><span class="sxs-lookup"><span data-stu-id="efaa6-129">2</span></span>          | <span data-ttu-id="efaa6-130">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-130">active</span></span>   | <span data-ttu-id="efaa6-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="efaa6-131">= 0+2</span></span>         |
| <span data-ttu-id="efaa6-132">3</span><span class="sxs-lookup"><span data-stu-id="efaa6-132">3</span></span>          | <span data-ttu-id="efaa6-133">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-133">active</span></span>   | <span data-ttu-id="efaa6-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="efaa6-134">= 0+2+2</span></span>       |
| <span data-ttu-id="efaa6-135">4</span><span class="sxs-lookup"><span data-stu-id="efaa6-135">4</span></span>          | <span data-ttu-id="efaa6-136">inactivo</span><span class="sxs-lookup"><span data-stu-id="efaa6-136">inactive</span></span> | <span data-ttu-id="efaa6-137">N/D</span><span class="sxs-lookup"><span data-stu-id="efaa6-137">n/a</span></span>           |
| <span data-ttu-id="efaa6-138">5</span><span class="sxs-lookup"><span data-stu-id="efaa6-138">5</span></span>          | <span data-ttu-id="efaa6-139">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-139">active</span></span>   | <span data-ttu-id="efaa6-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="efaa6-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="efaa6-141">6</span><span class="sxs-lookup"><span data-stu-id="efaa6-141">6</span></span>          | <span data-ttu-id="efaa6-142">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-142">active</span></span>   | <span data-ttu-id="efaa6-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="efaa6-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="efaa6-144">7</span><span class="sxs-lookup"><span data-stu-id="efaa6-144">7</span></span>          | <span data-ttu-id="efaa6-145">active</span><span class="sxs-lookup"><span data-stu-id="efaa6-145">active</span></span>   | <span data-ttu-id="efaa6-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="efaa6-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="efaa6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="efaa6-147">See also</span></span>

[<span data-ttu-id="efaa6-148">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="efaa6-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="efaa6-149">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="efaa6-149">Shader Model 6</span></span>](shader-model-6-0.md)
