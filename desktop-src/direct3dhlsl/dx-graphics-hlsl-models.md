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
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360518"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelos de sombreador frente a perfiles de sombreador

El lenguaje de sombreado de alto nivel para DirectX implementa una serie de modelos de sombreador. Con HLSL, puede crear sombreadores programables de tipo C para la canalización de Direct3D. Cada modelo de sombreador se basa en las funcionalidades del modelo anterior, implementando más funcionalidad con menos restricciones.

El modelo de sombreador 1 se inició con DirectX 8 e incluyó instrucciones de nivel de ensamblado y de tipo C. Este modelo tiene muchas limitaciones causadas por el hardware de sombreador programable temprano. El modelo de sombreador 2 y 3 se expandió en gran parte en el número de instrucciones y los sombreadores de constantes podrían usar. Son mucho más eficaces que el modelo de sombreador 1, pero siguen teniendo algunas de las limitaciones existentes del primer modelo de sombreador.

A partir de Windows Vista, el modelo 4 del sombreador es un rediseño completo. Permite instrucciones y constantes ilimitadas (dentro de las restricciones de hardware de la máquina), tiene objetos con plantilla para que el muestreo de textura sea más limpio y eficaz, y tiene las menos restricciones de cualquier modelo de sombreador. Sin embargo, requiere el Windows Driver Model que solo está disponible en el sistema operativo Windows Vista (o posterior).

## <a name="shader-profiles"></a>Perfiles de sombreador

Un perfil de sombreador es el destino para compilar un sombreador; En esta tabla se enumeran los perfiles de sombreador admitidos por cada modelo de sombreador.



| Modelo de sombreador                                                   | Perfiles de sombreador                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de sombreador 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modelo de sombreador 2](dx-graphics-hlsl-sm2.md)         | ps \_ 2 \_ 0, ps \_ \_ 2 x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ 0 level \_ \_ \_ 9 0, vs \_ 4 \_ \_ \_ 0 level 9 \_ 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 level \_ \_ 9 \_ 1, lib \_ 4 \_ 0 level 9 1, lib 4 0 \_ level \_ 9 \_ 3                                                                      |
| [Modelo de sombreador 3](dx-graphics-hlsl-sm3.md)         | ps \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, \_ vs 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ \_ 5 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (Aunque gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps \_ 4 \_ 1, vs 4 0 y vs 4 1 \_ \_ \_ \_ se introdujeron en el modelo de sombreador 4.0, el modelo de sombreador 5 agrega compatibilidad a estos perfiles de sombreador para búferes estructurados y búferes de direcciones de bytes).<br/> |
| [Modelo de sombreador 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |

Diferencias entre Direct3D 9 y Direct3D 10:

- Direct3D 9 introdujo los modelos de sombreador 1, 2 y 3.
- Direct3D 10 introdujo el modelo de sombreador 4.
- Direct3D 10.1 introdujo el modelo de sombreador 4.1.



 

## <a name="effect-profiles"></a>Perfiles de efecto

Un perfil de efecto es el destino para compilar un efecto o sombreador; En esta tabla se enumeran los perfiles de efecto que son compatibles con cada versión de Direct3D.

Diferencias entre Direct3D 9 y Direct3D 10:

- Direct3D 9 introdujo los perfiles de marco de efecto fx \_ 1 \_ 0 y fx \_ 2 \_ 0.
- Direct3D 10 introdujo effect-framework profile fx \_ 4 \_ 0.
- Direct3D 10.1 introdujo effect-framework profile fx \_ 4 \_ 1.
- Direct3D 11 introdujo effect-framework profile fx \_ 5 \_ 0.

> [!Note]  
> Estos perfiles de efectos heredados están en desuso.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





