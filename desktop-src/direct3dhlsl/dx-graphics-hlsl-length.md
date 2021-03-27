---
title: length
description: Devuelve la longitud del vector de punto flotante especificado.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- HLSL de longitud
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792040"
---
# <a name="length"></a><span data-ttu-id="b90a6-104">length</span><span class="sxs-lookup"><span data-stu-id="b90a6-104">length</span></span>

<span data-ttu-id="b90a6-105">Devuelve la longitud del vector de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="b90a6-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="b90a6-106">longitud *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="b90a6-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="b90a6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b90a6-107">Parameters</span></span>



| <span data-ttu-id="b90a6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b90a6-108">Item</span></span>                                                   | <span data-ttu-id="b90a6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90a6-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="b90a6-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="b90a6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b90a6-111">Vector de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="b90a6-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b90a6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b90a6-112">Return Value</span></span>

<span data-ttu-id="b90a6-113">Escalar de punto flotante que representa la longitud del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="b90a6-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b90a6-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="b90a6-114">Type Description</span></span>



| <span data-ttu-id="b90a6-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="b90a6-115">Name</span></span>  | [<span data-ttu-id="b90a6-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="b90a6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b90a6-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b90a6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b90a6-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b90a6-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b90a6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b90a6-119">*x*</span></span>   | [<span data-ttu-id="b90a6-120">**medios**</span><span class="sxs-lookup"><span data-stu-id="b90a6-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b90a6-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="b90a6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b90a6-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="b90a6-122">any</span></span>  |
| <span data-ttu-id="b90a6-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="b90a6-123">*ret*</span></span> | [<span data-ttu-id="b90a6-124">**escalar**</span><span class="sxs-lookup"><span data-stu-id="b90a6-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b90a6-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="b90a6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b90a6-126">1</span><span class="sxs-lookup"><span data-stu-id="b90a6-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b90a6-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b90a6-127">Minimum Shader Model</span></span>

<span data-ttu-id="b90a6-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b90a6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b90a6-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b90a6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="b90a6-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="b90a6-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b90a6-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="b90a6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b90a6-132">sí</span><span class="sxs-lookup"><span data-stu-id="b90a6-132">yes</span></span>                 |
| [<span data-ttu-id="b90a6-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b90a6-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b90a6-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="b90a6-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b90a6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b90a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90a6-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b90a6-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

