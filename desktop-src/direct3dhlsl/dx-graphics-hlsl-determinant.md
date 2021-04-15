---
title: determinante
description: Devuelve el determinante de la matriz cuadrada de punto flotante especificada.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- HLSL determinante
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984018"
---
# <a name="determinant"></a><span data-ttu-id="35d05-104">determinante</span><span class="sxs-lookup"><span data-stu-id="35d05-104">determinant</span></span>

<span data-ttu-id="35d05-105">Devuelve el determinante de la matriz cuadrada de punto flotante especificada.</span><span class="sxs-lookup"><span data-stu-id="35d05-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="35d05-106">determinante *RET* (*m*)</span><span class="sxs-lookup"><span data-stu-id="35d05-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="35d05-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35d05-107">Parameters</span></span>



| <span data-ttu-id="35d05-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="35d05-108">Item</span></span>                                                   | <span data-ttu-id="35d05-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="35d05-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="35d05-110"><span id="m"></span><span id="M"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="35d05-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="35d05-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="35d05-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="35d05-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35d05-112">Return Value</span></span>

<span data-ttu-id="35d05-113">Valor escalar y de punto flotante que representa el factor determinante del parámetro *m* .</span><span class="sxs-lookup"><span data-stu-id="35d05-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="35d05-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="35d05-114">Type Description</span></span>



| <span data-ttu-id="35d05-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="35d05-115">Name</span></span>  | [<span data-ttu-id="35d05-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="35d05-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="35d05-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="35d05-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="35d05-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="35d05-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="35d05-119">*m*</span><span class="sxs-lookup"><span data-stu-id="35d05-119">*m*</span></span>   | [<span data-ttu-id="35d05-120">**matrices**</span><span class="sxs-lookup"><span data-stu-id="35d05-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="35d05-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="35d05-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="35d05-122">any (número de filas = número de columnas)</span><span class="sxs-lookup"><span data-stu-id="35d05-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="35d05-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="35d05-123">*ret*</span></span> | [<span data-ttu-id="35d05-124">**escalar**</span><span class="sxs-lookup"><span data-stu-id="35d05-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="35d05-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="35d05-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="35d05-126">1</span><span class="sxs-lookup"><span data-stu-id="35d05-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="35d05-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="35d05-127">Minimum Shader Model</span></span>

<span data-ttu-id="35d05-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="35d05-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35d05-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="35d05-129">Shader Model</span></span>                                                                       | <span data-ttu-id="35d05-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="35d05-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="35d05-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="35d05-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="35d05-132">sí</span><span class="sxs-lookup"><span data-stu-id="35d05-132">yes</span></span>                   |
| [<span data-ttu-id="35d05-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35d05-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="35d05-134">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="35d05-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="35d05-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="35d05-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d05-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="35d05-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

