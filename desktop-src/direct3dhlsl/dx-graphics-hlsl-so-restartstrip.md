---
title: RestartStrip (objeto de Stream-Output de DirectX HLSL)
description: Finaliza la franja primitiva actual e inicia una nueva banda. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará el primitivo incompleto en el extremo.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997080"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="d8208-104">RestartStrip (objeto de Stream-Output de DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8208-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="d8208-105">Finaliza la franja primitiva actual e inicia una nueva banda.</span><span class="sxs-lookup"><span data-stu-id="d8208-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="d8208-106">Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará el primitivo incompleto en el extremo.</span><span class="sxs-lookup"><span data-stu-id="d8208-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>



|                 |
|-----------------|
| <span data-ttu-id="d8208-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="d8208-107">RestartStrip();</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d8208-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8208-108">Parameters</span></span>



| <span data-ttu-id="d8208-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8208-109">Item</span></span>                                                                                     | <span data-ttu-id="d8208-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8208-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="d8208-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguna**</span><span class="sxs-lookup"><span data-stu-id="d8208-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="d8208-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8208-112">Return Value</span></span>

<span data-ttu-id="d8208-113">None</span><span class="sxs-lookup"><span data-stu-id="d8208-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="d8208-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8208-114">Remarks</span></span>

<span data-ttu-id="d8208-115">Un corte de franja hace que finalice la franja actual y se inicie una nueva.</span><span class="sxs-lookup"><span data-stu-id="d8208-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="d8208-116">Un corte de franja se puede hacer llamando explícitamente a este método o simplemente representando hasta el valor de índice máximo (1, que es 0xFFFFFFFF para índices de 32 bits o 0xFFFF para índices de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="d8208-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="d8208-117">Cada instancia de un dibujo de instancia indizada genera automáticamente un corte de franja.</span><span class="sxs-lookup"><span data-stu-id="d8208-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="d8208-118">Esto es así incluso si la topología no es una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="d8208-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="d8208-119">La compatibilidad con el reinicio y el 1 valor mágico para un corte solo está disponible en dispositivos de [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="d8208-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="d8208-120">Siempre se supone que la salida es una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="d8208-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="d8208-121">Para que el resultado sea una lista de triángulos, debe llamar a RestartStrip entre cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="d8208-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="d8208-122">No se admiten los ventiladores de triángulo.</span><span class="sxs-lookup"><span data-stu-id="d8208-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d8208-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d8208-123">Minimum Shader Model</span></span>

<span data-ttu-id="d8208-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8208-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d8208-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d8208-125">Shader Model</span></span>                                              | <span data-ttu-id="d8208-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="d8208-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d8208-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d8208-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8208-128">sí</span><span class="sxs-lookup"><span data-stu-id="d8208-128">yes</span></span>       |
| [<span data-ttu-id="d8208-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8208-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8208-130">no</span><span class="sxs-lookup"><span data-stu-id="d8208-130">no</span></span>        |
| [<span data-ttu-id="d8208-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8208-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8208-132">no</span><span class="sxs-lookup"><span data-stu-id="d8208-132">no</span></span>        |
| [<span data-ttu-id="d8208-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8208-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8208-134">no</span><span class="sxs-lookup"><span data-stu-id="d8208-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d8208-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8208-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8208-136">Stream: salida de objeto</span><span class="sxs-lookup"><span data-stu-id="d8208-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

