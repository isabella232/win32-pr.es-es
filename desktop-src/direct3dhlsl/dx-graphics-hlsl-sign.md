---
title: sign
description: Devuelve el signo de x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- firmar HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997149"
---
# <a name="sign"></a><span data-ttu-id="958c4-104">sign</span><span class="sxs-lookup"><span data-stu-id="958c4-104">sign</span></span>

<span data-ttu-id="958c4-105">Devuelve el signo de *x*.</span><span class="sxs-lookup"><span data-stu-id="958c4-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="958c4-106">señal *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="958c4-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="958c4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="958c4-107">Parameters</span></span>



| <span data-ttu-id="958c4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="958c4-108">Item</span></span>                                                   | <span data-ttu-id="958c4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="958c4-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="958c4-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="958c4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="958c4-111">\[en \] el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="958c4-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="958c4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="958c4-112">Return Value</span></span>

<span data-ttu-id="958c4-113">Devuelve-1 si *x* es menor que cero; 0 si *x* es igual a cero; y 1 si *x* es mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="958c4-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="958c4-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="958c4-114">Type Description</span></span>



| <span data-ttu-id="958c4-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="958c4-115">Name</span></span>  | [<span data-ttu-id="958c4-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="958c4-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="958c4-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="958c4-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="958c4-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="958c4-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="958c4-119">*x*</span><span class="sxs-lookup"><span data-stu-id="958c4-119">*x*</span></span>   | <span data-ttu-id="958c4-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="958c4-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="958c4-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="958c4-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="958c4-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="958c4-122">any</span></span>                            |
| <span data-ttu-id="958c4-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="958c4-123">*ret*</span></span> | <span data-ttu-id="958c4-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="958c4-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="958c4-125">**int**</span><span class="sxs-lookup"><span data-stu-id="958c4-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="958c4-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="958c4-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="958c4-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="958c4-127">Minimum Shader Model</span></span>

<span data-ttu-id="958c4-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="958c4-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="958c4-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="958c4-129">Shader Model</span></span>                                                                       | <span data-ttu-id="958c4-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="958c4-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="958c4-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="958c4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="958c4-132">sí</span><span class="sxs-lookup"><span data-stu-id="958c4-132">yes</span></span>                         |
| [<span data-ttu-id="958c4-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="958c4-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="958c4-134">sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="958c4-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="958c4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="958c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958c4-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="958c4-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

