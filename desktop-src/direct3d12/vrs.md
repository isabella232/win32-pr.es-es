---
title: Sombreado de velocidad variable (VRS)
description: El sombreado de velocidad variable o el sombreado de píxeles general es un mecanismo que le permite asignar rendimiento o potencia de representación a velocidades que varían en la &mdash; &mdash; imagen representada.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: b26d2d67a6e4a5f7b599a9fc65f324b301346fde3170262e80235a25f8cfb88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045330"
---
# <a name="variable-rate-shading-vrs"></a>Sombreado de velocidad variable (VRS)

## <a name="the-motivation-for-vrs"></a>La motivación de VRS
Debido a las restricciones de rendimiento, un representador de gráficos no siempre puede permitirse ofrecer el mismo nivel de calidad a cada parte de su imagen de salida. El sombreado de velocidad variable o el sombreado de píxeles general es un mecanismo que le permite asignar rendimiento o potencia de representación a velocidades que varían en la &mdash; &mdash; imagen representada.

En algunos casos, la velocidad de sombreado se puede reducir con poca o ninguna reducción en la calidad de salida perceptible; lo que conduce a una mejora del rendimiento que es básicamente gratuita.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Sin suavizado de alias de varios ejemplos de VRS &mdash; con supermuestreo
Sin sombreado de velocidad variable, el único medio de controlar la tasa de sombreado es con suavizado de alias de varias muestras (MSAA) con ejecución basada en muestras (también conocida como supermuestreo).

MSAA es un mecanismo para reducir el alias geométrico y mejorar la calidad de representación de una imagen en comparación con no usar MSAA. El recuento de muestras de MSAA, que puede ser 1x, 2x, 4x, 8x o 16x, rige el número de muestras asignadas por píxel de destino de representación. El recuento de muestras de MSAA debe conocerse por adelantado cuando se asigna el destino y no se puede cambiar a partir de entonces.

El supermuestreo hace que el sombreador de píxeles se invoque una vez por muestra, con una mayor calidad, pero también un mayor costo de rendimiento en comparación con la ejecución por píxel.

La aplicación puede controlar su velocidad de sombreado eligiendo entre la ejecución basada en píxeles o MSAA con supermuestreo. Estas dos opciones no proporcionan un control muy preciso. Además, es posible que desee una velocidad de sombreado inferior para una determinada clase de objetos en comparación con el resto de la imagen. Estos objetos pueden incluir un objeto detrás de un elemento HUD, o una transparencia, un desenfoque (profundidad de campo, movimiento, etc.) o una distorsión óptica debido a la óptica vr. Pero eso no sería posible, porque la calidad y los costos del sombreado se fijan en toda la imagen.

## <a name="with-variable-rate-shading-vrs"></a>Con sombreado de velocidad variable (VRS)
El modelo de sombreado de velocidad variable (VRS) extiende el supermuestreo con MSAA en la dirección opuesta, "píxel gruesa", agregando el concepto de sombreado general. Aquí es donde el sombreado se puede realizar con una frecuencia más gruesa que un píxel. En otras palabras, un grupo de píxeles se puede sombrear como una sola unidad y, a continuación, el resultado se difunde a todos los ejemplos del grupo.

Una API de sombreado general permite a la aplicación especificar el número de píxeles que pertenecen a un grupo sombreado o *píxeles gruesos.* Puede variar el tamaño de píxel general después de asignar el destino de representación. Por lo tanto, diferentes partes de la pantalla o diferentes pases de dibujo pueden tener diferentes velocidades de sombreado.

Esta es una tabla que describe qué nivel de MSAA se admite con qué tamaño de píxel general. Algunos no se admiten en ninguna plataforma; mientras que otras se habilitan condicionalmente en función de una funcionalidad *(AdditionalShadingRatesSupported),* indicada por "Cap".

![En la tabla se muestra el tamaño de píxel general para los niveles de M S A.](images/CoarsePixelSizeSupport.PNG "Tamaños de píxeles gruesos")

Para los niveles de características que se deban analizar en la sección siguiente, no hay ninguna combinación general de tamaño de píxel y recuento de muestras, donde el hardware necesita realizar un seguimiento de más de 16 muestras por invocación del sombreador de píxeles. Esas combinaciones están sombreadas por medio tono en la tabla anterior.

## <a name="feature-tiers"></a>Niveles de características
Hay dos niveles para la implementación de VRS y dos funcionalidades que puede consultar. Cada nivel se describe con más detalle después de la tabla.

![En la tabla se muestran las características disponibles en los niveles 1 y 2.](images/Tiers.PNG "Niveles de VRS")

### <a name="tier-1"></a>Nivel 1
- La velocidad de sombreado solo se puede especificar por dibujo; no es más granular que eso.
- La velocidad de sombreado se aplica uniformemente a lo que se dibuja independientemente de dónde se encuentra dentro del destino de representación.

### <a name="tier-2"></a>Nivel 2
- La velocidad de sombreado se puede especificar por dibujo, como en el nivel 1. También se puede especificar mediante una combinación de base por dibujo y de:
  - Semántica de cada vértice que provoca y
  - una imagen de espacio de pantalla.
- Las tasas de sombreado de los tres orígenes se combinan mediante un conjunto de combinadores.
- El tamaño del icono de la imagen de espacio en pantalla es de 16 x 16 o más pequeño.
- Se garantiza que la tasa de sombreado solicitada por la aplicación se entrega exactamente (para la precisión de los filtros temporales y otros filtros de reconstrucción).
- SV_ShadingRate se admite la entrada ps.
- La velocidad de sombreado por vértice de provoking (también conocida como por primitiva), es válida cuando se usa una ventanilla y no se `SV_ViewportArrayIndex` escribe en ella.
- La velocidad por provoking-vertex se puede usar con más de una ventanilla si la funcionalidad *SupportsPerVertexShadingRateWithMultipleViewports* está establecida en `true` . Además, en ese caso, esa velocidad se puede usar cuando `SV_ViewportArrayIndex` se escribe en .

### <a name="list-of-capabilities"></a>Lista de capacidades
- *AdditionalShadingRatesSupported*
  - Tipo booleano.
  - Indica si se admiten tamaños de píxeles anchos de 2x4, 4x2 y 4x4 para la representación de una sola muestra; y si el tamaño de píxel general 2x4 es compatible con 2x MSAA.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Tipo booleano.
  - Indica si se puede usar más de una ventanilla con la velocidad de sombreado por vértice (también conocida como por primitiva).

## <a name="specifying-shading-rate"></a>Especificación de la velocidad de sombreado
Para mayor flexibilidad en las aplicaciones, se proporcionan diversos mecanismos para controlar la velocidad de sombreado. Hay diferentes mecanismos disponibles en función del nivel de característica de hardware.

### <a name="command-list"></a>Lista de comandos
Este es el mecanismo más sencillo para establecer la velocidad de sombreado. Está disponible en todos los niveles.

La aplicación puede especificar un tamaño de píxel general mediante el método [ **ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Esa API toma un único argumento de enumeración. La API proporciona un control general del nivel de calidad para representar la capacidad de establecer la velocidad de sombreado &mdash; por dibujo.

Los valores para este estado se expresan a través de la [**enumeración D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) datos.

#### <a name="coarse-pixel-size-support"></a>Compatibilidad con el tamaño de píxel general
Las tasas de sombreado 1x1, 1x2, 2x2 y 2x2 se admiten en todos los niveles.

Hay una funcionalidad, *AdditionalShadingRatesSupported,* para indicar si se admiten 2x4, 4x2 y 4x4 en el dispositivo.

### <a name="screen-space-image-image-based"></a>Imagen de espacio de pantalla (basada en imágenes)
En el nivel 2 y superior, puede especificar la velocidad de sombreado de píxeles con una imagen de espacio en pantalla.

La imagen de espacio en pantalla permite a la aplicación crear una imagen de "máscara de nivel de detalle (LOD)" que indica regiones de distinta calidad, como áreas que se cubrirán con desenfoque de movimiento, desenfoque de profundidad de campo, objetos transparentes o elementos de la interfaz de usuario de HUD. La resolución de la imagen está en macrobloqueos; no está en la resolución del destino de representación. En otras palabras, los datos de velocidad de sombreado se especifican con una granularidad de mosaicos de 8 x 8 o 16 x 16 píxeles, como se indica en el tamaño del icono VRS.

#### <a name="tile-size"></a>Tamaño de mosaico
La aplicación puede consultar una API para recuperar el tamaño de icono de VRS admitido para su dispositivo.

Los mosaicos son cuadrados y el tamaño hace referencia al ancho o alto del icono en texturas.

Si el hardware no admite el sombreado de velocidad variable de nivel 2, la consulta de funcionalidad para el tamaño del icono devuelve 0.

Si el hardware *admite el* sombreado de velocidad variable de nivel 2, el tamaño del icono es uno de estos valores.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Tamaño de la imagen de espacio de pantalla
Para un destino de representación de tamaño {rtWidth, rtHeight}, con un tamaño de mosaico determinado denominado **VRSTileSize,** la imagen de espacio de pantalla que la cubrirá es de estas dimensiones.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

La parte superior izquierda de la imagen de espacio de pantalla (0, 0) está bloqueada en la parte superior izquierda del destino de representación (0, 0).

Para buscar la coordenada (x,y) de un icono que se corresponda con una ubicación determinada en el destino de representación, divida las coordenadas de espacio de ventana de (x, y) por el tamaño del icono, omitiendo los bits fraccionales.

Si la imagen de espacio en pantalla es mayor de lo necesario para un destino de representación determinado, no se usan las partes adicionales de la derecha o inferior.

Si la imagen de espacio en pantalla es demasiado pequeña para un destino de representación determinado, cualquier intento de lectura de la imagen más allá de sus extensiones reales produce una velocidad de sombreado predeterminada de 1x1. Esto se debe a que la parte superior izquierda de la imagen de espacio en pantalla (0, 0) está bloqueada en la parte superior izquierda del destino de representación (0, 0) y "leer más allá de las extensiones de destino de representación" significa leer demasiado grandes valores para x e y.

#### <a name="format-layout-resource-properties"></a>Formato, diseño, propiedades de recursos
El formato de esta superficie es una superficie de 8 bits de canal único [**(DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

El recurso es la dimensión **TEXTURE2D.**

No se puede matriz ni se puede micar. Debe tener explícitamente un nivel mip.

Tiene el recuento de muestras 1 y la calidad de la muestra 0.

Tiene el diseño de textura **UNKNOWN**. Implícitamente no puede ser un diseño de fila principal, porque no se permite el adaptador cruzado.

La manera esperada en que se rellenan los datos de la imagen del espacio de pantalla es:
1. Escribir los datos mediante un sombreador de proceso; la imagen de espacio de pantalla está enlazada como un UAV, o
2. Copie los datos en la imagen de espacio en pantalla.

Al crear la imagen de espacio en pantalla, se permiten estas marcas.

- Ninguno
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

No se permiten estas marcas.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

El tipo de montón del recurso no puede ser UPLOAD ni READBACK.

El recurso no se puede SIMULTANEOUS_ACCESS. No se permite que el recurso sea entre adaptadores.

#### <a name="data"></a>data
Cada byte de la imagen de espacio en pantalla corresponde a un valor de la [**enumeración D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  pantalla.

#### <a name="resource-state"></a>Estado del recurso
Un recurso debe pasar a un estado de solo lectura cuando se usa como una imagen de espacio en pantalla. Un estado de solo [**lectura, D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states), se define para este propósito.

El recurso de imagen se pasa fuera de ese estado para volver a escribirse.

#### <a name="setting-the-image"></a>Establecimiento de la imagen
La imagen de espacio de pantalla para especificar la velocidad del sombreador se establece en la lista de comandos.

Un recurso que se ha establecido como origen de velocidad de sombreado no se puede leer ni escribir desde ninguna fase del sombreador.

Se puede establecer una imagen de espacio `null` de pantalla para especificar la velocidad del sombreador. Esto tiene el efecto de que 1x1 se usa de forma coherente como contribución de la imagen de espacio en pantalla. Inicialmente, se puede considerar que la imagen de espacio de pantalla está establecida en `null` .

#### <a name="promotion-and-decay"></a>Promoción y decadencia
Un recurso de imagen de espacio de pantalla no tiene ninguna implicación especial con respecto a la promoción o decadencia.

### <a name="per-primitive-attribute"></a>Atributo por primitiva
Un atributo por primitivo agrega la capacidad de especificar un término de velocidad de sombreado como atributo de un vértice que provoca. Este atributo tiene sombreado plano, es decir, se propaga a todos los píxeles del triángulo o primitivo &mdash; de línea actual. El uso de un atributo por primitivo puede permitir un control más preciso de la calidad de la imagen en comparación con los otros especificadores de velocidad de sombreado.

El atributo por primitivo es una semántica configurable denominada `SV_ShadingRate` . `SV_ShadingRate`existe como parte del modelo [de sombreador HLSL 6.4.](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12)

Si un vs o GS establece , pero `SV_ShadingRate` VRS no está habilitado, la configuración semántica no tiene ningún efecto. Si no se especifica ningún valor para por primitiva, se asume un valor de tasa de sombreado de 1x1 como contribución por `SV_ShadingRate` primitiva.

### <a name="combining-shading-rate-factors"></a>Combinación de factores de velocidad de sombreado
Los distintos orígenes de la velocidad de sombreado se aplican en secuencia mediante este diagrama.

![En el diagrama se muestra un estado de canalización, con la etiqueta A, con provoking vertex shading rate (Provoking vertex shading rate), con la etiqueta B, aplicada a un combinador y, a continuación, la velocidad de sombreado basada en imágenes, etiquetada como B, aplicada en un combinador.](images/Combiners.PNG "Combinadores de sombreado")

Cada par de A y B se combina mediante un combinador.

\* Al especificar una tasa de sombreador por atributo de vértice.

- Si se usa un sombreador de geometría, la velocidad de sombreado se puede especificar a través de eso.
- Si no se usa un sombreador de geometría, el vértice que invoca especifica la velocidad de sombreado.

#### <a name="list-of-combiners"></a>Lista de combinadores
Se admiten los siguientes combinadores. Usar un combinador (C) y dos entradas (A y B).

- **Paso a través.** C.xy = A.xy.
- **Invalide**. C.xy = B.xy.
- **Mayor calidad.** C.xy = min(A.xy, B.xy).
- **De menor calidad.** C.xy = max(A.xy, B.xy).
- **Aplique el costo B con respecto a A**. C.xy = min(maxRate, A.xy + B.xy).

donde `maxRate` es la mayor dimensión permitida de píxeles gruesos en el dispositivo. Esto sería

- **D3D12_AXIS_SHADING_RATE_2X** (es decir, un valor de 1), si AdditionalShadingRatesSupported es `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (es decir, un valor de 2), si AdditionalShadingRatesSupported es `true` .

La elección del combinador para el sombreado de velocidad variable se establece en la lista de comandos a través de [**ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Si no se establece ningún combinador, permanecen en el valor predeterminado, que es PASSTHROUGH.

Si el origen de un combinador es un D3D12_AXIS_SHADING_RATE [**,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)que no se permite en la tabla de  compatibilidad, la entrada se sanitiza a una velocidad de sombreado admitida.

Si la salida de un combinador no se corresponde con una velocidad de sombreado admitida en la plataforma, el resultado se sanitiza a una velocidad de sombreado que *se* admite.

### <a name="default-state-and-state-clearing"></a>Estado predeterminado y borrado de estado
Todos los orígenes de velocidad de sombreado, es

- la velocidad especificada por el estado de canalización (especificada en la lista de comandos),
- la velocidad especificada por la imagen del espacio de pantalla, y
- el atributo por primitivo

tienen un valor predeterminado **de D3D12_SHADING_RATE_1X1**. Los combinadores predeterminados son {PASSTHROUGH, PASSTHROUGH}.

Si no se especifica ninguna imagen de espacio de pantalla, se deduce una velocidad de sombreado de 1x1 desde ese origen.

Si no se especifica ningún atributo por primitivo, se deduce una tasa de sombreado de 1x1 desde ese origen.

[ID3D12CommandList::ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) restablece la velocidad especificada por el estado de canalización al valor predeterminado y la selección de la imagen de espacio de pantalla en el valor predeterminado de "no screen-space image".

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Consulta de la velocidad de sombreado mediante SV_ShadingRate
Es útil saber qué velocidad de sombreado seleccionó el hardware en cualquier invocación de sombreador de píxeles determinada. Esto podría habilitar una variedad de optimizaciones en el código de PS. Una variable del sistema solo PS, `SV_ShadingRate` , proporciona información sobre la velocidad de sombreado.

### <a name="type"></a>Tipo
El tipo de esta semántica es uint.

### <a name="data-interpretation"></a>Interpretación de los datos
Los datos se interpretan como un valor de la [**enumeración D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) datos.

### <a name="if-vrs-is-not-being-used"></a>Si no se usa VRS
Si no se usa el sombreado de píxeles general, se leen como un valor de `SV_ShadingRate` 1x1, lo que indica píxeles finos.

### <a name="behavior-under-sample-based-execution"></a>Comportamiento en la ejecución basada en muestras
Un sombreador de píxeles produce un error de compilación si introduce y también usa la ejecución basada en muestras, por ejemplo, al introducir o usar la palabra clave `SV_ShadingRate` &mdash; de `SV_SampleIndex` interpolación de ejemplo.

> ### <a name="remarks-on-deferred-shading"></a>Comentarios sobre el sombreado aplazado
>
> Es posible que los pases de iluminación de una aplicación de sombreado diferido necesiten saber qué velocidad de sombreado se usó para qué área de la pantalla. Esto es para que los envíos de pases de iluminación se puedan iniciar a una velocidad más general. La `SV_ShadingRate` variable se puede usar para lograr esto si se escribe en el gbuffer.

## <a name="depth-and-stencil"></a>Profundidad y galería de símbolos
Cuando se usa el sombreado de píxeles general, la profundidad y la galería de símbolos y la cobertura siempre se calculan y emiten a la resolución de ejemplo completa.

## <a name="using-the-shading-rate-requested"></a>Uso de la velocidad de sombreado solicitada
Para todos los niveles, se espera que si se solicita una velocidad de sombreado y se admite en la combinación de nivel de dispositivo y MSAA, esa es la velocidad de sombreado que entrega el hardware.

Una tasa de sombreado solicitada significa una velocidad de sombreado calculada como salida de los combinadores (vea la sección Combinación de [factores](#combining-shading-rate-factors) de velocidad de sombreado de este tema).

Una velocidad de sombreado admitida es 1x1, 1x2, 2x1 o 2x2 en una operación de representación en la que el recuento de muestras es menor o igual que cuatro. Si la *funcionalidad AdditionalShadingRatesSupported* es , también se admiten tasas de sombreado de `true` 2x4, 4x2 y 4x4 para algunos recuentos de ejemplo (consulte la tabla de la sección Con sombreado de velocidad [variable (VRS)](#with-variable-rate-shading-vrs) de este tema).

## <a name="screen-space-derivatives"></a>Derivados del espacio de pantalla
Los cálculos de degradados de píxel a píxel adyacente se ven afectados por el sombreado de píxeles general. Por ejemplo, cuando se usan 2 x 2 píxeles anchos, un degradado tendrá el doble de tamaño que cuando no se usen píxeles anchos. Es posible que la aplicación quiera ajustar los sombreadores para compensarlo o no, en &mdash; función de la funcionalidad que desee.

Dado que los mips se eligen en función de un derivado del espacio de pantalla, el uso del sombreado de píxeles general afecta a la selección de mip. El uso del sombreado de píxeles gruesos hace que se seleccionen mips menos detallados en comparación con cuando no se usan píxeles gruesos.

## <a name="attribute-interpolation"></a>Interpolación de atributos
Las entradas de un sombreador de píxeles se pueden interpolar en función de sus vértices de origen. Dado que el sombreado de velocidad variable afecta a las áreas del destino escritas por cada invocación del sombreador de píxeles, interactúa con la interpolación de atributos. Los tres tipos de interpolación son center, centroid y sample.

### <a name="center"></a>Center
La ubicación central de interpolación de un píxel grueso es el centro geométrico del área de píxeles gruesa completa. `SV_Position` siempre se interpola en el centro de la región de píxeles gruesas.

### <a name="centroid"></a>Centroide
Cuando se usa el sombreado de píxeles general con MSAA, para cada píxel fino todavía se escribirá en el número completo de muestras asignadas para el nivel MSAA del destino. Por lo tanto, la ubicación de interpolación de centroide considerará todas las muestras de píxeles finos dentro de píxeles anchos. Dicho esto, la ubicación de interpolación de centroide se define como la primera muestra cubierta, en orden creciente de índice de muestra. La cobertura efectiva de la muestra es AND-ed con el bit correspondiente del estado de rasterizador SampleMask.

> [!NOTE]
> Cuando se usa el sombreado de píxeles general en el nivel 1, SampleMask siempre es una máscara completa. Si SampleMask está configurado para no ser una máscara completa, el sombreado de píxeles general se deshabilita en el nivel 1.

### <a name="sample-based-execution"></a>Ejecución basada en muestras
La ejecución basada en muestras o el supermuestreo causado por el uso de la característica de interpolación de ejemplo se puede usar con sombreado de píxeles general y hace que se invoque el sombreador de píxeles por &mdash; &mdash; muestra. Para los destinos del recuento de muestras N, el sombreador de píxeles se invoca N veces por píxel fino.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Los intrínsecos del modelo de extracción no son compatibles con el sombreado de píxeles general en el nivel 1. Si se intenta usar intrínsecos del modelo de extracción con sombreado de píxeles general en el nivel 1, el sombreado de píxeles general se deshabilita automáticamente.

El `EvaluateAttributeSnapped` intrínseco se puede usar con sombreado de píxeles general en el nivel 2. Su sintaxis es la misma que siempre ha sido.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Para el contexto, `EvaluateAttributeSnapped` tiene un parámetro de desplazamiento con dos campos. Cuando se usa sin sombreado de píxeles general, solo se usan los cuatro bits de orden inferior del total de treinta y dos. Estos cuatro bits representan el intervalo [-8, 7]. Este intervalo abarca una cuadrícula de 16 x 16 dentro de un píxel. El intervalo es tal que se incluyen los bordes superior e izquierdo del píxel, y los bordes inferior y derecho no. Offset (-8, -8) está en la esquina superior izquierda y offset (7, 7) está en la esquina inferior derecha. Desplazamiento (0, 0) es el centro del píxel.

Cuando se usa con sombreado de píxeles general, el parámetro offset de es capaz de `EvaluateAttributeSnapped` especificar un intervalo más amplio de ubicaciones. El parámetro offset selecciona una cuadrícula de 16 x 16 para cada píxel fino y hay varios píxeles finos. El intervalo expressible y el número de bits que se usan dependen del tamaño de píxel general. Se incluyen los bordes superior e izquierdo del píxel grueso, y los bordes inferior y derecho no.

En la tabla siguiente se describe la interpretación del parámetro `EvaluateAttributeSnapped` offset para cada tamaño de píxel general.

#### <a name="evaluateattributesnappeds-offset-range"></a>Intervalo de desplazamiento de EvaluateAttributeSnapped

|Tamaño de píxel general  |Intervalo indexable             |Tamaño del intervalo representable  |Número de bits necesarios {x, y}  |Máscara binaria de bits utilizables          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (bien)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{000000000000xxxx, 00000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{000000000000xxxx, 0000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{00000000000xxxxx, 00000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|2x4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4 x 4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

Las tablas siguientes son una guía para la conversión de la representación de punto fijo a decimal y fraccional. El primer bit utilizable de la máscara binaria es el bit de signo y el resto de la máscara binaria consta de la parte numérica.

El esquema de número para los valores de cuatro bits pasados a `EvaluateAttributeSnapped` no es específico del sombreado de velocidad variable. Se repite aquí para que sea completa.

Para valores de cuatro bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|         1000 |-0,5f     |-8 / 16     |
|         1001 |-0,4375f  |-7 / 16|    |
|         1010 |-0,375f   |-6 / 16|    |
|         1011 |-0,3125f  |-5 / 16     |
|         1100 |-0,25f    |-4 / 16     |
|         1101 |-0,1875f  |-3 / 16     |
|         1110 |-0,125f   |-2 / 16     |
|         1111 |-0,0625f  |-1 /16      |
|         0000 |0,0f      |0 / 16      |
|         0001 |-0,0625f  |1 / 16      |
|         0010 |-0,125f   |2 / 16      |
|         0011 |-0,1875f  |3 / 16      |
|         0100 |-0,25f    |4 / 16      |
|         0101 |-0,3125f  |5 / 16      |
|         0110 |-0,375f   |6 / 16      |
|         0111 |-0,4375f  |7 / 16      |

Para valores de cinco bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16 / 16    |
|        10001 |-0.9375   |-15 / 16    |
|        10010 |-0.875    |-14 / 16    |
|        10011 |-0.8125   |-13 / 16    |
|        10100 |-0.75     |-12 / 16    |
|        10101 |-0.6875   |-11 / 16    |
|        10110 |-0.625    |-10 / 16    |
|        10111 |-0.5625   |-9 / 16     |
|        11000 |-0,5      |-8 / 16     |
|        11001 |-0.4375   |-7 / 16     |
|        11010 |-0.375    |-6 / 16     |
|        11011 |-0.3125   |-5 / 16     |
|        11100 |-0.25     |-4 / 16     |
|        11101 |-0.1875   |-3 / 16     |
|        11110 |-0.125    |-2 / 16     |
|        11111 |-0.0625   |-1 / 16     |
|        00000 |0         |0 / 16      |
|        00001 |0.0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0.1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0.3125    |5 / 16      |
|        00110 |0.375     |6 / 16      |
|        00111 |0.4375    |7 / 16      |
|        01000 |0,5       |8 / 16      |
|        01001 |0.5625    |9 / 16      |
|        01010 |0.625     |10 / 16     |
|        01011 |0.6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0.8125    |13 / 16     |
|        01110 |0.875     |14 / 16     |
|        01111 |0.9375    |15 / 16     |

Para valores de seis bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32 / 16    |
|       100001 |-1.9375   |-31 / 16    |
|       100010 |-1.875    |-30 / 16    |
|       100011 |-1.8125   |-29 / 16    |
|       100100 |-1.75     |-28 / 16    |
|       100101 |-1.6875   |-27 / 16    |
|       100110 |-1.625    |-26 / 16    |
|       100111 |-1.5625   |-25 / 16    |
|       101000 |-1.5      |-24 / 16    |
|       101001 |-1.4375   |-23 / 16    |
|       101010 |-1.375    |-22 / 16    |
|       101011 |-1.3125   |-21 / 16    |
|       101100 |-1.25     |-20 / 16    |
|       101101 |-1.1875   |-19 / 16    |
|       101110 |-1.125    |-18 / 16    |
|       101111 |-1.0625   |-17 / 16    |
|       110000 |-1        |-16 / 16    |
|       110001 |-0.9375   |-15 / 16    |
|       110010 |-0.875    |-14 / 16    |
|       110011 |-0.8125   |-13 / 16    |
|       110100 |-0.75     |-12 / 16    |
|       110101 |-0.6875   |-11 / 16    |
|       110110 |-0.625    |-10 / 16    |
|       110111 |-0.5625   |-9 / 16     |
|       111000 |-0,5      |-8 / 16     |
|       111001 |-0.4375   |-7 / 16     |
|       111010 |-0.375    |-6 / 16     |
|       111011 |-0.3125   |-5 / 16     |
|       111100 |-0.25     |-4 / 16     |
|       111101 |-0.1875   |-3 / 16     |
|       111110 |-0.125    |-2 / 16     |
|       111111 |-0.0625   |-1 / 16     |
|       000000 |0         |0 / 16      |
|       000001 |0.0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0.1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0.3125    |5 / 16      |
|       000110 |0.375     |6 / 16      |
|       000111 |0.4375    |7 / 16      |
|       001000 |0,5       |8 / 16      |
|       001001 |0.5625    |9 / 16      |
|       001010 |0.625     |10 / 16     |
|       001011 |0.6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0.8125    |13 / 16     |
|       001110 |0.875     |14 / 16     |
|       001111 |0.9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1.0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1.1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1.3125    |21 / 16     |
|       010110 |1.375     |22 / 16     |
|       010111 |1.4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1.5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1.6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1.8125    |29 / 16     |
|       011110 |1.875     |30 / 16     |
|       011111 |1.9375    |31 / 16     |

De la misma manera que con los píxeles finos, la cuadrícula de ubicaciones evaluables se centra en el centro de píxeles general cuando se usa sombreado `EvaluateAttributeSnapped` de píxeles general.

## <a name="setsamplepositions"></a>SetSamplePositions
Cuando se usa la API [**ID3D12GraphicsCommandList1::SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) con sombreado general, la API establece las posiciones de ejemplo para píxeles finos.

## <a name="sv_coverage"></a>SV_Coverage
Si se declara como una entrada o salida de sombreador en el nivel 1, se deshabilita el `SV_Coverage` sombreado de píxeles general.

Puede usar la semántica con sombreado de píxeles general en el nivel 2 y refleja qué muestras de un destino `SV_Coverage` MSAA se escriben.

Cuando se usa el sombreado de píxeles general, lo que permite que varios píxeles de origen conste un icono, la máscara de cobertura representa todas las muestras que &mdash; &mdash; proceden de ese icono.

Dada la compatibilidad del sombreado de píxeles general con MSAA, el número de bits de cobertura necesarios para especificarse puede variar. Por ejemplo, con un recurso MSAA 4x que usa [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate), cada píxel grueso escribe en cuatro píxeles finos y cada píxel fino tiene cuatro ejemplos. Esto significa que cada píxel general escribe en un total de 4 * 4 = 16 muestras.

### <a name="number-of-coverage-bits-needed"></a>Número de bits de cobertura necesarios
En la tabla siguiente se indica cuántos bits de cobertura se necesitan para cada combinación de tamaño de píxel general y nivel de MSAA.

![En la tabla se muestra el tamaño de píxeles general, el número de píxeles finos y los niveles de M S A A.](images/NumberOfCoverageBits.PNG "Bits de cobertura")

Como se indica en la tabla, no es posible usar píxeles gruesos para escribir en más de 16 muestras a la vez mediante la característica de sombreado de velocidad variable expuesta a través de Direct3D 12. Esta restricción se debe a las restricciones de Direct3D 12 con respecto a qué niveles de MSAA se permiten con qué tamaño de píxel general (consulte la tabla de la sección Con sombreado de velocidad [variable (VRS)](#with-variable-rate-shading-vrs) de este tema).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Ordenación y formato de bits en la máscara de cobertura
Los bits de la máscara de cobertura se adhieren a un orden bien definido. La máscara consta de coberturas de píxeles de izquierda a derecha y, a continuación, de arriba abajo (columna principal). Los bits de cobertura son los bits de orden bajo de la semántica de cobertura y se empaquetan de forma densa.

En la tabla siguiente se muestra el formato de máscara de cobertura para las combinaciones admitidas de tamaño de píxel general y nivel de MSAA.

![En la tabla se muestra el tamaño de píxel general, el diagrama de píxeles general y los bits de cobertura A de 1 x M S A.](images/Coverage1x.PNG "Cobertura a 1x")

En la tabla siguiente se representan 2 píxeles MSAA, donde cada píxel tiene dos muestras de índices 0 y 1.

El posicionamiento de las etiquetas de las muestras en los píxeles tiene fines ilustrativos y no necesariamente transmiten las ubicaciones espaciales {X, Y} de las muestras en ese píxel; especialmente dado que las posiciones de ejemplo se pueden cambiar mediante programación. El índice basado en 0 hace referencia a los ejemplos.

![En la tabla se muestra el tamaño de píxel general, el diagrama de píxeles general y los bits de cobertura A de 2 x M S A.](images/Coverage2x.PNG "Cobertura a 2x")

En la tabla siguiente se muestran 4 píxeles MSAA, donde cada píxel tiene cuatro muestras de índices 0, 1, 2 y 3.

![En la tabla se muestra el tamaño de píxel general, el diagrama de píxeles general y los bits de cobertura A de 4 M S A.](images/Coverage4x.PNG "Cobertura a 4x")

## <a name="discard"></a>Discard (Descartar)
Cuando se usa la semántica HLSL con sombreado de `discard` píxeles gruesos, se descartan los píxeles más anchos.

## <a name="target-independent-rasterization-tir"></a>Rasterización independiente del destino (TIR)
TIR no se admite cuando se usa el sombreado de píxeles general.

## <a name="raster-order-views-rovs"></a>Vistas de orden de trama (ROV)
Los interbloqueos ROV se especifican como que funcionan con granularidad de píxeles fina. Si el sombreado se realiza por ejemplo, los interbloqueos funcionan con granularidad de la muestra.

## <a name="conservative-rasterization"></a>Rasterización conservadora
Puede usar la rasterización conservadora con sombreado de velocidad variable. Cuando se usa la rasterización conservadora con sombreado de píxeles general, los píxeles finos dentro de los píxeles más anchos se rasterizan de forma conservadora al tener cobertura completa.

### <a name="coverage"></a>Cobertura
Cuando se usa la rasterización conservadora, la semántica de cobertura contiene máscaras completa para píxeles finos cubiertos y 0 para píxeles finos que no están cubiertos.

## <a name="bundles"></a>Agrupaciones
Puede llamar a las API de sombreado de velocidad variable en una agrupación.

## <a name="render-passes"></a>Fases de representación
Puede llamar a las API de sombreado de velocidad variable en un [paso de representación.](/windows/desktop/direct3d12/direct3d-12-render-passes)

## <a name="calling-the-vrs-apis"></a>Llamada a las API de VRS
En esta sección siguiente se describe la manera en que el sombreado de velocidad variable es accesible para la aplicación a través de Direct3D 12.

### <a name="capability-querying"></a>Consultas de funcionalidad

Para consultar la funcionalidad de sombreado de velocidad variable del adaptador, llame a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)y proporcione una estructura [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) para que la función se rellene por usted. La **estructura D3D12_FEATURE_DATA_D3D12_OPTIONS6** contiene varios miembros, incluido uno del tipo enumerado [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6::VariableShadingRateTier) y otro que indica si se admite el procesamiento en segundo plano (D3D12_FEATURE_DATA_D3D12_OPTIONS6::BackgroundProcessingSupported).

Para consultar la funcionalidad de nivel 1, por ejemplo, puede hacerlo.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Velocidades de sombreado

Los valores de la [ **enumeración D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) se organizan para que las tasas de sombreado se puedan descomponer fácilmente en dos ejes, donde los valores de cada eje se representan de forma compacta en el espacio logarítmico según la enumeración [ **D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

Puede crear una macro para crear velocidades de sombreado de dos ejes en una velocidad de sombreado como esta.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

La plataforma también proporciona estas macros, definidas en `d3d12.h` .

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Se pueden usar para diseccionar y comprender `SV_ShaderRate` .

> [!NOTE]
> Esta interpretación de datos está orientada a describir la imagen de espacio en pantalla, que pueden manipular los sombreadores. Esto se describe más adelante en las secciones anteriores. Pero no hay ninguna razón para no tener una definición coherente de los tamaños de píxeles gruesos que se usarán en todas partes, incluso al establecer la velocidad de sombreado de nivel de comando.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Establecimiento de la velocidad de sombreado y los combinadores de nivel de comando
La velocidad de sombreado y, opcionalmente, los combinadores se especifican mediante el método [**ID3D12GraphicsCommandList5::RSSetShadingRate.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) Se pasa un [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) para la velocidad de sombreado base y una matriz opcional de [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) valores.

### <a name="preparing-the-screen-space-image"></a>Preparación de la imagen de espacio en pantalla
El estado de recurso de solo lectura que designa una imagen de velocidad de sombreado utilizable se define [como D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Configuración de la imagen de espacio de pantalla
Especifique la imagen de espacio en pantalla mediante el método [**ID3D12GraphicsCommandList5::RSSetShadingRateImage.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage)

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Consulta del tamaño del icono
Puede consultar el tamaño del icono desde el [**D3D12_FEATURE_DATA_D3D12_OPTIONS6::ShadingRateImageTileSize.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) Consulte [Las consultas de funcionalidad anteriores.](#capability-querying)

Se recupera una dimensión, ya que las dimensiones horizontal y vertical son siempre las mismas. Si la funcionalidad del sistema es D3D12_SHADING_RATE_TIER_NOT_SUPPORTED [**,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)el tamaño del icono devuelto es 0.
