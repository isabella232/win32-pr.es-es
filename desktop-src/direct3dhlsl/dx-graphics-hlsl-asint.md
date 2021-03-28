---
title: asint
description: Interpreta el patrón de bits de x como un entero.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- asint HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078142"
---
# <a name="asint"></a><span data-ttu-id="23c5a-104">asint</span><span class="sxs-lookup"><span data-stu-id="23c5a-104">asint</span></span>

<span data-ttu-id="23c5a-105">Interpreta el patrón de bits de *x* como un entero.</span><span class="sxs-lookup"><span data-stu-id="23c5a-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="23c5a-106">RET Asin (*x*)</span><span class="sxs-lookup"><span data-stu-id="23c5a-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="23c5a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23c5a-107">Parameters</span></span>



| <span data-ttu-id="23c5a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="23c5a-108">Item</span></span>                                                   | <span data-ttu-id="23c5a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="23c5a-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="23c5a-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="23c5a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="23c5a-111">\[en \] el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="23c5a-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="23c5a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23c5a-112">Return Value</span></span>

<span data-ttu-id="23c5a-113">La entrada se interpreta como un entero.</span><span class="sxs-lookup"><span data-stu-id="23c5a-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="23c5a-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="23c5a-114">Type Description</span></span>



| <span data-ttu-id="23c5a-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="23c5a-115">Name</span></span>  | [<span data-ttu-id="23c5a-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="23c5a-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="23c5a-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="23c5a-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="23c5a-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="23c5a-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="23c5a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="23c5a-119">*x*</span></span>   | <span data-ttu-id="23c5a-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="23c5a-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="23c5a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="23c5a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="23c5a-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="23c5a-122">any</span></span>                            |
| <span data-ttu-id="23c5a-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="23c5a-123">*ret*</span></span> | <span data-ttu-id="23c5a-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="23c5a-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="23c5a-125">**int**</span><span class="sxs-lookup"><span data-stu-id="23c5a-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="23c5a-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="23c5a-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23c5a-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="23c5a-127">Minimum Shader Model</span></span>

<span data-ttu-id="23c5a-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23c5a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23c5a-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="23c5a-129">Shader Model</span></span>                                                        | <span data-ttu-id="23c5a-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="23c5a-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="23c5a-131">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="23c5a-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="23c5a-132">sí</span><span class="sxs-lookup"><span data-stu-id="23c5a-132">yes</span></span>       |
| [<span data-ttu-id="23c5a-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23c5a-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="23c5a-134">no</span><span class="sxs-lookup"><span data-stu-id="23c5a-134">no</span></span>        |
| [<span data-ttu-id="23c5a-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23c5a-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="23c5a-136">no</span><span class="sxs-lookup"><span data-stu-id="23c5a-136">no</span></span>        |
| [<span data-ttu-id="23c5a-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23c5a-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="23c5a-138">No</span><span class="sxs-lookup"><span data-stu-id="23c5a-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="23c5a-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="23c5a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c5a-140">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="23c5a-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

