---
title: Sombreadores de HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen sombreadores de lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2321511be2ef912a6dce6710b233cb59dcc7712e9e8f63db890d8707822c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733778"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Sombreadores de HLSL de Direct3D 12 Raytracing

Los siguientes sombreadores HLSL admiten la canalización de trazado de rayos de Direct3D 12. Estos sombreadores son funciones compiladas en una biblioteca, con el modelo de destino lib_6_3, e identificadas por un atributo *[shader("shadertype")]* en la función de sombreador. Vea **Intrínsecos** **y valores del** sistema para ver lo que se permite para cada tipo de sombreador.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                       | Descripción                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sombreador de cualquier acierto**](any-hit-shader.md)<br/>                              | Sombreador que se invoca cuando las intersecciones de rayos no son opacas.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador al que se puede llamar**](callable-shader.md)<br/>                              | Sombreador que se invoca desde otro sombreador con la **función intrínseca CallShader.**<br/>                                                                                                                                                                                                                                              |
| [**Sombreador del acierto más cercano**](closest-hit-shader.md)<br/>                              | Sombreador que se invoca cuando está habilitado y se ha determinado el impacto más cercano o se ha finalizado la búsqueda de intersección de rayos.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de intersección**](intersection-shader.md)<br/>                              | Sombreador que se usa para implementar primitivas de intersección personalizadas para los rayos que cruzan un volumen de límite asociado (rectángulo de selección).<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de errores**](miss-shader.md)<br/>                              | Sombreador que se invoca cuando no se encuentra ni se acepta ninguna intersección de rayo.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de generación de rayos**](ray-generation-shader.md)<br/>                              | Sombreador que llama [**a TraceRay**](traceray-function.md) para generar rayos.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia principal](direct3d-12-core-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





