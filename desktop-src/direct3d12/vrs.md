---
title: Sombreado de velocidad variable (VRS)
description: El sombreado de velocidad variable &mdash; o el sombreado de píxeles gruesos &mdash; es un mecanismo que permite asignar potencia y rendimiento de la representación que varían en la imagen representada.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: be2367ceb72d2e693d86b6f279b627f3bffa9e1c
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104549191"
---
# <a name="variable-rate-shading-vrs"></a>Sombreado de velocidad variable (VRS)

## <a name="the-motivation-for-vrs"></a>La motivación de VRS
Debido a las restricciones de rendimiento, un representador de gráficos no siempre puede permitirse ofrecer el mismo nivel de calidad a cada parte de la imagen de salida. El sombreado de velocidad variable &mdash; o el sombreado de píxeles gruesos &mdash; es un mecanismo que permite asignar potencia y rendimiento de la representación que varían en la imagen representada.

En algunos casos, la tasa de sombreado se puede reducir con poca o ninguna reducción en la calidad de salida perceptible; Esto conduce a una mejora del rendimiento esencialmente gratuita.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Sin &mdash; suavizado de contorno de muestreo múltiple con VRS
Sin el sombreado de velocidad variable, el único medio para controlar la tasa de sombreado es con el suavizado de contorno de muestras múltiples (MSAA) con ejecución basada en muestras (también conocida como supermuestreo).

MSAA es un mecanismo para reducir el alias geométrico y mejorar la calidad de representación de una imagen en comparación con no usar MSAA. El recuento de muestras de MSAA, que puede ser 1x, 2x, 4x, 8X o 16X, rige el número de muestras asignadas por píxel de destino de representación. El recuento de muestras de MSAA se debe conocer por adelantado cuando se asigna el destino y no se puede cambiar después.

El supermuestreo hace que el sombreador de píxeles se invoque una vez por ejemplo, con una calidad más alta, pero también mayor costo de rendimiento en comparación con la ejecución por píxel.

La aplicación puede controlar su tasa de sombreado eligiendo entre la ejecución basada en píxeles o MSAA-with-supermuestreing. Estas dos opciones no proporcionan un control muy fino. Además, es posible que desee una tasa de sombreado inferior para una clase determinada de objetos en comparación con el resto de la imagen. Estos objetos pueden incluir un objeto detrás de un elemento HUD, una transparencia, un desenfoque (profundidad de campo, movimiento, etc.) o una distorsión óptica debido a la fibra óptica de VR. Pero esto no sería posible porque la calidad y los costos de sombreado se fijan en toda la imagen.

## <a name="with-variable-rate-shading-vrs"></a>Con sombreado de velocidad variable (VRS)
El modelo de sombreado de velocidad variable (VRS) amplía el supermuestreo con la dirección de MSAA en el opuesto, "píxel grueso", agregando el concepto de sombreado grueso. Aquí es donde el sombreado se puede realizar a una frecuencia más ancha que un píxel. Es decir, un grupo de píxeles se puede sombrear como una sola unidad y, a continuación, el resultado se difunde a todos los ejemplos del grupo.

Una API de sombreado grueso permite a la aplicación especificar el número de píxeles que pertenecen a un grupo sombreado o a un *píxel grueso*. Puede cambiar el tamaño de los píxeles gruesos después de haber asignado el destino de representación. Por lo tanto, distintas partes de la pantalla o de diferentes pasadas de dibujo pueden tener diferentes tasas de sombreado.

Esta es una tabla que describe qué nivel de MSAA es compatible con el tamaño de píxel grueso. Algunos no se admiten en ninguna plataforma; mientras que otros se habilitan condicionalmente en función de una capacidad (*AdditionalShadingRatesSupported*), indicada por "Cap".

![coarsePixelSizeSupport](images/CoarsePixelSizeSupport.PNG "Tamaños de píxeles gruesos")

En el caso de los niveles de características que se describen en la sección siguiente, no hay una combinación de tamaño de píxeles grueso y de número de muestras, donde el hardware necesita realizar un seguimiento de más de 16 muestras por invocación del sombreador de píxeles. Estas combinaciones están sombreadas en semitono en la tabla anterior.

## <a name="feature-tiers"></a>Niveles de características
Hay dos niveles para la implementación de VRS y dos funcionalidades que puede consultar. Cada nivel se describe con mayor detalle después de la tabla.

![niveles](images/Tiers.PNG "Niveles de VRS")

### <a name="tier-1"></a>Nivel 1
- La tasa de sombreado solo se puede especificar para cada dibujo; no es más granular que eso.
- La tasa de sombreado se aplica uniformemente a lo que se dibuja independientemente del lugar en el que se encuentra dentro del destino de representación.

### <a name="tier-2"></a>Nivel 2
- La tasa de sombreado se puede especificar en función de cada dibujo, como en el nivel 1. También se puede especificar mediante una combinación de por dibujo y de:
  - Semántica de cada vértice de la provocación, y
  - imagen de espacio de pantalla.
- Las tasas de sombreado de los tres orígenes se combinan mediante un conjunto de combinadores.
- El tamaño del mosaico de imagen de espacio de pantalla es 16x16 o inferior.
- La tasa de sombreado solicitada por la aplicación se garantiza que se entregue exactamente (para la precisión de los filtros temporales y otros filtros de reconstrucción).
- SV_ShadingRate se admite la entrada de PS.
- La tasa de sombreado por provocó el vértice (también conocido como por primitivo) es válida cuando se usa una ventanilla y `SV_ViewportArrayIndex` no se escribe en ella.
- La velocidad de los vértices por provocó se puede usar con más de una ventanilla si la funcionalidad *SupportsPerVertexShadingRateWithMultipleViewports* está establecida en `true` . Además, en ese caso, se puede usar esa velocidad cuando `SV_ViewportArrayIndex` se escribe en.

### <a name="list-of-capabilities"></a>Lista de capacidades
- *AdditionalShadingRatesSupported*
  - Tipo booleano.
  - Indica si se admiten los tamaños de píxeles generales 2x4, 4 TB y 4x4 para la representación de muestreo único; y si el tamaño de píxel grueso 2x4 es compatible con el doble MSAA.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Tipo booleano.
  - Indica si se puede usar más de una ventanilla con el tipo de sombreado por vértice (también conocido como por primitivo).

## <a name="specifying-shading-rate"></a>Especificar la tasa de sombreado
Para ofrecer flexibilidad en las aplicaciones, hay una variedad de mecanismos que se proporcionan para controlar la tasa de sombreado. Hay diferentes mecanismos disponibles según el nivel de características de hardware.

### <a name="command-list"></a>Lista de comandos
Este es el mecanismo más sencillo para establecer la tasa de sombreado. Está disponible en todos los niveles.

La aplicación puede especificar un tamaño de píxel grueso mediante el [método **ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Esa API toma un solo argumento de enumeración. La API proporciona un control general del nivel de calidad para representar &mdash; la capacidad de establecer la tasa de sombreado por dibujo.

Los valores de este estado se expresan a través de la enumeración [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

#### <a name="coarse-pixel-size-support"></a>Compatibilidad con el tamaño de píxeles grueso
Las tasas de sombreado 1x1, 1x2, 2x2 y 2x2 se admiten en todos los niveles.

Hay una funcionalidad, *AdditionalShadingRatesSupported*, para indicar si se admiten 2x4, 4 TB y 4x4 en el dispositivo.

### <a name="screen-space-image-image-based"></a>Imagen de espacio de pantalla (basada en imagen)
En el nivel 2 y superior, puede especificar la velocidad de sombreado de píxeles con una imagen de espacio en pantalla.

La imagen de espacio de pantalla permite a la aplicación crear una imagen de "máscara de nivel de detalle (LOD)" que indica regiones de calidad variable, como áreas que se tratarán con el desenfoque de movimiento, el desenfoque de profundidad de campo, los objetos transparentes o los elementos de la interfaz de usuario de HUD. La resolución de la imagen está en macrobloques; no se encuentra en la resolución del destino de representación. En otras palabras, los datos de la tasa de sombreado se especifican con una granularidad de mosaicos de 8 a 16 o 16 x 16 píxeles, tal y como se indica en el tamaño del mosaico VRS.

#### <a name="tile-size"></a>Tamaño de mosaico
La aplicación puede consultar una API para recuperar el tamaño de mosaico de VRS admitido para su dispositivo.

Los mosaicos son cuadrados y el tamaño hace referencia al ancho o al alto del icono en textura.

Si el hardware no admite el sombreado de velocidad variable de nivel 2, la consulta de capacidad para el tamaño de mosaico devuelve 0.

Si *el hardware admite* el sombreado de velocidad variable de nivel 2, el tamaño del mosaico es uno de estos valores.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Tamaño de imagen de espacio de pantalla
Para un destino de representación de size {rtWidth, rtHeight}, con un tamaño de mosaico determinado denominado **VRSTileSize**, la imagen de espacio de pantalla que cubrirá es de estas dimensiones.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

La parte superior izquierda de la imagen de espacio de pantalla (0,0) está bloqueada en la parte superior izquierda del destino de representación (0,0).

Para buscar la coordenada (x, y) de un icono que se corresponda con una ubicación determinada en el destino de representación, divida las coordenadas del espacio de la ventana de (x, y) por el tamaño del mosaico, omitiendo los bits fraccionarios.

Si la imagen de espacio de pantalla es mayor de lo que necesita para un destino de representación determinado, no se usan las partes adicionales de la derecha o inferior.

Si la imagen de espacio de pantalla es demasiado pequeña para un destino de representación determinado, cualquier intento de lectura de la imagen más allá de sus extensiones reales produce una tasa de sombreado predeterminada de 1x1. Esto se debe a que la parte superior izquierda de la imagen del espacio de pantalla (0,0) está bloqueada en la parte superior izquierda del destino de representación (0,0) y la lectura más allá de las extensiones del destino de representación significa que se está leyendo una gran cantidad de valores para x e y.

#### <a name="format-layout-resource-properties"></a>Formato, diseño, propiedades de recursos
El formato de esta superficie es una superficie de 8 bits de canal único ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

El recurso es Dimension **TEXTURE2D**.

No puede ser arrayd ni mipped. Debe tener explícitamente un nivel de MIP.

Tiene el recuento de muestras 1 y la calidad de ejemplo 0.

Tiene un diseño de textura **desconocido**. No puede ser un diseño de fila principal, ya que no se permite el adaptador cruzado.

La manera esperada en la que se rellenan los datos de imagen de espacio de pantalla es
1. Escribir los datos mediante un sombreador de cálculo; la imagen del espacio de pantalla se enlaza como UAV, o bien
2. Copie los datos en la imagen de espacio de pantalla.

Al crear la imagen de espacio de pantalla, se permiten estas marcas.

- NONE
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

No se permiten estas marcas.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

El tipo de montón del recurso no se puede cargar ni READBACK.

No se puede SIMULTANEOUS_ACCESS el recurso. No se permite el recurso entre adaptadores.

#### <a name="data"></a>data
Cada byte de la imagen de espacio de pantalla corresponde a un valor de la enumeración [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  .

#### <a name="resource-state"></a>Estado del recurso
Un recurso se debe pasar a un estado de solo lectura cuando se usa como imagen de espacio de pantalla. Se define un estado de solo lectura, [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states), para este propósito.

El recurso de imagen se pasa de ese estado para volver a escribir.

#### <a name="setting-the-image"></a>Establecimiento de la imagen
La imagen de espacio de pantalla para especificar la tasa de sombreador se establece en la lista de comandos.

Un recurso que se ha establecido como un origen de la tasa de sombreado no se puede leer ni escribir en ninguna fase del sombreador.

`null`Se puede establecer una imagen de espacio de pantalla para especificar la velocidad del sombreador. Esto tiene el efecto de que 1x1 se use de forma coherente como contribución de la imagen de espacio de pantalla. La imagen del espacio de pantalla se puede considerar inicialmente como establecida en `null` .

#### <a name="promotion-and-decay"></a>Promoción y caída
Un recurso de imagen de espacio de pantalla no tiene ninguna implicación especial con respecto a la promoción o la caída.

### <a name="per-primitive-attribute"></a>Atributo por primitivo
Un atributo por primitivo agrega la capacidad de especificar un término de tasa de sombreado como un atributo de un vértice de provocó. Este atributo tiene una sombra plana &mdash; , es decir, se propaga a todos los píxeles del triángulo o la línea primitivos actuales. El uso de un atributo por primitivo puede permitir un control más preciso de la calidad de la imagen en comparación con los demás especificadores de velocidad de sombreado.

El atributo por primitivo es una semántica configurable denominada `SV_ShadingRate` . `SV_ShadingRate` existe como parte del [modelo de sombreador de HLSL 6,4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12).

Si se establece VS o GS `SV_ShadingRate` , pero VRS no está habilitado, la configuración semántica no tiene ningún efecto. Si no se especifica ningún valor para `SV_ShadingRate` por primitivo, se supone que el valor de la tasa de sombreado es 1x1 como contribución por primitiva.

### <a name="combining-shading-rate-factors"></a>Combinación de factores de velocidad de sombreado
Los distintos orígenes de la tasa de sombreado se aplican en secuencia mediante este diagrama.

![combinadores](images/Combiners.PNG "Separadores de sombreado")

Cada par de A y B se combina mediante un combinador.

\* Al especificar una tasa de sombreador por atributo de vértice.

- Si se usa un sombreador de geometría, se puede especificar la tasa de sombreado a través de ese.
- Si no se usa un sombreador de geometría, el vértice de la llamada especifica la tasa de sombreado.

#### <a name="list-of-combiners"></a>Lista de los combinadores
Se admiten los siguientes combinados. Usar un combinador (C) y dos entradas (A y B).

- **Paso a través**. C. XY = A. XY.
- **Reemplazar**. C. XY = B. XY.
- **Mayor calidad**. C. XY = mín (A. XY, B. XY).
- **Calidad inferior**. C. XY = Max (A. XY, B. XY).
- **Aplique el costo B en relación con un**. C. XY = min (maxRate, A. XY + B. XY).

donde `maxRate` es la dimensión más grande permitida del píxel grueso en el dispositivo. Esto sería

- **D3D12_AXIS_SHADING_RATE_2X** (es decir, un valor de 1), si AdditionalShadingRatesSupported es `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (es decir, un valor de 2), si AdditionalShadingRatesSupported es `true` .

La elección del combinador para el sombreado de velocidad variable se establece en la lista de comandos a través de [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Si no se establece ningún combinado, se mantienen en el valor predeterminado, que es PASSTHROUGH.

Si el origen de un combinador es un [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate), lo que no se permite en la tabla de soporte técnico, la entrada se limpia a una tasa de sombreado que *se* admite.

Si la salida de un combinador no se corresponde con una tasa de sombreado admitida en la plataforma, el resultado se limpia a una tasa de sombreado que *se* admite.

### <a name="default-state-and-state-clearing"></a>Estado predeterminado y borrado de estado
Todas las fuentes de la tasa de sombreado, es decir,

- la tasa especificada por el estado de la canalización (especificada en la lista de comandos).
- la velocidad especificada por la imagen de espacio de pantalla y
- el atributo por primitivo

tener un valor predeterminado de **D3D12_SHADING_RATE_1X1**. Los combinadores predeterminados son {PASSTHROUGH, PASSTHROUGH}.

Si no se especifica ninguna imagen de espacio de pantalla, se deduce una tasa de sombreado de 1x1 de ese origen.

Si no se especifica ningún atributo por primitivo, se deduce una tasa de sombreado de 1x1 a partir de ese origen.

[ID3D12CommandList:: ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) restablece la tasa especificada en el estado de canalización en el valor predeterminado y la selección de la imagen de espacio de pantalla en el valor predeterminado de "sin imagen de espacio de pantalla".

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Consulta de la tasa de sombreado mediante SV_ShadingRate
Resulta útil saber qué tipo de sombreado ha seleccionado el hardware en cualquier invocación del sombreador de píxeles dada. Esto podría habilitar diversas optimizaciones en el código PS. Una variable del sistema solo PS, `SV_ShadingRate` , proporciona información sobre la tasa de sombreado.

### <a name="type"></a>Tipo
El tipo de esta semántica es uint.

### <a name="data-interpretation"></a>Interpretación de datos
Los datos se interpretan como un valor de la enumeración [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

### <a name="if-vrs-is-not-being-used"></a>Si no se utiliza VRS
Si no se utiliza el sombreado de píxeles gruesos, `SV_ShadingRate` se vuelve a leer como un valor de 1x1, lo que indica unos píxeles.

### <a name="behavior-under-sample-based-execution"></a>Comportamiento en la ejecución basada en muestras
Un sombreador de píxeles produce un error en la compilación si `SV_ShadingRate` especifica y también usa la ejecución basada en &mdash; el ejemplo, por ejemplo, al insertar `SV_SampleIndex` o utilizar la palabra clave de interpolación de ejemplo.

> ### <a name="remarks-on-deferred-shading"></a>Comentarios sobre el sombreado diferido
>
> Es posible que los pasos de iluminación de una aplicación de sombreado diferida tengan que saber qué tipo de sombreado se ha usado para el área de la pantalla. Esto es para que los envíos de paso de iluminación se puedan iniciar a una tarifa más amplia. La `SV_ShadingRate` variable se puede usar para lograr esto si se escribe en el gbuffer.

## <a name="depth-and-stencil"></a>Profundidad y estarcido
Cuando se usa el sombreado de píxeles grueso, la profundidad y el estarcido y la cobertura siempre se calculan y se emiten en la resolución de ejemplo completa.

## <a name="using-the-shading-rate-requested"></a>Uso de la tasa de sombreado solicitada
En el caso de todos los niveles, se espera que si se solicita una tasa de sombreado y se admita en la combinación de nivel de dispositivo y MSAA, es decir, el tipo de sombreado que entrega el hardware.

Una tasa de sombreado solicitada significa una tasa de sombreado calculada como una salida de los combinadores (consulte la sección [combinación de factores de sombreado](#combining-shading-rate-factors) de este tema).

Una tasa de sombreado compatible es 1x1, 1x2, 2x1 o 2x2 en una operación de representación en la que el recuento de muestras es menor o igual que cuatro. Si la capacidad de *AdditionalShadingRatesSupported* es `true` , a continuación, 2x4, 4 TB y 4x4 también son compatibles con las tasas de sombreado para algunos recuentos de muestras (vea la tabla en la sección [con el sombreado de velocidad variable (VRS)](#with-variable-rate-shading-vrs) de este tema).

## <a name="screen-space-derivatives"></a>Derivados de espacio de pantalla
Los cálculos de degradados de píxel a adyacentes se ven afectados por el sombreado de píxeles gruesos. Por ejemplo, cuando se usan píxeles gruesos de 2x2, un degradado será el doble del tamaño en comparación con cuando no se usen píxeles gruesos. Es posible que la aplicación desee ajustar los sombreadores para compensar esto &mdash; o no, en función de la funcionalidad que desee.

Dado que MIPS se elige en función de un derivado de espacio de pantalla, el uso de sombreado de píxeles gruesos afecta a la selección de MIP. El uso de sombreado de píxeles gruesos hace que se seleccione MIPS menos detallado en comparación con cuando no se usan píxeles gruesos.

## <a name="attribute-interpolation"></a>Interpolación de atributos
Las entradas de un sombreador de píxeles se pueden interpolar en función de sus vértices de origen. Dado que el sombreado de velocidad variable afecta a las áreas del destino escritas por cada invocación del sombreador de píxeles, interactúa con la interpolación de atributos. Los tres tipos de interpolación son Center, centroide y sample.

### <a name="center"></a>Center
La ubicación de interpolación central de un píxel grueso es el centro geométrico del área de píxeles gruesos completos. `SV_Position` siempre se interpola en el centro de la región de píxeles grueso.

### <a name="centroid"></a>Centroide
Cuando se usa el sombreado de píxeles grueso con MSAA, para cada píxel fino todavía se escribirá en el número completo de muestras asignadas para el nivel de MSAA del destino. Por lo tanto, la ubicación de interpolación centroide considerará todos los ejemplos de píxeles finos en píxeles gruesos. Dicho esto, la ubicación de interpolación centroide se define como el primer ejemplo descrito, en orden creciente de índice de ejemplo. La cobertura efectiva del ejemplo es y-Ed con el bit correspondiente del estado de rasterizador SampleMask.

> [!NOTE]
> Cuando se usa el sombreado de píxeles grueso en el nivel 1, SampleMask siempre es una máscara completa. Si SampleMask está configurado para que no sea una máscara completa, el sombreado de píxeles grueso se deshabilita en el nivel 1.

### <a name="sample-based-execution"></a>Ejecución basada en el ejemplo
La ejecución basada en muestras o el *supermuestreado* &mdash; que se debe al uso de la característica de interpolación de ejemplo &mdash; se pueden utilizar con el sombreado de píxeles gruesos y hace que el sombreador de píxeles se invoque por muestra. En el caso de los destinos del recuento de muestras N, el sombreador de píxeles se invoca N veces por píxel fino.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Los intrínsecos del modelo de extracción no son compatibles con el sombreado de píxeles gruesos en el nivel 1. Si se intenta usar funciones intrínsecas de modelo de extracción con sombreado de píxeles grueso en el nivel 1, el sombreado de píxeles gruesos se deshabilita automáticamente.

El intrínseco puede `EvaluateAttributeSnapped` usarse con el sombreado de píxeles gruesos en el nivel 2. Su sintaxis es la misma que siempre ha sido.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

En el contexto, `EvaluateAttributeSnapped` tiene un parámetro de desplazamiento con dos campos. Cuando se usa sin sombreado de píxeles grueso, solo se usan los cuatro bits de orden inferior de los 32 completos. Estos cuatro bits representan el intervalo [-8, 7]. Este intervalo abarca una cuadrícula de 16x16 dentro de un píxel. El intervalo es tal que se incluyen los bordes superior e izquierdo del píxel, y los bordes inferior y derecho no lo están. PosiciónInicial (-8,-8) está en la esquina superior izquierda y el desplazamiento (7,5) está en la esquina inferior derecha. PosiciónInicial (0,0) es el centro del píxel.

Cuando se usa con el sombreado de píxeles gruesos, `EvaluateAttributeSnapped` el parámetro offset es capaz de especificar un intervalo más amplio de ubicaciones. El parámetro offset selecciona una cuadrícula 16x16 para cada píxel fino y hay varios píxeles finos. El intervalo que se permite expresar y el número de bits resultante depende del tamaño de píxel grueso. Se incluyen los bordes superior e izquierdo del píxel grueso y los bordes inferior y derecho no lo están.

En la tabla siguiente se describe la interpretación del `EvaluateAttributeSnapped` parámetro offset de cada tamaño de píxel grueso.

#### <a name="evaluateattributesnappeds-offset-range"></a>Intervalo de desplazamiento de EvaluateAttributeSnapped

|Tamaño de píxel grueso  |Intervalo indexable             |Tamaño de intervalo representable  |Número de bits necesarios {x, y}  |Máscara binaria de bits utilizable          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fino)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{000000000000xxxx, 000000000000xxxx}|    
|1 instancia                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{00000000000xxxxx, 000000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|2x4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4 TB                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4 x 4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

Las tablas siguientes son una guía para la conversión desde el punto fijo hasta el decimal y la representación fraccionaria. El primer bit utilizable de la máscara binaria es el bit de signo y el resto de la máscara binaria consta de la parte numérica.

El esquema de números para los valores de cuatro bits pasados a `EvaluateAttributeSnapped` no es específico del sombreado de velocidad variable. Se repite aquí para que haya integridad.

Para valores de cuatro bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|         1000 |-0.5 f     |-8/16     |
|         1001 |-0.4375 f  |-7/16|    |
|         1010 |-0.375 f   |-6/16|    |
|         1011 |-0.3125 f  |-5/16     |
|         1100 |-0,25 f    |-4/16     |
|         1101 |-0.1875 f  |-3/16     |
|         1110 |-0,125 f   |-2/16     |
|         1111 |-0.0625 f  |-1/16      |
|         0000 |0,0F      |0 / 16      |
|         0,001 |-0.0625 f  |1 / 16      |
|         milésima |-0,125 f   |2 / 16      |
|         0011 |-0.1875 f  |3 / 16      |
|         0100 |-0,25 f    |4 / 16      |
|         0101 |-0.3125 f  |5 / 16      |
|         0110 |-0.375 f   |6 / 16      |
|         0111 |-0.4375 f  |7 / 16      |

Para valores de cinco bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16/16    |
|        10001 |-0,9375   |-15/16    |
|        10010 |-0,875    |-14/16    |
|        10011 |-0,8125   |-13/16    |
|        10100 |-0.75     |-12/16    |
|        10101 |-0,6875   |-11/16    |
|        10110 |-0,625    |-10/16    |
|        10111 |-0,5625   |-9/16     |
|        11000 |-0,5      |-8/16     |
|        11001 |-0,4375   |-7/16     |
|        11010 |-0,375    |-6/16     |
|        11011 |-0,3125   |-5/16     |
|        11100 |-0.25     |-4/16     |
|        11101 |-0,1875   |-3/16     |
|        11110 |-0,125    |-2/16     |
|        11111 |-0,0625   |-1/16     |
|        00000 |0         |0 / 16      |
|        00001 |0,0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0,1875    |3 / 16      |
|        00100 |0,25 %      |4 / 16      |
|        00101 |0,3125    |5 / 16      |
|        00110 |0,375     |6 / 16      |
|        00111 |0,4375    |7 / 16      |
|        01000 |0.5       |8 / 16      |
|        01001 |0,5625    |9 / 16      |
|        01010 |0,625     |10 / 16     |
|        01011 |0,6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0,8125    |13 / 16     |
|        01110 |0,875     |14 / 16     |
|        01111 |0,9375    |15 / 16     |

Para valores de seis bits.

| Valor binario | Decimal  | Fracciones |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32/16    |
|       100001 |-1,9375   |-31/16    |
|       100010 |-1,875    |-30/16    |
|       100011 |-1,8125   |-29/16    |
|       100100 |-1,75     |-28/16    |
|       100101 |-1,6875   |-27/16    |
|       100110 |-1,625    |-26/16    |
|       100111 |-1,5625   |-25/16    |
|       101000 |-1,5      |-24/16    |
|       101001 |-1,4375   |-23/16    |
|       101010 |-1,375    |-22/16    |
|       101011 |-1,3125   |-21/16    |
|       101100 |-1.25     |-20/16    |
|       101101 |-1,1875   |-19/16    |
|       101110 |-1,125    |-18/16    |
|       101111 |-1,0625   |-17/16    |
|       110000 |-1        |-16/16    |
|       110001 |-0,9375   |-15/16    |
|       110010 |-0,875    |-14/16    |
|       110011 |-0,8125   |-13/16    |
|       110100 |-0.75     |-12/16    |
|       110101 |-0,6875   |-11/16    |
|       110110 |-0,625    |-10/16    |
|       110111 |-0,5625   |-9/16     |
|       111000 |-0,5      |-8/16     |
|       111001 |-0,4375   |-7/16     |
|       111010 |-0,375    |-6/16     |
|       111011 |-0,3125   |-5/16     |
|       111100 |-0.25     |-4/16     |
|       111101 |-0,1875   |-3/16     |
|       111110 |-0,125    |-2/16     |
|       111111 |-0,0625   |-1/16     |
|       000000 |0         |0 / 16      |
|       000001 |0,0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0,1875    |3 / 16      |
|       000100 |0,25 %      |4 / 16      |
|       000101 |0,3125    |5 / 16      |
|       000110 |0,375     |6 / 16      |
|       000111 |0,4375    |7 / 16      |
|       001000 |0.5       |8 / 16      |
|       001001 |0,5625    |9 / 16      |
|       001010 |0,625     |10 / 16     |
|       001011 |0,6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0,8125    |13 / 16     |
|       001110 |0,875     |14 / 16     |
|       001111 |0,9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1,0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1,1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1,3125    |21 / 16     |
|       010110 |1,375     |22 / 16     |
|       010111 |1,4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1,5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1,6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1,8125    |29 / 16     |
|       011110 |1,875     |30 / 16     |
|       011111 |1,9375    |31 / 16     |

Del mismo modo que con los píxeles finos, la `EvaluateAttributeSnapped` cuadrícula de ubicaciones evaluables se centra en el centro de píxeles grueso cuando se usa el sombreado de píxeles gruesos.

## <a name="setsamplepositions"></a>SetSamplePositions
Cuando se usa la API [**ID3D12GraphicsCommandList1:: SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) con sombreado grueso, la API establece las posiciones de ejemplo para los píxeles finos.

## <a name="sv_coverage"></a>SV_Coverage
Si `SV_Coverage` se declara como entrada o salida del sombreador en el nivel 1, el sombreado de píxeles gruesos estará deshabilitado.

Puede usar la `SV_Coverage` semántica con el sombreado de píxeles gruesos en el nivel 2 y refleja qué muestras de un destino de MSAA se están escribiendo.

Cuando se usa el sombreado de píxeles grueso, lo que permite que varios píxeles de origen contengan &mdash; un icono, &mdash; la máscara de cobertura representa todos los ejemplos que proceden de ese mosaico.

Dada la compatibilidad de sombreado de píxeles generales con MSAA, el número de bits de cobertura que se deben especificar puede variar. Por ejemplo, con un recurso de MSAA a 4x mediante [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate), cada píxel grueso escribe en cuatro finos píxeles y cada píxel fino tiene cuatro ejemplos. Esto significa que cada píxel grueso escribe en un total de 4 * 4 = 16 muestras.

### <a name="number-of-coverage-bits-needed"></a>Número de bits de cobertura necesarios
En la tabla siguiente se indica el número de bits de cobertura necesarios para cada combinación de tamaño de píxel grueso y nivel de MSAA.

![NumberOfCoverageBits](images/NumberOfCoverageBits.PNG "Bits de cobertura")

Como se indica en la tabla, no es posible usar los píxeles gruesos para escribir más de 16 muestras a la vez mediante la característica de sombreado de velocidad variable expuesta a través de Direct3D 12. Esta restricción se debe a las restricciones de Direct3D 12 con respecto a los niveles de MSAA permitidos con el tamaño de píxel grueso (consulte la tabla de la sección [con el sombreado de velocidad variable (VRS)](#with-variable-rate-shading-vrs) de este tema).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Ordenación y formato de bits en la máscara de cobertura
Los bits de la máscara de cobertura se adhieren a un orden bien definido. La máscara se compone de coberturas de píxeles de izquierda a derecha y, a continuación, el orden de arriba a abajo (columna principal). Los bits de cobertura son los bits de orden inferior de la semántica de cobertura y se empaquetan de forma densa.

En la tabla siguiente se muestra el formato de la máscara de cobertura para las combinaciones admitidas de tamaño de píxeles grueso y nivel de MSAA.

![Coverage1x](images/Coverage1x.PNG "Cobertura en 1x")

En la tabla siguiente se describen 2x píxeles de MSAA, donde cada píxel tiene dos muestras de índices 0 y 1.

La posición de las etiquetas de las muestras en los píxeles es para fines ilustrativos y no transmite necesariamente las ubicaciones espaciales {X, Y} de los ejemplos en ese píxel; especialmente dado que las posiciones de ejemplo se pueden cambiar mediante programación. A los ejemplos se hace referencia mediante su índice de base 0.

![Coverage2x](images/Coverage2x.PNG "Cobertura a 2x")

En la tabla siguiente se muestran 4x píxeles de MSAA, donde cada píxel tiene cuatro muestras de índices 0, 1, 2 y 3.

![Coverage4x](images/Coverage4x.PNG "Cobertura a 4x")

## <a name="discard"></a>Discard (Descartar)
Cuando la semántica de HLSL `discard` se usa con sombreado de píxeles grueso, se descartan los píxeles gruesos.

## <a name="target-independent-rasterization-tir"></a>Rasterización independiente del destino (TIR)
TIR no se admite cuando se usa el sombreado de píxeles grueso.

## <a name="raster-order-views-rovs"></a>Vistas de orden de trama (ROVs)
Los interbloqueos de ROV se especifican como funcionando con granularidad de píxeles finos. Si el sombreado se realiza por ejemplo, los interbloqueos funcionan con la granularidad de ejemplo.

## <a name="conservative-rasterization"></a>Rasterización conservadora
Puede usar la rasterización conservadora con sombreado de velocidad variable. Cuando se utiliza la rasterización conservadora con el sombreado de píxeles gruesos, los píxeles finos dentro de los píxeles gruesos se rasterizan de manera conservadora al recibir una cobertura completa.

### <a name="coverage"></a>Cobertura
Cuando se usa la rasterización conservadora, la semántica de cobertura contiene máscaras completas para los píxeles finos cubiertos y 0 para los píxeles finos que no están cubiertos.

## <a name="bundles"></a>Agrupaciones
Puede llamar a las API de sombreado de velocidad variable en una agrupación.

## <a name="render-passes"></a>Fases de representación
Puede llamar a las API de sombreado de velocidad variable en una [fase de representación](/windows/desktop/direct3d12/direct3d-12-render-passes).

## <a name="calling-the-vrs-apis"></a>Llamada a las API de VRS
En la siguiente sección se describe la manera en que el sombreado de velocidad variable es accesible para la aplicación a través de Direct3D 12.

### <a name="capability-querying"></a>Consulta de funcionalidades

Para consultar la capacidad de sombreado de velocidad variable del adaptador, llame a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)y proporcione una [estructura de **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) para que la función se rellene automáticamente. La estructura de **D3D12_FEATURE_DATA_D3D12_OPTIONS6** contiene varios miembros, incluido uno que es del tipo enumerado [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: VariableShadingRateTier) y otro que indica si se admite el procesamiento en segundo plano (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: BackgroundProcessingSupported).

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

### <a name="shading-rates"></a>Tasas de sombreado

Los valores de la [enumeración **D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) se organizan de modo que las tasas de sombreado se decomposable fácilmente en dos ejes, donde los valores de cada eje se representan de forma compacta en el espacio logarítmico según la [enumeración **D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

Puede crear una macro para crear dos tasas de sombreado de eje en una velocidad de sombreado como esta.

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

Se pueden usar para analizar minuciosamente y entender `SV_ShaderRate` .

> [!NOTE]
> Esta interpretación de datos está orientada hacia la descripción de la imagen de espacio de pantalla, que se puede manipular mediante sombreadores. Esto se describe con más detalle en las secciones anteriores. Sin embargo, no hay ninguna razón para no tener una definición coherente de los tamaños de píxeles gruesos que se van a usar en todas partes, incluida la configuración de la tasa de sombreado de nivel de comando.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Establecer la tasa de sombreado y los combinadores de nivel de comando
La tasa de sombreado y, opcionalmente, los combinados se especifican a través del método [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) . Se pasa un valor [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) para la tasa de sombreado base y una matriz opcional de valores [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) .

### <a name="preparing-the-screen-space-image"></a>Preparar la imagen de espacio de pantalla
El estado de los recursos de solo lectura que designa una imagen de tasa de sombreado utilizable se define como [D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Establecer la imagen de espacio de pantalla
La imagen de espacio de pantalla se especifica mediante el método [**ID3D12GraphicsCommandList5:: RSSetShadingRateImage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) .

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Consultar el tamaño del mosaico
Puede consultar el tamaño del mosaico desde el miembro [**D3D12_FEATURE_DATA_D3D12_OPTIONS6:: ShadingRateImageTileSize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Consulte la [consulta de funcionalidades](#capability-querying) anterior.

Se recupera una dimensión, ya que las dimensiones horizontal y vertical siempre son las mismas. Si la capacidad del sistema es [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier), el tamaño de mosaico devuelto es 0.
