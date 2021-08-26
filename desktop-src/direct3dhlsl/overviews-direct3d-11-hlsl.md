---
title: Modelo 5 del sombreador HLSL
description: Modelo 5 del sombreador HLSL
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 537b2460b73f30397561dea37bcb3711b64a935c43d45662428585a47d6f6574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095355"
---
# <a name="hlsl-shader-model-5"></a>Modelo 5 del sombreador HLSL

Esta sección contiene material de información general para High-Level Shader Language, en concreto las nuevas características del modelo de sombreador 5 introducidas en Microsoft Direct3D 11.

## <a name="in-this-section"></a>En esta sección



| Elemento                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | La vinculación dinámica permite al tiempo de ejecución tomar una decisión en tiempo de dibujo (en lugar de en tiempo de compilación) sobre la ruta de acceso del código que se va a ejecutar. Esto reduce el problema de proliferación del sombreador causado por sombreadores con firmas de entrada casi idénticas.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Nuevas características del sombreador de geometría, como la creación de instancias, que proporciona un aumento del rendimiento cuando no importa el orden de las primitivas en la secuencia, y varios flujos de salida de punto para que un sombreador pueda generar vértices en más de una secuencia.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Teselación](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | El entorno de ejecución de Direct3D 11 admite tres nuevas fases que implementan teselación, que convierte las superficies de subdivisión de bajo detalle en primitivas de mayor detalle en la GPU. Los mosaicos de teselación (o se divide) superficies de alto orden en estructuras adecuadas para la representación. Las tres fases de teselación son el sombreador de casco, el teselador y las fases de sombreador de dominio.<br/> |



 

Además, la sección de referencia trata muchos elementos de [](d3d11-graphics-reference-sm5-attributes.md)API nuevos para el modelo de sombreador 5, incluidos: atributos [,](d3d11-graphics-reference-sm5-intrinsics.md)funciones intrínsecas, objetos y métodos del modelo de sombreador [5](d3d11-graphics-reference-sm5-objects.md)y valores [del sistema](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

