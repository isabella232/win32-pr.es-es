---
title: Sombreadores de HLSL de Direct3D 12 Raytracing
description: Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105648155"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Sombreadores de HLSL de Direct3D 12 Raytracing

Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12. Estos sombreadores son funciones compiladas en una biblioteca, con el modelo de destino lib_6_3 y que se identifican mediante un atributo *[Shader ("shadertype")]* en la función de sombreador. Vea **intrínsecos** y **valores del sistema** para ver lo que se permite para cada tipo de sombreador.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                       | Descripción                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sombreador de cualquier acierto**](any-hit-shader.md)<br/>                              | Sombreador que se invoca cuando las intersecciones de rayo no son opacas.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador al que se puede llamar**](callable-shader.md)<br/>                              | Sombreador que se invoca desde otro sombreador con la función intrínseca **CallShader** .<br/>                                                                                                                                                                                                                                              |
| [**Sombreador del acierto más cercano**](closest-hit-shader.md)<br/>                              | Sombreador que se invoca cuando está habilitado y se ha determinado el acierto más cercano o ha finalizado la búsqueda de interseccións de Ray.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de intersección**](intersection-shader.md)<br/>                              | Sombreador que se utiliza para implementar primitivas de intersección personalizadas para los rayos que intersectan con un volumen de límite asociado (rectángulo de selección).<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de errores**](miss-shader.md)<br/>                              | Sombreador que se invoca cuando no se encuentran ni se aceptan intersecciones de rayo.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de generación de rayos**](ray-generation-shader.md)<br/>                              | Sombreador que llama a [**TraceRay**](traceray-function.md) para generar rayos.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia básica](direct3d-12-core-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





