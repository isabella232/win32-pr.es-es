---
title: Rasterización conservadora de Direct3D 11,3
description: La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003cb7e31c1380943318b34f9308f6b5e72d6e51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271341"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterización conservadora de Direct3D 11,3

La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.

-   [Información general](#overview)
-   [Interacciones con la canalización](#interactions-with-the-pipeline)
-   [Detalles de implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La rasterización conservadora significa que se rasterizan todos los píxeles que están al menos parcialmente incluidos en una primitiva representada, lo que significa que se invoca el sombreador de píxeles. El comportamiento normal es el muestreo, que no se usa si está habilitada la rasterización conservadora.

La rasterización conservadora es útil en una serie de situaciones, entre las que se incluyen la certeza de la detección de colisiones, la selección de la oclusión y la detección de visibilidad.

Por ejemplo, en la siguiente ilustración se muestra un triángulo verde representado mediante la rasterización conservadora. El área marrón se conoce como "región de incertidumbre", una región en la que los errores de redondeo y otros problemas agregan incertidumbre a las dimensiones exactas del triángulo. Los triángulos rojos de cada vértice muestran cómo se calcula la región de incertidumbre. Los cuadrados grises grandes muestran los píxeles que se representarán. Los cuadrados de color rosa muestran los píxeles representados mediante la "regla superior izquierda", que entran en juego cuando el borde del triángulo cruza el borde de los píxeles. Puede haber falsos positivos (píxeles establecidos que no deberían haber) que el sistema normalmente, pero no siempre seleccionará.

![muestra la regla superior izquierda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interacciones con la canalización

Para muchos detalles sobre cómo la rasterización conservadora interactúa con la canalización de gráficos, consulte [rasterización conservadora de D3D12](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Detalles de la implementación

El tipo de rasterización compatible con Direct3D 12 a veces se conoce como "rasterización conservadora sobreestimada". También existe el concepto de "rasterización conservadora desestimada", lo que significa que solo se rasterizan los píxeles que están totalmente incluidos en una primitiva representada. La información de rasterización conservadora subestimada está disponible a través del sombreador de píxeles mediante el uso de datos de cobertura de entrada y solo está disponible la rasterización conservadora sobreestimada como modo de rasterización.

Si alguna parte de una primitiva se superpone a un píxel, ese píxel se considerará tratado y se rasterizará. Cuando un borde o esquina de una primitiva cae a lo largo del borde o la esquina de un píxel, la aplicación de la "regla superior izquierda" es específica de la implementación. Sin embargo, para las implementaciones que admiten triángulos degenerados, un triángulo degenerado a lo largo de un borde o una esquina debe cubrir al menos un píxel.

Las implementaciones de rasterización conservadora pueden variar en hardware diferente y generar falsos positivos, lo que significa que pueden decidir incorrectamente que los píxeles están incluidos. Esto puede deberse a detalles específicos de la implementación, como los errores primitivos de aumento o ajuste inherentes a las coordenadas de vértices de punto fijo utilizadas en la rasterización. La razón por la que los falsos positivos (con respecto a las coordenadas de vértices de punto fijo) son válidos es que se necesita una cantidad de falsos positivos para permitir que una implementación realice la evaluación de cobertura en los vértices con ajuste de nivel (es decir, las coordenadas de vértices que se han convertido desde el punto flotante al punto fijo 16,8 usado en el rasterizador), pero

Las implementaciones de rasterización conservadora no producen falsos negativos con respecto a las coordenadas de vértices de punto flotante para primitivas posteriores al ajuste no generadas: Si alguna parte de una primitiva se superpone a cualquier parte de un píxel, ese píxel se rasteriza.

Los triángulos degenerados (índices duplicados en un búfer de índice o colineales en 3D), o se convierten en degenerados después de la conversión de punto fijo (vértices colineales en el rasterizador), pueden o no ser reactivados; ambos son comportamientos válidos. Los triángulos degenerados se deben tener en cuenta hacia atrás, por lo que si una aplicación requiere un comportamiento concreto, puede utilizar la selección de la parte trasera o la prueba para orientarse hacia delante. Los triángulos degenerados usan los valores asignados al vértice 0 para todos los valores interpolados.

Hay tres niveles de compatibilidad de hardware, además de la posibilidad de que el hardware no sea compatible con esta característica.

-   El nivel 1 admite regiones de incertidumbre de 1/2 píxeles y no se genera ninguna postsnap. Esto es adecuado para la representación en mosaico, un Atlas de textura, la generación de mapas ligeros y las instantáneas de subpíxeles.
-   El nivel 2 agrega las regiones de incertidumbre y 1/256 posteriores a la instantánea. También agrega compatibilidad con la aceleración del algoritmo basado en la CPU (por ejemplo, voxelization).
-   El nivel 3 agrega 1/512 regiones de incertidumbre, cobertura interna de entrada y admite la selección de la oclusión. La cobertura de entrada agrega el nuevo valor `SV_InnerCoverage` al lenguaje de sombreado de alto nivel (HLSL). Se trata de un entero escalar de 32 bits que se puede especificar en la entrada a un sombreador de píxeles y que representa la información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel está totalmente incluido).

## <a name="api-summary"></a>API summary

Los siguientes métodos, estructuras, enumeraciones y clases auxiliares hacen referencia a la rasterización conservadora:

-   [**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estructura que contiene la descripción del rasterizador, anotando la \_ \_ clase auxiliar CD3D12 de rasterizador DESC2 para crear descripciones de rasterizador.
-   [**D3D11 \_ \_ \_ Modo de rasterización conservador**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) : valores de enumeración para el modo (activado o desactivado).
-   [**D3D11 \_ \_Data Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estructura que contiene el nivel de compatibilidad.
-   [**D3D11 \_ \_ \_ Nivel de rasterización conservador**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : valores de enumeración para cada nivel de soporte del hardware.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para tener acceso a las características admitidas.

## <a name="related-topics"></a>Temas relacionados
* [Características de Direct3D 11,3](direct3d-11-3-features.md)