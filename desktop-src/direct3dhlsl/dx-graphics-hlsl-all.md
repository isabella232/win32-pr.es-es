---
title: todo
description: Determina si todos los componentes del valor especificado son distintos de cero.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- todo HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984086"
---
# <a name="all"></a><span data-ttu-id="953b3-104">todo</span><span class="sxs-lookup"><span data-stu-id="953b3-104">all</span></span>

<span data-ttu-id="953b3-105">Determina si todos los componentes del valor especificado son distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="953b3-105">Determines if all components of the specified value are non-zero.</span></span>



| <span data-ttu-id="953b3-106">*RET* todo (*x*)</span><span class="sxs-lookup"><span data-stu-id="953b3-106">*ret* all(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="953b3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="953b3-107">Parameters</span></span>



| <span data-ttu-id="953b3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="953b3-108">Item</span></span>                                                   | <span data-ttu-id="953b3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="953b3-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="953b3-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="953b3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="953b3-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="953b3-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="953b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="953b3-112">Return Value</span></span>

<span data-ttu-id="953b3-113">**True** si todos los componentes del parámetro *x* son distintos de cero; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="953b3-113">**True** if all components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="953b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="953b3-114">Remarks</span></span>

<span data-ttu-id="953b3-115">Esta función es similar a [**cualquier**](dx-graphics-hlsl-any.md) función intrínseca de HLSL.</span><span class="sxs-lookup"><span data-stu-id="953b3-115">This function is similar to the [**any**](dx-graphics-hlsl-any.md) HLSL intrinsic function.</span></span> <span data-ttu-id="953b3-116">La función **any** determina si alguno de los componentes del valor especificado es distinto de cero, mientras que la función **All** determina si todos los componentes del valor especificado son distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="953b3-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="953b3-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="953b3-117">Type Description</span></span>



| <span data-ttu-id="953b3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="953b3-118">Name</span></span>  | [<span data-ttu-id="953b3-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="953b3-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="953b3-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="953b3-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="953b3-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="953b3-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="953b3-122">*x*</span><span class="sxs-lookup"><span data-stu-id="953b3-122">*x*</span></span>   | <span data-ttu-id="953b3-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="953b3-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="953b3-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="953b3-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="953b3-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="953b3-125">any</span></span>  |
| <span data-ttu-id="953b3-126">*direcc*</span><span class="sxs-lookup"><span data-stu-id="953b3-126">*ret*</span></span> | [<span data-ttu-id="953b3-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="953b3-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="953b3-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="953b3-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="953b3-129">1</span><span class="sxs-lookup"><span data-stu-id="953b3-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="953b3-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="953b3-130">Minimum Shader Model</span></span>

<span data-ttu-id="953b3-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="953b3-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="953b3-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="953b3-132">Shader Model</span></span>                                                                       | <span data-ttu-id="953b3-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="953b3-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="953b3-134">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="953b3-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="953b3-135">sí</span><span class="sxs-lookup"><span data-stu-id="953b3-135">yes</span></span>                   |
| [<span data-ttu-id="953b3-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="953b3-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="953b3-137">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="953b3-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="953b3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="953b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953b3-139">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="953b3-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

