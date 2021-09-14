---
title: Modelo de sombreador 4
description: Shader Model 4 es un superconjunto de las funcionalidades de Shader Model 3, salvo que Shader Model 4 no admite las características de Shader Model 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c863d952990cd05394244fe662650df59568eeaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974707"
---
# <a name="shader-model-4"></a>Modelo de sombreador 4

Shader Model 4 es un superconjunto de las funcionalidades de [Shader Model 3](dx-graphics-hlsl-sm3.md), salvo que Shader Model 4 no admite las características de Shader Model 1. Se ha diseñado mediante un núcleo de sombreador común que proporciona un conjunto común de características a todos los sombreadores programables, que solo se pueden programar mediante HLSL.




| Característica | Funcionalidad | 
|---------|------------|
| Conjunto de instrucciones | <a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones HLSL</strong></a> | 
| Conjunto de registro | El conjunto de registros es accesible a través de miembros en búferes constantes y de textura mediante semántica HLSL para cosas como el empaquetado de componentes.<ul><li>Registros de sombreador de píxeles (vea <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registros - ps_4_0</a> y Registros - <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">ps_4_1</a>)</li><li>Registros del sombreador de <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">vértices</a> (vea Registros - vs_4_0 <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">y Registros - vs_4_1</a>)</li><li>Registros del sombreador de geometría (vea <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registros - gs_4_0</a> y Registros - <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">gs_4_1</a>)</li></ul> | 
| Máximo del sombreador de vértices | Sin restricción | 
| Máximo de sombreador de píxeles | Sin restricción | 
| Nuevos perfiles de sombreador agregados | gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1* | 
| Nuevo perfil Effect-Framework agregado | fx_4_0, fx_4_1* | 




 

\* - gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1 y fx \_ 4 \_ 1 se admiten en Direct3D 10.1 o superior.

El modelo de sombreador 4 admite una nueva fase de canalización(la fase de sombreador de geometría) que se puede usar para crear o modificar la geometría existente. También incluye dos nuevos tipos de objeto: un objeto de salida de flujo diseñado para transmitir datos fuera de la fase de geometría y un objeto de textura con plantilla que implementa funciones de muestreo de textura.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Constantes](dx-graphics-hlsl-constants.md)
-   [Objeto Geometry-Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
-   [Objeto Texture](dx-graphics-hlsl-to-type.md)

El modelo de sombreador 4 admite reglas de empaquetado que dictan la forma en que se pueden organizar los datos de forma estricta cuando se almacenan. Estas reglas se describen en [Reglas de empaquetado para variables constantes.](dx-graphics-hlsl-packing-rules.md)

En la sección Ensamblado del modelo de sombreador [4](dx-graphics-hlsl-sm4-asm.md) se describen las instrucciones de ensamblado que admiten el Modelo de sombreador 4 y el Modelo de sombreador 4.1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




