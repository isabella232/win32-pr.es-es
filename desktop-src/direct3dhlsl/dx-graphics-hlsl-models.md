---
title: Modelos de sombreador frente a perfiles de sombreador
description: Modelos de sombreador frente a perfiles de sombreador
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903740"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelos de sombreador frente a perfiles de sombreador

El lenguaje de sombreado de alto nivel para DirectX implementa una serie de modelos de sombreador. Con HLSL, puede crear sombreadores programables similares a C para la canalización de Direct3D. Cada modelo de sombreador se basa en las capacidades del modelo antes de hacerlo, implementando más funcionalidad con menos restricciones.

El modelo de sombreador 1 comenzó con DirectX 8 e incluye instrucciones de nivel de ensamblado y de tipo C. Este modelo tiene muchas limitaciones causadas por el hardware del sombreador programable inicial. El modelo de sombreador 2 y 3 se expande en gran medida en el número de instrucciones y los sombreadores de constantes podrían usar. Son mucho más eficaces que el modelo de sombreador 1, pero siguen teniendo algunas de las limitaciones existentes del primer modelo de sombreador.

A partir de Windows Vista, el modelo de sombreador 4 es un rediseño completo. Permite instrucciones y constantes ilimitadas (dentro de las restricciones de hardware de la máquina), tiene objetos con plantilla para hacer que el muestreo de textura sea más limpio y más eficaz, y tiene el menor número de restricciones de cualquier modelo de sombreador. Sin embargo, requiere el Modelo de controlador de Windows que solo está disponible en el sistema operativo Windows Vista (o posterior).

## <a name="shader-profiles"></a>Perfiles del sombreador

Un perfil de sombreador es el destino para compilar un sombreador; en esta tabla se enumeran los perfiles del sombreador que son compatibles con cada modelo de sombreador.



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modelo de sombreador                                       | Perfiles del sombreador                                                                                                                                                                                                                                                                                       |
| [Modelo de sombreador 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modelo de sombreador 2](dx-graphics-hlsl-sm2.md)         | PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 0, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 3, vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 0, vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1, vs \_ 4 \_ 0 nivel 9 3, \_ \_ \_ lib \_ 4 0 nivel 9 1, \_ \_ \_ \_ lib \_ 4 \_ \_ \_ \_ 0 nivel 9 3                                                                      |
| [Modelo de sombreador 3](dx-graphics-hlsl-sm3.md)         | PS \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)         | CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 1, \_ vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 0 \_ , vs \_ 5 \_ 0, lib \_ 5 \_ 0 (aunque GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 y vs \_ 4 \_ 1 se introdujeron en el modelo de sombreador 4,0, el modelo de sombreador 5 agrega compatibilidad con estos perfiles de sombreador para búferes estructurados y búferes de direcciones<br/> |
| [Modelo de sombreador 6](shader-model-6-0.md)             | CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> Direct3D 9 incorporó los modelos de sombreador 1, 2 y 3.<br/> Direct3D 10 presentó el modelo de sombreador 4.<br/> Direct3D 10,1 presentó el modelo de sombreador 4,1.<br/> |



 

## <a name="effect-profiles"></a>Perfiles de efectos

Un perfil de efecto es el destino para compilar un efecto o sombreador; en esta tabla se enumeran los perfiles de efecto que son compatibles con cada versión de Direct3D.



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> Direct3D 9 incorporó los perfiles de marco de efecto FX \_ 1 \_ 0 y FX \_ 2 \_ 0.<br/> Direct3D 10 presentó Effect-Framework Profile FX \_ 4 \_ 0.<br/> Direct3D 10,1 incorporó Effect-Framework Profile FX \_ 4 \_ 1.<br/> En Direct3D 11 se incorporó Effect-Framework Profile FX \_ 5 \_ 0.<br/> |



 

> [!Note]  
> Estos perfiles de efectos heredados están desusados.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





