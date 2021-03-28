---
title: cualquiera
description: Determina si alguno de los componentes del valor especificado es distinto de cero.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- cualquier HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984083"
---
# <a name="any"></a><span data-ttu-id="b20cd-104">cualquiera</span><span class="sxs-lookup"><span data-stu-id="b20cd-104">any</span></span>

<span data-ttu-id="b20cd-105">Determina si alguno de los componentes del valor especificado es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b20cd-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="b20cd-106">*RET* any (*x*)</span><span class="sxs-lookup"><span data-stu-id="b20cd-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="b20cd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b20cd-107">Parameters</span></span>



| <span data-ttu-id="b20cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b20cd-108">Item</span></span>                                                   | <span data-ttu-id="b20cd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b20cd-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b20cd-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="b20cd-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b20cd-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b20cd-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b20cd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b20cd-112">Return Value</span></span>

<span data-ttu-id="b20cd-113">**True** si alguno de los componentes del parámetro *x* es distinto de cero; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b20cd-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b20cd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b20cd-114">Remarks</span></span>

<span data-ttu-id="b20cd-115">Esta función es similar a la función intrínseca de HLSL [**All**](dx-graphics-hlsl-all.md) .</span><span class="sxs-lookup"><span data-stu-id="b20cd-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="b20cd-116">La función **any** determina si alguno de los componentes del valor especificado es distinto de cero, mientras que la función **All** determina si todos los componentes del valor especificado son distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="b20cd-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="b20cd-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="b20cd-117">Type Description</span></span>



| <span data-ttu-id="b20cd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b20cd-118">Name</span></span>  | [<span data-ttu-id="b20cd-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="b20cd-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b20cd-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b20cd-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="b20cd-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b20cd-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="b20cd-122">*x*</span><span class="sxs-lookup"><span data-stu-id="b20cd-122">*x*</span></span>   | <span data-ttu-id="b20cd-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="b20cd-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="b20cd-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b20cd-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b20cd-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="b20cd-125">any</span></span>  |
| <span data-ttu-id="b20cd-126">*direcc*</span><span class="sxs-lookup"><span data-stu-id="b20cd-126">*ret*</span></span> | [<span data-ttu-id="b20cd-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="b20cd-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="b20cd-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="b20cd-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="b20cd-129">1</span><span class="sxs-lookup"><span data-stu-id="b20cd-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b20cd-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b20cd-130">Minimum Shader Model</span></span>

<span data-ttu-id="b20cd-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b20cd-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b20cd-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b20cd-132">Shader Model</span></span>                                                                       | <span data-ttu-id="b20cd-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="b20cd-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="b20cd-134">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="b20cd-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b20cd-135">sí</span><span class="sxs-lookup"><span data-stu-id="b20cd-135">yes</span></span>                   |
| [<span data-ttu-id="b20cd-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b20cd-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b20cd-137">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b20cd-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b20cd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b20cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20cd-139">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b20cd-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

