---
title: asuint
description: Interpreta el patrón de bits de x como un entero sin signo.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984059"
---
# <a name="asuint"></a><span data-ttu-id="1a7b5-104">asuint</span><span class="sxs-lookup"><span data-stu-id="1a7b5-104">asuint</span></span>

<span data-ttu-id="1a7b5-105">Interpreta el patrón de bits de *x* como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="1a7b5-106">RET asuint (*x*)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="1a7b5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a7b5-107">Parameters</span></span>



| <span data-ttu-id="1a7b5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1a7b5-108">Item</span></span>                                                   | <span data-ttu-id="1a7b5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a7b5-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="1a7b5-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="1a7b5-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1a7b5-111">\[en \] el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1a7b5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a7b5-112">Return Value</span></span>

<span data-ttu-id="1a7b5-113">La entrada se interpreta como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="1a7b5-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="1a7b5-114">Type Description</span></span>



| <span data-ttu-id="1a7b5-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="1a7b5-115">Name</span></span>  | [<span data-ttu-id="1a7b5-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="1a7b5-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1a7b5-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="1a7b5-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="1a7b5-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1a7b5-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1a7b5-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1a7b5-119">*x*</span></span>   | <span data-ttu-id="1a7b5-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="1a7b5-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="1a7b5-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="1a7b5-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="1a7b5-122">any</span></span>                            |
| <span data-ttu-id="1a7b5-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="1a7b5-123">*ret*</span></span> | <span data-ttu-id="1a7b5-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="1a7b5-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1a7b5-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="1a7b5-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="1a7b5-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="1a7b5-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a7b5-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1a7b5-127">Minimum Shader Model</span></span>

<span data-ttu-id="1a7b5-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1a7b5-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1a7b5-129">Shader Model</span></span>                                                        | <span data-ttu-id="1a7b5-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="1a7b5-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="1a7b5-131">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="1a7b5-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="1a7b5-132">sí</span><span class="sxs-lookup"><span data-stu-id="1a7b5-132">yes</span></span>       |
| [<span data-ttu-id="1a7b5-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="1a7b5-134">no</span><span class="sxs-lookup"><span data-stu-id="1a7b5-134">no</span></span>        |
| [<span data-ttu-id="1a7b5-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="1a7b5-136">no</span><span class="sxs-lookup"><span data-stu-id="1a7b5-136">no</span></span>        |
| [<span data-ttu-id="1a7b5-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="1a7b5-138">No</span><span class="sxs-lookup"><span data-stu-id="1a7b5-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="1a7b5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a7b5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7b5-140">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1a7b5-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

