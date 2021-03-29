---
title: clip
description: Descarta el píxel actual si el valor especificado es menor que cero.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- recorte de HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984019"
---
# <a name="clip"></a><span data-ttu-id="24088-104">clip</span><span class="sxs-lookup"><span data-stu-id="24088-104">clip</span></span>

<span data-ttu-id="24088-105">Descarta el píxel actual si el valor especificado es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="24088-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="24088-106">clip (*x*)</span><span class="sxs-lookup"><span data-stu-id="24088-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="24088-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24088-107">Parameters</span></span>



| <span data-ttu-id="24088-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="24088-108">Item</span></span>                                                   | <span data-ttu-id="24088-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="24088-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="24088-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="24088-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="24088-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="24088-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="24088-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24088-112">Return Value</span></span>

<span data-ttu-id="24088-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24088-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="24088-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24088-114">Remarks</span></span>

<span data-ttu-id="24088-115">Use la función intrínseca de **clip** HLSL para simular los planos de recorte si cada componente del parámetro *x* representa la distancia desde un plano.</span><span class="sxs-lookup"><span data-stu-id="24088-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="24088-116">Además, utilice la función de **recorte** para probar el comportamiento alfa, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="24088-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="24088-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="24088-117">Type Description</span></span>



| <span data-ttu-id="24088-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="24088-118">Name</span></span> | [<span data-ttu-id="24088-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="24088-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="24088-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="24088-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="24088-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="24088-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="24088-122">*x*</span><span class="sxs-lookup"><span data-stu-id="24088-122">*x*</span></span>  | <span data-ttu-id="24088-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="24088-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="24088-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="24088-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="24088-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="24088-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="24088-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="24088-126">Minimum Shader Model</span></span>

<span data-ttu-id="24088-127">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="24088-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="24088-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="24088-128">Shader Model</span></span>                                              | <span data-ttu-id="24088-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="24088-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="24088-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="24088-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="24088-131">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="24088-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="24088-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24088-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="24088-133">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="24088-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="24088-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24088-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="24088-135">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="24088-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="24088-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24088-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="24088-137">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="24088-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="24088-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="24088-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24088-139">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="24088-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

