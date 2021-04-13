---
title: Modelo de sombreador 5
description: Esta sección contiene las páginas de referencia para el modelo 5 del sombreador HLSL.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420910"
---
# <a name="shader-model-5"></a>Modelo de sombreador 5

Esta sección contiene las páginas de referencia para el modelo 5 del sombreador HLSL.

El modelo de sombreador 5 es un supraconjunto de las capacidades del [modelo de sombreador 4](dx-graphics-hlsl-sm4.md). Se ha diseñado con un núcleo de sombreador común que proporciona un conjunto común de características para todos los sombreadores programables, que solo se pueden programar mediante HLSL.



| Característica                   | Funcionalidad                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conjunto de instrucciones           | [**Funciones intrínsecas de HLSL**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Sombreador de vértices máximo         | Sin restricción                                                                                                                                         |
| Sombreador de píxeles máximo          | Sin restricción                                                                                                                                         |
| Nuevos perfiles de sombreador agregados | CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS 4 1 \_ \_ \* , vs \_ 4 \_ 1, \* CS \_ 5 \_ 0, DS \_ 5 0, GS 5 \_ \_ \_ 0, HS \_ 5 0 \_ , PS \_ 5 \_ 0, vs \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 y vs \_ 4 \_ 1 se introdujeron en el modelo de sombreador 4,0. sin embargo, DirectX 11 agrega compatibilidad con [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) y búferes de direcciones de bytes al modelo de sombreador 4 que se ejecuta en hardware de DirectX 10.

El modelo de sombreador 5 presenta el [sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) que proporciona informática de uso general de alta velocidad.

En una lista de las [características de Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features)se incluye una lista más completa de las características del modelo de sombreador 5.

En la sección de [ensamblado modelo de sombreador 5](shader-model-5-assembly--directx-hlsl-.md) se describen las instrucciones de ensamblado que admite el modelo de sombreador 5.

## <a name="in-this-section"></a>En esta sección



| Elemento                                                                                                                                                                                                                                                        | Descripción                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Páginas de referencia para los atributos del modelo de sombreador 5.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funciones intrínsecas del modelo de sombreador 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Páginas de referencia de las funciones intrínsecas del modelo de sombreador 5.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Páginas de referencia para objetos y métodos del modelo de sombreador 5.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valores del sistema del modelo de sombreador 5](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Páginas de referencia para los valores del sistema del modelo de sombreador 5.<br/>       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

