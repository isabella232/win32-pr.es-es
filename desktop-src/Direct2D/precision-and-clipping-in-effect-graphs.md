---
title: Precisión y recorte numérico en gráficos de efecto
description: Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y predictibilidad con respecto a la precisión numérica.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f2af6fdee4561caa60ea22a0c700593f2333727e6c5a63c5346fdc78bbdb40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160509"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Precisión y recorte numérico en gráficos de efecto

Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y predictibilidad con respecto a la precisión numérica. En este tema se describen los procedimientos recomendados y la configuración pertinente en Direct2D, que son útiles si:

-   El gráfico de efectos se basa en una alta precisión numérica o colores fuera del intervalo 0, 1, y quiere asegurarse de que siempre \[ \] estarán disponibles.
-   O bien, el gráfico de efectos se basa en la implementación de representación para fijar los colores intermedios al intervalo 0, 1 y desea asegurarse de que esta fijación \[ \] siempre se produce.

Direct2D a menudo divide un gráfico de efectos en secciones y representa cada sección en un paso independiente. La salida de algunos pasos se puede almacenar en texturas intermedias de Direct3D que, de forma predeterminada, tienen un intervalo numérico y una precisión limitados. Direct2D no garantiza si se usan estas texturas intermedias o dónde. Este comportamiento puede variar según las funcionalidades de GPU, así como entre Windows versiones.

En Windows 10, Direct2D usa menos texturas intermedias debido a su uso de vinculación de sombreador. Por lo tanto, Direct2D puede generar resultados diferentes con la configuración predeterminada que en versiones Windows anteriores. Esto afecta principalmente a escenarios en los que la vinculación del sombreador es posible en un gráfico de efectos y ese gráfico también contiene efectos que producen colores de salida de intervalo extendido.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Información general sobre la representación de efectos y los intermedios

Para representar un gráfico de efectos, Direct2D busca primero el gráfico subyacente de "transformaciones", donde una transformación es un nodo de grafo que se usa dentro de un efecto. Hay diferentes tipos de transformaciones, incluidas las que proporcionan sombreadores De Direct3D para que las use Direct2D.

Por ejemplo, Direct2D puede representar un gráfico de efectos de la siguiente manera:

![gráfico de efectos con texturas intermedias](images/precision-and-clipping-1.png)

Direct2D busca oportunidades para reducir el número de texturas intermedias que se usan para representar el gráfico de efectos. esta lógica es opaca para las aplicaciones. Por ejemplo, Direct2D puede representar el siguiente gráfico mediante una llamada a draw de Direct3D y sin texturas intermedias:

![gráfico de efectos sin texturas intermedias](images/precision-and-clipping-2.png)

Antes de Windows 10, Direct2D siempre usaba texturas intermedias si se usaban varios sombreadores de píxeles dentro del mismo gráfico de efectos. La mayoría de los efectos integrados que simplemente ajustan los valores de color (por ejemplo, Brillo o Saturación) lo hacen mediante sombreadores de píxeles.

En Windows 10, Direct2D ahora puede evitar el uso de texturas intermedias en tales casos. Para ello, vincula internamente sombreadores de píxeles adyacentes. Por ejemplo:

![Gráfico de efectos de Windows 10 con varios sombreadores de píxeles y sin texturas intermedias](images/precision-and-clipping-3.png)

Tenga en cuenta que no todos los sombreadores de píxeles adyacentes de un gráfico se pueden vincular juntos y, por tanto, solo determinados gráficos producirán una salida diferente en Windows 10. Para obtener detalles completos, [vea Effect Shader Linking](effect-shader-linking.md). Las restricciones principales son:

-   Un efecto no se vinculará con los efectos que consumen su salida, si el primer efecto está conectado como entrada a varios efectos.
-   Un efecto no se vinculará con un conjunto de efectos como entrada, si el primer efecto muestrea su entrada en una posición lógica diferente de su salida. Por ejemplo, un efecto de matriz de colores podría vincularse con su entrada, pero un efecto de convolución no lo será.

## <a name="built-in-effect-behavior"></a>Comportamiento del efecto integrado

Muchos efectos integrados pueden producir colores fuera del intervalo 0, 1 en el espacio de colores sin multiplicar, incluso cuando sus colores de entrada están dentro \[ \] de ese intervalo. Cuando esto sucede, estos colores pueden estar sujetos a recortes numéricos. Tenga en cuenta que es importante tener en cuenta el intervalo de colores en un espacio sin multiplicar, aunque los efectos integrados suelen producir colores en el espacio premultiplicado. Esto garantiza que los colores permanecen dentro del intervalo, incluso si otros efectos posteriormente no se multiplican.

Algunos de los efectos que pueden emitir estos colores fuera del intervalo ofrecen una propiedad "ClampOutput". Entre ellas se incluyen las siguientes:

-   [Matriz de colores](color-matrix.md)
-   [Composición aritmética](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Efectos de transferencia](built-in-effects.md)

Establecer la propiedad ClampOutput en TRUE en estos efectos garantiza que se logrará un resultado coherente independientemente de factores como la vinculación del sombreador. Tenga en cuenta que la fijación se produce en un espacio sin multiplicar.

Otros efectos integrados también pueden producir colores de salida más allá del intervalo 0, 1 en un espacio sin multiplicar, incluso cuando sus píxeles de colores (y las propiedades "Color" si existen) están dentro de ese \[ \] intervalo. Entre ellas se incluyen las siguientes:

-   [Efectos de transformación y escalado](built-in-effects.md) (cuando la propiedad Modo de interpolación es cúbica o cúbica de alta calidad)
-   [Efectos de iluminación](built-in-effects.md)
-   [Detección de borde](edge-detection-effect.md) (cuando la propiedad Superponer bordes es TRUE)
-   [Exposición](exposure-effect.md)
-   [Compuesto](composite.md) (cuando la propiedad Mode es Más)
-   [Temperatura y tono](temperature-and-tint-effect.md)
-   [Sepia](sepia-effect.md)
-   [Saturación](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forzar el recorte numérico dentro de un gráfico de efectos

Al usar los efectos enumerados anteriormente que no tienen una propiedad ClampOutput, las aplicaciones deben considerar la posibilidad de forzar la fijación numérica. Esto se puede hacer insertando un efecto adicional en el gráfico que fija sus píxeles. Se puede usar un efecto de matriz de colores, con su propiedad 'ClampOutput' establecida en TRUE y dejando la propiedad 'ColorMatrix' como valor predeterminado (paso a través).

Una segunda opción para lograr resultados coherentes es solicitar que Direct2D use texturas intermedias que tengan mayor precisión. Este procedimiento se describe a continuación.

## <a name="controlling-precision-of-intermediate-textures"></a>Control de la precisión de texturas intermedias

Direct2D proporciona varias maneras de controlar la precisión de un gráfico. Antes de usar formatos de alta precisión en Direct2D, las aplicaciones deben asegurarse de que la GPU los admite lo suficiente. Para comprobarlo, use [**ID2D1DeviceContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Las aplicaciones pueden crear un dispositivo Direct3D mediante WARP (emulación de software) para garantizar que todas las precisións de búfer se admiten independientemente del hardware de GPU real en el dispositivo. Esto se recomienda en escenarios como la aplicación de efectos a una foto mientras se guarda en el disco. Incluso si Direct2D admite formatos de búfer de alta precisión en la GPU, se recomienda usar WARP en este escenario en GPU de nivel de característica 9.X, debido a la precisión limitada de la aritmética del sombreador y el muestreo en algunas GPU móviles de bajo consumo.

En cada caso siguiente, la precisión solicitada es realmente la precisión mínima que usará Direct2D. Se puede usar una mayor precisión si no se requieren intermedios. Direct2D también puede compartir texturas intermedias para diferentes partes del mismo grafo o gráficos diferentes por completo. En este caso, Direct2D usa la precisión máxima solicitada para todas las operaciones implicadas.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Selección de precisión de ID2D1DeviceContext::SetRenderingControls

La manera más sencilla de controlar la precisión de las texturas intermedias de Direct2D es usar [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Esto controla la precisión de todas las texturas intermedias, siempre que una precisión no se establezca manualmente en los efectos o transformaciones directamente.


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>Selección de precisión de entradas y destinos de representación

Las aplicaciones también pueden basarse en la precisión de las entradas en un gráfico de efectos para controlar la precisión de las texturas intermedias. Esto es así siempre que no se especifique una precisión de búfer mediante [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))y no se establezca manualmente en los efectos y la transformación directamente.

Las precisións de las entradas a los efectos se propagan a través del gráfico para seleccionar la precisión de los intermedios de nivel inferior. Cuando se encuentran distintas ramas en el gráfico de efectos, se usa la mayor precisión de cualquier entrada.

La precisión seleccionada en función de un mapa de bits de Direct2D se determina a partir de su formato de píxel. La precisión seleccionada para [**un ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) se determina a partir del formato de píxel WIC del IWICBitmapSource subyacente que se usa para crear **id2D1ImageSource.** Tenga en cuenta que Direct2D no permite crear orígenes de imágenes con orígenes WIC mediante precisións no admitidas por Direct2D y la GPU.

Es posible que Direct2D no pueda asignar un efecto a una precisión basada en sus entradas. Esto sucede cuando un efecto no tiene entradas o cuando se usa [**id2D1CommandList,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) que no tiene ninguna precisión específica. En este caso, la precisión de las texturas intermedias se determina a partir del conjunto de mapas de bits como destino de representación actual del contexto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Selección de precisión directamente sobre el efecto y las transformaciones

La precisión mínima de las texturas intermedias también se puede establecer en ubicaciones explícitas dentro de un gráfico de efectos. Esto solo se recomienda para escenarios avanzados.

La precisión mínima se puede establecer mediante una propiedad en un efecto como se muestra a continuación:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Dentro de una implementación de efecto, la precisión mínima se puede establecer mediante ID2D1RenderInfo::SetOutputPrecision como se muestra a continuación:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Tenga en cuenta que la precisión establecida en un efecto se propagará a los efectos de nivel inferior en el mismo gráfico de efectos, a menos que se establezca una precisión diferente en esos efectos de bajada. La precisión establecida en una transformación dentro de un efecto no afecta a la precisión de los nodos de transformación de nivel inferior.

A continuación se muestra la lógica recursiva completa que se usa para determinar la precisión mínima de un búfer intermedio que almacena la salida de un nodo de transformación determinado:

![Lógica de precisión mínima del búfer intermedio](images/precision-and-clipping-4.png)

 

 