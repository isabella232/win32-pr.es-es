---
title: Uso de datos de características de Direct3D 11 para complementar los niveles de características de Direct3D
description: Descubra cómo comprobar la compatibilidad del dispositivo con características opcionales, incluidas las características que se agregaron en versiones recientes de Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c2e7392f576b8c0dca059a4ef2fdd2ee6415230e5fd41e497d60899332f674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124053"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Uso de datos de características de Direct3D 11 para complementar los niveles de características de Direct3D

Descubra cómo comprobar la compatibilidad del dispositivo con características opcionales, incluidas las características que se agregaron en versiones recientes de Windows.

[Los niveles de características de Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indican conjuntos bien definidos de funcionalidad de GPU que se corresponden aproximadamente con distintas generaciones de hardware gráfico. Esto simplifica enormemente la tarea de comprobar las capacidades de hardware y también proporciona una experiencia coherente en una amplia gama de dispositivos diferentes.

Para tener en cuenta parte de la varianza en las distintas implementaciones de hardware (incluido el hardware heredado, el hardware móvil y el hardware moderno), algunas características se consideran opcionales. La compatibilidad con estas características se puede determinar llamando a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) y suministrando la estructura FEATURE DATA de D3D11 \_ \_ \_ \* pertinente. En este tema se describen las distintas características opcionales de Direct3D 11, cómo algunas de ellas funcionan juntas y cómo puede evitar la comprobación de cada característica opcional única.

## <a name="how-to-check-for-optional-feature-support"></a>Comprobación de la compatibilidad con características opcionales

Llame [**a ID3D11Device::CheckFeatureSupport,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)proporcionando la estructura que representa la característica opcional que le gustaría usar. Si el método devuelve **S \_ OK**, significa que está en una versión del entorno de ejecución de Direct3D que admite la característica opcional. Si devuelve **E \_ INVALIDARG**, significa que está en una versión del entorno de ejecución de Direct3D 11 desde antes de que se agregara la característica opcional; esto significa que la característica opcional no está disponible, junto con cualquier otra característica opcional introducida en la misma versión de Direct3D 11 o posterior.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>¿Puedo minimizar el trabajo necesario para las comprobaciones de compatibilidad de características?

Además de tener el tiempo de ejecución adecuado de Direct3D 11 (normalmente asociado a una versión de Windows), el controlador de gráficos también debe ser lo suficientemente reciente como para admitir la característica opcional. Las especificaciones de WDDM requieren que se admitan características opcionales si el hardware puede admitirlo. Por lo tanto, cuando un controlador de gráficos admite una de las características opcionales que se agregaron en una versión determinada de Windows, normalmente significa que el controlador de gráficos admite las otras características agregadas en esa versión de Windows. Por ejemplo, si un controlador de dispositivo admite sombras en el nivel de característica 9, sabrá que el controlador de dispositivo es al menos WDDM 1.2.

**Nota**  Si un dispositivo Microsoft [](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D admite el nivel de característica 11.1, todas las características opcionales indicadas por [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) se admiten automáticamente, excepto **SAD4ShaderInstructions** y **ExtendedDoublesShaderInstructions**.

El tiempo de ejecución siempre establece las siguientes agrupaciones de miembros de forma idéntica. Es decir, todos los valores de una agrupación son **TRUE** o **FALSE:**

-   **DiscardAPIsSeenByDriver** y **FlagsForUpdateAndCopySeenByDriver**
-   **ClearView,** **CopyWithOverlap,** **ConstantBufferPartialUpdate,** **ConstantBufferOffsetting** y **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** y **MultisampleRTVWithForcedSampleCountOne**

Opciones de nivel **de característica 11.2 ([**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** las características opcionales indicadas por este campo son independientes y deben comprobarse individualmente.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Compatibilidad con características Windows RT dispositivos 8.1 y Windows Phone 8.1

Windows RT tabletas pueden admitir una variedad de niveles de características y características opcionales, están optimizados para un consumo reducido de energía y usan gráficos integrados en lugar de GPU discretas. Windows Las aplicaciones de la tienda para dispositivos ARM deben admitir el nivel de característica 9.1. Las aplicaciones DirectX para Windows RT deben aprovechar las características opcionales que pueden ahorrar energía y ciclos (como la creación de instancias simples) cuando están disponibles.

Windows Phone 8 dispositivos móviles admiten el nivel de característica 9.3 con características opcionales específicas. Consulte [Nivel de característica 9 3 de Direct3D para Windows Phone \_ 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>¿Cuáles son las características opcionales de Direct3D 11?

En el resto de este artículo se describen las características opcionales disponibles en Direct3D 11.2. Las características se describen en orden cronológico por el momento en que se agregaron para que pueda tener una idea de qué características hay en las distintas versiones de Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Compatibilidad opcional del sombreador de proceso con el nivel de característica 10

La siguiente característica siempre está disponible para dispositivos de nivel de característica 10:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** si es **TRUE,** el dispositivo admite sombreadores de proceso. Esto incluye compatibilidad con búferes sin procesar y estructurados.

Cuando el dispositivo de nivel de característica 10 0 o 10 1 admite esta característica, no se garantiza que el dispositivo admita el sombreador de proceso \_ \_ 4.1. Las aplicaciones deben estar preparadas para volver a un sombreador de proceso 4.0 si [**ID3D11Device::CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) produce una excepción con un programa de sombreador de proceso 4.1.

## <a name="optional-capabilities-for-feature-level-9"></a>Funcionalidades opcionales para el nivel de característica 9

Las siguientes características se agregan para el nivel de característica 9 a partir de Windows 8:

**[**OPCIONES D3D11 \_ FEATURE DATA \_ \_ D3D9: \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)** indica compatibilidad con el direccionamiento de textura de encapsulado con texturas que no son de potencia de 2. Si esto es compatible, se puede usar EL ENCAPSULADO DE MODO DE DIRECCIÓN DE TEXTURA D3D11 \_ \_ con \_ \_ dichas texturas.

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indica compatibilidad con muestreadores de comparación en sombreadores de nivel de característica 9 x del modelo de sombreador 4.0. \_ Esto se usa para realizar pruebas de profundidad en sombreadores de píxeles, lo que permite la compatibilidad con técnicas comunes como la asignación de sombras y las galerías de símbolos.

Se agregó la siguiente característica para dispositivos de nivel 9 a partir de Windows 8.1:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indica compatibilidad con características de creación de instancias sencillas que podrían estar disponibles en el hardware de nivel 9 de DirectX. La creación de instancias simple significa que todos los miembros **InstanceDataStepRate** de las estructuras [**D3D11 \_ INPUT ELEMENT \_ \_ DESC usadas**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) para definir el diseño de entrada deben ser iguales a 1. Los dispositivos que admiten el nivel de característica 9.3 o superior ya incluyen compatibilidad total con la creación de instancias.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Compatibilidad opcional de precisión de punto flotante para programas de sombreador

**[**D3D11 \_ FEATURE DATA SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)** los campos de esta estructura indican la longitud de los números de punto flotante cuando se habilita la precisión mínima, o 0 si solo se admite la precisión de punto flotante de 32 bits completa.

En el caso de los dispositivos de nivel de característica 9, la precisión mínima del sombreador de vértices puede ser diferente del sombreador de píxeles. La precisión del sombreador de vértices se indica **en el campo AllOtherShaderStagesMinPrecision.**

**[**D3D11 \_ FEATURE \_ DATA \_ DOUBLES:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** los dispositivos de nivel de característica 11 pueden admitir cálculos de precisión doble dentro de los programas del modelo de sombreador 5.0. La compatibilidad con cálculos de precisión doble dentro del sombreador significa que los valores float se pueden convertir en dobles dentro del programa de sombreador de proceso, lo que proporciona la ventaja de cálculo de mayor precisión dentro de cada paso del sombreador. Los números de precisión doble se deben volver a convertir en floats antes de escribirse en el búfer de salida. Tenga en cuenta que no se admite necesariamente la división de precisión doble.

## <a name="additional-capabilities-for-direct3d-112"></a>Funcionalidades adicionales para Direct3D 11.2

Direct3D 11.2 agrega cuatro nuevas características opcionales que pueden ser compatibles con dispositivos Direct3D 11. Estas características están en la estructura [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)

**TiledResourcesTier:** Indica la compatibilidad con los recursos en mosaico e indica el nivel admitido.

**MinMaxFiltering:** Indica la compatibilidad con las opciones de filtrado D3D11 FILTER MINIMUM y \_ \_ \_ \* D3D11 FILTER MAXIMUM, que comparan el resultado del filtrado con el valor mínimo \_ \_ \_ \* (o máximo). Vea [**D3D11 \_ FILTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Indica compatibilidad para borrar las vistas de recursos de búfer de profundidad.

**MapOnDefaultBuffers:** Indica la compatibilidad con los búferes de destino de representación de asignación creados con la **marca \_ USAGE DEFAULT \_ de D3D11.**

## <a name="tile-based-rendering"></a>Representación basada en mosaicos

**[**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info)** indica si el dispositivo gráfico realiza por lotes los comandos de representación y realiza la representación basada en mosaicos de forma predeterminada. Se puede usar como sugerencia para la optimización del motor de gráficos.

## <a name="optional-features-for-development-and-debugging"></a>Características opcionales para el desarrollo y la depuración

**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS::D iscardAPIsSeenByDriver:** puede supervisar este miembro durante el desarrollo para descartar controladores heredados en hardware donde [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) y [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) podrían haber sido beneficiosos.

COMPATIBILIDAD CON MARCADORES DE DATOS DE CARACTERÍSTICAS **[**D3D11: \_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support)** se admite si el hardware y el controlador admiten el marcado de datos para la generación de perfiles de GPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 