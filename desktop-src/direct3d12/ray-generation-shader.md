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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072915"
---
# <a name="ray-generation-shader"></a>Sombreador de generación de rayos

Sombreador que llama [**a TraceRay**](traceray-function.md) para generar rayos. La carga inicial de rayos definida por el usuario para cada rayo se proporciona al **sitio de llamada TraceRay.**  [**CallShader también**](callshader-function.md) se puede usar en sombreadores de generación de rayos para invocar [sombreadores a los que se puede llamar.](callable-shader.md)

**DispatchRays invoca** una cuadrícula de invocaciones de sombreador de generación de rayos.  Cada invocación (subproceso) de un sombreador de generación de rayos conoce su ubicación en la cuadrícula general, puede generar rayos arbitrarios a través de [**TraceRay**](traceray-function.md)y funciona independientemente de otras invocaciones. No hay ningún orden definido de ejecución de subprocesos entre sí.

## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


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

 

 




