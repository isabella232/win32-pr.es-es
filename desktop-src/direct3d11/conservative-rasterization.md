---
title: Rasterización conservadora de Direct3D 11.3
description: La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408575"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterización conservadora de Direct3D 11.3

La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.

-   [Información general](#overview)
-   [Interacciones con la canalización](#interactions-with-the-pipeline)
-   [Detalles de la implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La rasterización conservadora significa que todos los píxeles que están cubiertos parcialmente por un primitivo representado se rasterizan, lo que significa que se invoca el sombreador de píxeles. El comportamiento normal es el muestreo, que no se usa si está habilitada la rasterización conservadora.

La rasterización conservadora es útil en una serie de situaciones, incluida la certeza en la detección de colisiones, la selección de oclusión y la detección de visibilidad.

Por ejemplo, en la ilustración siguiente se muestra un triángulo verde representado mediante la rasterización conservadora. El área marrones se conoce como "región de incertidumbre", una región donde los errores de redondeo y otros problemas agregan cierta incertidumbre a las dimensiones exactas del triángulo. Los triángulos rojos de cada vértice muestran cómo se calcula la región de incertidumbre. Los cuadrados grises grandes muestran los píxeles que se representarán. Los cuadrados de color rojo muestran píxeles representados mediante la "regla superior izquierda", que entra en juego a medida que el borde del triángulo cruza el borde de los píxeles. Puede haber falsos positivos (conjunto de píxeles que no deberían haber sido) que el sistema normalmente, pero no siempre cull.

![muestra la regla superior izquierda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interacciones con la canalización

Para obtener muchos detalles sobre cómo interactúa la rasterización conservadora con la canalización de gráficos, consulte Rasterización conservadora [de D3D12.](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="implementation-details"></a>Detalles de la implementación

El tipo de rasterización admitido en Direct3D 12 a veces se conoce como "rasterización conservadora sobrestimada". También existe el concepto de "rasterización conservadora infravalorizada", lo que significa que solo se rasterizan los píxeles que están totalmente cubiertos por una primitiva representado. La información de rasterización conservadora subestimada está disponible a través del sombreador de píxeles mediante el uso de datos de cobertura de entrada, y solo la rasterización conservadora sobrestimada está disponible como modo de rasterización.

Si alguna parte de una primitiva se superpone a un píxel, ese píxel se considera cubierto y, a continuación, se rasteriza. Cuando un borde o una esquina de una primitiva se encuentra a lo largo del borde o la esquina de un píxel, la aplicación de la "regla superior izquierda" es específica de la implementación. Sin embargo, para las implementaciones que admiten triángulos degenerados, un triángulo degenerado a lo largo de un borde o esquina debe cubrir al menos un píxel.

Las implementaciones de rasterización conservadoras pueden variar en diferentes hardware y generar falsos positivos, lo que significa que pueden decidir incorrectamente que se cubren píxeles. Esto puede ocurrir debido a detalles específicos de la implementación, como errores primitivos de crecimiento o ajuste inherentes a las coordenadas de vértice de punto fijo usadas en la rasterización. La razón por la que los falsos positivos (con respecto a las coordenadas de vértice de punto fijo) son válidos es porque se necesita cierta cantidad de falsos positivos para permitir que una implementación realice la evaluación de cobertura en los vértices posteriores al ajuste (es decir, coordenadas de vértice que se han convertido de punto flotante al punto fijo 16,8 usado en el rasterizador), pero respetan la cobertura producida por las coordenadas de vértice de punto flotante originales.

Las implementaciones de rasterización conservadora no producen falsos negativos con respecto a las coordenadas de vértice de punto flotante para primitivos post snap no degenerados: si alguna parte de una primitiva se superpone a cualquier parte de un píxel, ese píxel se rasteriza.

Los triángulos que son degenerados (índices duplicados en un búfer de índice o colisionar en 3D) o que se vuelven degenerados después de la conversión de punto fijo (vértices de colisión en el rasterizador), pueden ser o no culled; ambos son comportamientos válidos. Los triángulos degenerados deben considerarse orientados hacia atrás, por lo que si una aplicación requiere un comportamiento específico, puede usar la selección de la cara posterior o probar la cara frontal. Los triángulos degenerados usan los valores asignados al vértice 0 para todos los valores interpolados.

Hay tres niveles de compatibilidad con hardware, además de la posibilidad de que el hardware no admita esta característica.

-   El nivel 1 admite regiones de incertidumbre de 1/2 píxeles y no hay degeneraciones posteriores al ajuste. Esto es bueno para la representación en mosaico, un atlas de textura, la generación de mapas claros y los mapas de sombra de subpíxeles.
-   El nivel 2 agrega regiones de incertidumbre posteriores al snap y 1/256. También agrega compatibilidad con la aceleración de algoritmos basada en CPU (por ejemplo, vóxelización).
-   El nivel 3 agrega regiones de incertidumbre de 1/512, cobertura de entrada interna y admite la selección de oclusión. La cobertura de entrada agrega el nuevo valor `SV_InnerCoverage` al lenguaje de sombreado de alto nivel (HLSL). Se trata de un entero escalar de 32 bits que se puede especificar en la entrada de un sombreador de píxeles y representa la información de rasterización conservadora infravalorada (es decir, si se garantiza que un píxel está totalmente cubierto).

## <a name="api-summary"></a>API summary

Los métodos, estructuras, enumeraciones y clases auxiliares siguientes hacen referencia a la rasterización conservadora:

-   [**D3D11 \_ RASTERIZER \_ DESC2:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) estructura que mantiene la descripción del rasterizador, y que tiene en cuenta la clase auxiliar CD3D12 \_ RASTERIZER DESC2 para crear descripciones \_ de rasterizador.
-   [**D3D11 \_ MODO \_ DE \_ RASTERIZACIÓN CONSERVADOR:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) valores de enumeración para el modo (on o off).
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) estructura que mantiene el nivel de soporte técnico.
-   [**D3D11 \_ NIVEL \_ DE \_ RASTERIZACIÓN CONSERVADOR:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) valores de enumeración para cada nivel de compatibilidad del hardware.
-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) método para acceder a las características admitidas.

## <a name="related-topics"></a>Temas relacionados
* [Características de Direct3D 11.3](direct3d-11-3-features.md)