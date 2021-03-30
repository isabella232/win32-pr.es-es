---
title: abs
description: Devuelve el valor absoluto del valor especificado.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- HLSL de ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984058"
---
# <a name="abs"></a><span data-ttu-id="69517-104">abs</span><span class="sxs-lookup"><span data-stu-id="69517-104">abs</span></span>

<span data-ttu-id="69517-105">Devuelve el valor absoluto del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="69517-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="69517-106">RET ABS (*x*)</span><span class="sxs-lookup"><span data-stu-id="69517-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="69517-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69517-107">Parameters</span></span>



| <span data-ttu-id="69517-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="69517-108">Item</span></span>                                                   | <span data-ttu-id="69517-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="69517-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="69517-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="69517-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="69517-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="69517-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="69517-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69517-112">Return Value</span></span>

<span data-ttu-id="69517-113">Valor absoluto del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="69517-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="69517-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="69517-114">Type Description</span></span>



| <span data-ttu-id="69517-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="69517-115">Name</span></span>  | [<span data-ttu-id="69517-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="69517-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="69517-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="69517-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="69517-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="69517-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="69517-119">*x*</span><span class="sxs-lookup"><span data-stu-id="69517-119">*x*</span></span>   | <span data-ttu-id="69517-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="69517-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="69517-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="69517-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="69517-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="69517-122">any</span></span>                            |
| <span data-ttu-id="69517-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="69517-123">*ret*</span></span> | <span data-ttu-id="69517-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69517-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="69517-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69517-125">same as input *x*</span></span>                                                              | <span data-ttu-id="69517-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69517-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69517-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="69517-127">Minimum Shader Model</span></span>

<span data-ttu-id="69517-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="69517-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69517-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="69517-129">Shader Model</span></span>                                                                       | <span data-ttu-id="69517-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="69517-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="69517-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="69517-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="69517-132">sí</span><span class="sxs-lookup"><span data-stu-id="69517-132">yes</span></span>                   |
| [<span data-ttu-id="69517-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69517-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="69517-134">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="69517-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="69517-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="69517-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69517-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="69517-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

