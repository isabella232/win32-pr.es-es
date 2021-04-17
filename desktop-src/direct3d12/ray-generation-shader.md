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
# <a name="ray-generation-shader"></a>Sombreador de generación de rayos

Sombreador que llama a [**TraceRay**](traceray-function.md) para generar rayos. La carga de rayo inicial definida por el usuario para cada rayo se proporciona al sitio de llamada **TraceRay** .  [**CallShader**](callshader-function.md) también se puede usar en sombreadores de generación de rayos para invocar [sombreadores Invocables](callable-shader.md).

**DispatchRays** invoca una cuadrícula de las invocaciones del sombreador de generación de rayo.  Cada invocación (subproceso) de un sombreador de generación de rayo conoce su ubicación en la cuadrícula global, puede generar rayos arbitrarios a través de [**TraceRay**](traceray-function.md)y funciona independientemente de otras invocaciones. No hay ningún orden definido de ejecución de subprocesos con respecto al otro.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("raygeneration")]
```



## <a name="example"></a>Ejemplo

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

 

 




