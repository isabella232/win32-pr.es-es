---
title: RestartStrip (objeto Stream-Output HLSL de DirectX)
description: Finaliza la franja primitiva actual e inicia una nueva. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará la primitiva incompleta al final.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120200"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="acc31-104">RestartStrip (objeto Stream-Output HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="acc31-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="acc31-105">Finaliza la franja primitiva actual e inicia una nueva.</span><span class="sxs-lookup"><span data-stu-id="acc31-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="acc31-106">Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará la primitiva incompleta al final.</span><span class="sxs-lookup"><span data-stu-id="acc31-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="acc31-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="acc31-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="acc31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acc31-108">Parameters</span></span>



| <span data-ttu-id="acc31-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="acc31-109">Item</span></span>                                                                                     | <span data-ttu-id="acc31-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="acc31-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="acc31-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="acc31-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="acc31-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acc31-112">Return Value</span></span>

<span data-ttu-id="acc31-113">None</span><span class="sxs-lookup"><span data-stu-id="acc31-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="acc31-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acc31-114">Remarks</span></span>

<span data-ttu-id="acc31-115">Un corte de franja hace que la franja actual finalice y se inicie una nueva.</span><span class="sxs-lookup"><span data-stu-id="acc31-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="acc31-116">Un corte de franja se puede realizar llamando explícitamente a este método o simplemente representando hasta el valor de índice máximo ( 1, que es 0xffffffff para índices de 32 bits o 0xffff para índices de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="acc31-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="acc31-117">Cada instancia de un dibujo con instancia indizada genera automáticamente un corte de franja.</span><span class="sxs-lookup"><span data-stu-id="acc31-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="acc31-118">Esto es así incluso si la topología no es una franja de triángulos.</span><span class="sxs-lookup"><span data-stu-id="acc31-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="acc31-119">La compatibilidad con el reinicio y el 1 "valor mágico" para un corte solo está disponible en los dispositivos de nivel [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) característica 10.0 o superior.</span><span class="sxs-lookup"><span data-stu-id="acc31-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="acc31-120">Siempre se supone que la salida es una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="acc31-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="acc31-121">Para convertir la salida en una lista de triángulos, debe llamar a RestartStrip entre cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="acc31-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="acc31-122">No se admiten los ventiladores de triángulo.</span><span class="sxs-lookup"><span data-stu-id="acc31-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="acc31-123">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="acc31-123">Minimum Shader Model</span></span>

<span data-ttu-id="acc31-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc31-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="acc31-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="acc31-125">Shader Model</span></span>                                              | <span data-ttu-id="acc31-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="acc31-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="acc31-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="acc31-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="acc31-128">Sí</span><span class="sxs-lookup"><span data-stu-id="acc31-128">yes</span></span>       |
| [<span data-ttu-id="acc31-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acc31-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="acc31-130">No</span><span class="sxs-lookup"><span data-stu-id="acc31-130">no</span></span>        |
| [<span data-ttu-id="acc31-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acc31-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="acc31-132">No</span><span class="sxs-lookup"><span data-stu-id="acc31-132">no</span></span>        |
| [<span data-ttu-id="acc31-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acc31-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="acc31-134">No</span><span class="sxs-lookup"><span data-stu-id="acc31-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="acc31-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acc31-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc31-136">Objeto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="acc31-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

