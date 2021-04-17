---
description: Sombreador que llama a TraceRay para generar rayos.
ms.assetid: ''
title: Sombreador de generación de rayos
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705383"
---
# <a name="ray-generation-shader"></a><span data-ttu-id="fd300-103">Sombreador de generación de rayos</span><span class="sxs-lookup"><span data-stu-id="fd300-103">Ray Generation Shader</span></span>

<span data-ttu-id="fd300-104">Sombreador que llama a [**TraceRay**](traceray-function.md) para generar rayos.</span><span class="sxs-lookup"><span data-stu-id="fd300-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="fd300-105">La carga de rayo inicial definida por el usuario para cada rayo se proporciona al sitio de llamada **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="fd300-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="fd300-106">[**CallShader**](callshader-function.md) también se puede usar en sombreadores de generación de rayos para invocar [sombreadores Invocables](callable-shader.md).</span><span class="sxs-lookup"><span data-stu-id="fd300-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="fd300-107">**DispatchRays** invoca una cuadrícula de las invocaciones del sombreador de generación de rayo.</span><span class="sxs-lookup"><span data-stu-id="fd300-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="fd300-108">Cada invocación (subproceso) de un sombreador de generación de rayo conoce su ubicación en la cuadrícula global, puede generar rayos arbitrarios a través de [**TraceRay**](traceray-function.md)y funciona independientemente de otras invocaciones.</span><span class="sxs-lookup"><span data-stu-id="fd300-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="fd300-109">No hay ningún orden definido de ejecución de subprocesos con respecto al otro.</span><span class="sxs-lookup"><span data-stu-id="fd300-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="fd300-110">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fd300-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="fd300-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd300-111">Example</span></span>

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




