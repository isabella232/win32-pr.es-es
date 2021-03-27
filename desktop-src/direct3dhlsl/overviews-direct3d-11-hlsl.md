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
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904672"
---
# <a name="hlsl-shader-model-5"></a>Modelo 5 del sombreador HLSL

Esta sección contiene material de información general para el lenguaje de sombreador de High-Level, concretamente las nuevas características del modelo de sombreador 5 que se introdujeron en Microsoft Direct3D 11.

## <a name="in-this-section"></a>En esta sección



| Elemento                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | La vinculación dinámica permite que el tiempo de ejecución tome una decisión en tiempo de dibujo (en lugar de tiempo de compilación) sobre qué ruta de acceso del código se va a ejecutar. Esto reduce el problema de proliferación del sombreador causado por los sombreadores con firmas de entrada casi idénticas.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Nuevas características del sombreador de geometría, entre las que se incluyen: creación de instancias, que proporciona un aumento del rendimiento cuando el orden de los primitivos en la secuencia no es importante, y flujos de salida de varios puntos para que un sombreador pueda generar vértices en más de una secuencia.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tesela](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | El tiempo de ejecución de Direct3D 11 admite tres nuevas fases que implementan Teselación, que convierte las superficies de subdivisiones de bajo detalle en primitivas más detalladas en la GPU. Mosaicos de teselación (o rotura) de superficies de orden superior en estructuras adecuadas para la representación. Las tres fases de teselación son las fases del sombreador de casco, del teselador y del sombreador de dominio.<br/> |



 

Además, la sección de referencia abarca muchos elementos de API nuevos para el modelo de sombreador 5: [atributos](d3d11-graphics-reference-sm5-attributes.md), [funciones intrínsecas](d3d11-graphics-reference-sm5-intrinsics.md), [objetos y métodos de modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)y [valores del sistema](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

