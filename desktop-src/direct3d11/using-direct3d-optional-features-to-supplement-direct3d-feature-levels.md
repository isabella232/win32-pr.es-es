---
title: Usar datos de características de Direct3D 11 para complementar los niveles de características de Direct3D
description: Averigüe cómo comprobar la compatibilidad de dispositivos con características opcionales, incluidas las que se agregaron en las versiones recientes de Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcc770812281ea89e8ebb68065aa68a00e1887d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359126"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Usar datos de características de Direct3D 11 para complementar los niveles de características de Direct3D

Averigüe cómo comprobar la compatibilidad de dispositivos con características opcionales, incluidas las que se agregaron en las versiones recientes de Windows.

[Los niveles de características de Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indican conjuntos bien definidos de funcionalidad de GPU que se corresponden aproximadamente con diferentes generaciones de hardware de gráficos. Esto simplifica en gran medida la tarea de comprobar la capaibilities de hardware y también proporciona una experiencia coherente en una amplia gama de dispositivos diferentes.

Para tener en cuenta algunas de las varianzas en distintas implementaciones de hardware, incluido el hardware heredado, el hardware móvil y el hardware moderno, algunas características se consideran opcionales. La compatibilidad con estas características se puede determinar mediante una llamada a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) y el suministro de la estructura de datos de la característica D3D11 pertinente \_ \_ \_ \* . En este tema se describen las distintas características opcionales de Direct3D 11, cómo funcionan juntas y cómo se puede evitar la comprobación de cada una de las características opcionales.

## <a name="how-to-check-for-optional-feature-support"></a>Cómo comprobar la compatibilidad con características opcionales

Llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), que proporciona la estructura que representa la característica opcional que le gustaría usar. Si el método devuelve **S \_ correcto**, significa que está en una versión del tiempo de ejecución de Direct3D que admite la característica opcional. Si devuelve **E \_ INVALIDARG**, significa que está en una versión del tiempo de ejecución de Direct3D 11 desde antes de que se agregara la característica opcional, lo que significa que la característica opcional no está disponible, junto con cualquier otra característica opcional introducida en la misma versión de Direct3D 11 o posterior.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>¿Se puede minimizar el trabajo necesario para las comprobaciones de compatibilidad de las características?

Además de tener el tiempo de ejecución de Direct3D 11 correcto (normalmente asociado a una versión de Windows), el controlador de gráficos también debe ser lo suficientemente reciente como para admitir la característica opcional. Las especificaciones de WDDM requieren características opcionales que se admitirán si el hardware lo admite. Por tanto, cuando un controlador de gráficos admite una de las características opcionales que se agregaron en una versión determinada de Windows, normalmente significa que el controlador de gráficos admite las demás características agregadas en esa versión de Windows. Por ejemplo, si un controlador de dispositivo admite sombras en el nivel de característica 9, sabrá que el controlador de dispositivo es al menos WDDM 1,2.

**Nota:**    Si un dispositivo de Microsoft Direct3D admite el [nivel de características](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, todas las características opcionales indicadas por [**\_ \_ \_ \_ las opciones de D3D11 de datos de características de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) se admiten automáticamente excepto **SAD4ShaderInstructions** y **ExtendedDoublesShaderInstructions**.

El tiempo de ejecución siempre establece las siguientes agrupaciones de miembros de forma idéntica. Es decir, todos los valores de una agrupación son **true** o **false** juntos:

-   **DiscardAPIsSeenByDriver** y **FlagsForUpdateAndCopySeenByDriver**
-   **Clearview**, **CopyWithOverlap**, **ConstantBufferPartialUpdate**, **ConstantBufferOffsetting** y **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** y **MultisampleRTVWithForcedSampleCountOne**

**Opciones de nivel de características 11,2 ([**D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** las características opcionales que se indican en este campo son independientes y deben comprobarse de forma individual.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Compatibilidad de características en dispositivos Windows RT 8,1 y Windows Phone 8,1

Los dispositivos de tableta de Windows RT pueden admitir diversos niveles de características y características opcionales, están optimizados para reducir el consumo de energía y usan gráficos integrados en lugar de GPU discretas. Las aplicaciones de la tienda Windows para dispositivos ARM deben admitir el nivel de características 9,1. Las aplicaciones de DirectX para Windows RT deben aprovechar las características opcionales que pueden ahorrar energía y ciclos, como la creación de instancias simples, cuando están disponibles.

Windows Phone 8 dispositivos móviles admiten el nivel de características 9,3 con características opcionales específicas. Consulte [nivel de características de Direct3D 9 \_ 3 para Windows Phone 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>¿Cuáles son las características opcionales de Direct3D 11?

En el resto de este artículo se describen las características opcionales disponibles en Direct3D 11,2. Las características se describen en orden cronológico por cuando se agregaron para que pueda tener una idea de qué características se encuentran en versiones diferentes de Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Compatibilidad con el sombreador de cálculo opcional para el nivel de característica 10

La característica siguiente siempre está disponible para los dispositivos de nivel de característica 10:

**[**D3D11 \_ D3D10 de datos de características \_ \_ \_ X \_ \_ Opciones de hardware**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** si es **true**, el dispositivo admite los sombreadores de cálculo. Esto incluye compatibilidad con búferes sin formato y estructurados.

Cuando el dispositivo de nivel de característica 10 \_ 0 o 10 \_ 1 es compatible con esta característica, no se garantiza que el dispositivo admita el sombreador de cálculo 4,1. Las aplicaciones deben estar preparadas para revertir a un sombreador de cálculo 4,0 si [**ID3D11Device:: CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) produce una excepción con un programa del sombreador de cálculo 4,1.

## <a name="optional-capabilities-for-feature-level-9"></a>Funcionalidades opcionales para el nivel de características 9

Se han agregado las siguientes características para el nivel de característica 9 a partir de Windows 8:

**[**\_ Opciones de \_ \_ D3D9 de \_ datos de características de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** indica compatibilidad para ajustar el direccionamiento de textura con texturas que no son de potencia de 2. Si se admite, se \_ \_ \_ \_ puede usar el ajuste de modo de dirección de textura D3D11 con estas texturas.

**[**\_ \_ \_ \_ \_ Compatibilidad con D3D11 de datos de características de D3D9**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indica compatibilidad con los ejemplos de comparación en los sombreadores de nivel de característica 4,0 de nivel de función \_ . Se usa para realizar pruebas de profundidad en sombreadores de píxeles, lo que permite la compatibilidad con técnicas comunes como la asignación de instantáneas y las galerías de símbolos.

Se ha agregado la siguiente característica a los dispositivos de nivel de característica 9 a partir de Windows 8.1:

**[**\_ \_ \_ \_ \_ \_ Compatibilidad con la creación de instancias de D3D11 de datos de características D3D9**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indica compatibilidad con las características de creación de instancias simples que podrían estar disponibles en el hardware de nivel 9 de DirectX. La creación de instancias simple significa que todos los miembros de **InstanceDataStepRate** de las estructuras [**DESC del \_ \_ elemento \_ de entrada D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) usadas para definir el diseño de entrada deben ser iguales a 1. Los dispositivos que admiten el nivel de características 9,3 o superior ya incluyen compatibilidad total con la creación de instancias.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Compatibilidad de precisión de punto flotante opcional para programas de sombreador

**[**\_ Compatibilidad de \_ \_ \_ \_ precisión \_ mínima del sombreador de datos de características de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** los campos de este struct indican la longitud de los números de punto flotante cuando la precisión mínima está habilitada, o 0 si solo se admite la precisión de punto flotante de 32 bits completa.

En el caso de los dispositivos de nivel de característica 9, la precisión mínima del sombreador de vértices puede ser diferente del sombreador de píxeles. La precisión del sombreador de vértices se indica en el campo **AllOtherShaderStagesMinPrecision** .

**[**D3D11 \_ de \_ datos \_ de características dobles**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles):** los dispositivos de nivel de característica 11 pueden admitir cálculos de precisión doble en los programas del modelo de sombreador 5,0. La compatibilidad con los cálculos de precisión doble dentro del sombreador significa que los valores float se pueden convertir en valores double en el programa del sombreador de cálculo, lo que proporciona la ventaja de un cálculo de precisión mayor en cada paso del sombreador. Los números de precisión doble deben volver a convertirse en valores Float antes de que se escriban en el búfer de salida. Tenga en cuenta que no se admite necesariamente la división de precisión doble.

## <a name="additional-capabilities-for-direct3d-112"></a>Funcionalidades adicionales para Direct3D 11,2

Direct3D 11,2 agrega cuatro nuevas características opcionales que pueden ser compatibles con dispositivos Direct3D 11. Estas características se encuentran en la [**D3D11 de datos de características de \_ \_ \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) :

**TiledResourcesTier:** Indica la compatibilidad con los recursos en mosaico e indica el nivel de nivel admitido.

**MinMaxFiltering:** Indica compatibilidad con \_ \_ \_ \* las opciones de filtrado máximo y D3D11 del filtro D3D11, que comparan \_ \_ \_ \* el resultado del filtrado con el valor mínimo (o máximo). Vea [**\_ filtro D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Indica compatibilidad para borrar vistas de recursos de búfer de profundidad.

**MapOnDefaultBuffers:** Indica la compatibilidad con la asignación de búferes de destino de representación creados con la marca **\_ \_ predeterminada de uso de D3D11** .

## <a name="tile-based-rendering"></a>Representación basada en mosaicos

**[**\_ Información de \_ \_ arquitectura de \_ datos de características de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** indica si el dispositivo gráfico procesa los comandos de representación por lotes y realiza la representación basada en mosaicos de forma predeterminada. Se puede usar como una sugerencia para la optimización del motor de gráficos.

## <a name="optional-features-for-development-and-debugging"></a>Características opcionales para el desarrollo y la depuración

**D3D11 \_ Opciones de D3D11 de datos de características \_ \_ \_ ::D iscardapisseenbydriver:** puede supervisar este miembro durante el desarrollo para descartar controladores heredados en hardware donde [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) y [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) podrían haber sido beneficiosos.

**[**\_ \_ \_ \_ Compatibilidad con el marcador de datos de características de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** se admite si el hardware y el controlador admiten el marcado de datos para la generación de perfiles de GPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 