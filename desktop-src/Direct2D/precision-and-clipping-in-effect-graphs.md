---
title: Recorte numérico y de precisión en gráficos de efectos
description: Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y previsibilidad con respecto a la precisión numérica.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90628661ec8cd3f16ff6a6149aecbb7e8be3e5a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078208"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Recorte numérico y de precisión en gráficos de efectos

Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y previsibilidad con respecto a la precisión numérica. En este tema se describen los procedimientos recomendados y los valores relevantes en Direct2D que son útiles si:

-   El gráfico de efectos depende de una precisión numérica alta o de colores fuera del \[ intervalo de 0, 1 y desea asegurarse de que \] siempre estarán disponibles.
-   O bien, el gráfico de efectos se basa en la implementación de representación para fijar los colores intermedios en el \[ intervalo de 0, 1 \] y desea asegurarse de que esta fijación siempre se produce

A menudo, Direct2D divide un gráfico de efectos en secciones y representa cada sección en un paso independiente. El resultado de algunos pasos puede almacenarse en texturas de Direct3D intermedias que, de forma predeterminada, tienen un intervalo numérico y una precisión limitados. Direct2D no ofrece ninguna garantía sobre si se usan estas texturas intermedias. Este comportamiento puede variar según las funcionalidades de GPU, así como entre las versiones de Windows.

En Windows 10, Direct2D usa menos texturas intermedias debido a su uso de la vinculación del sombreador. Por tanto, Direct2D puede generar resultados diferentes con la configuración predeterminada que en versiones anteriores de Windows. Esto afecta principalmente a escenarios en los que la vinculación del sombreador es posible en un gráfico de efectos y ese grafo también contiene efectos que generan colores de salida de intervalo extendido.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Información general sobre la representación de efectos e intermedios

Para representar un gráfico de efectos, Direct2D busca primero el gráfico subyacente de "transformaciones", donde una transformación es un nodo de gráfico que se usa dentro de un efecto. Hay diferentes tipos de transformaciones, incluidas las que proporcionan sombreadores de Direct3D para que Direct2D los use.

Por ejemplo, Direct2D puede representar un gráfico de efectos de la manera siguiente:

![gráfico de efectos con texturas intermedias](images/precision-and-clipping-1.png)

Direct2D busca oportunidades para reducir el número de texturas intermedias que se usan para representar el gráfico de efectos. esta lógica es opaca para las aplicaciones. Por ejemplo, Direct2D puede representar el siguiente gráfico mediante una llamada a Draw de Direct3D y sin texturas intermedias:

![gráfico de efecto sin texturas intermedias](images/precision-and-clipping-2.png)

Antes de Windows 10, Direct2D siempre usaría texturas intermedias si se usaran varios sombreadores de píxeles en el mismo gráfico de efectos. La mayoría de los efectos integrados que solo ajustan los valores de color (por ejemplo, brillo o saturación) lo hacen mediante sombreadores de píxeles.

En Windows 10, Direct2D ahora puede evitar el uso de texturas intermedias en estos casos. Para ello, vincula internamente los sombreadores de píxeles adyacentes. Por ejemplo:

![gráfico de efectos de Windows 10 con varios sombreadores de píxeles y sin texturas intermedias](images/precision-and-clipping-3.png)

Tenga en cuenta que no todos los sombreadores de píxeles adyacentes de un gráfico se pueden vincular entre sí y, por lo tanto, solo ciertos gráficos generarán una salida diferente en Windows 10. Para obtener detalles completos, consulte [vinculación del sombreador de efectos](effect-shader-linking.md). Las restricciones principales son:

-   Un efecto no se vinculará con efectos que consuman su salida, si el primer efecto está conectado como una entrada a varios efectos.
-   Un efecto no se vinculará con un conjunto de efectos como entrada, si el primer efecto muestrea su entrada en una posición lógica diferente de la salida. Por ejemplo, un efecto de la matriz de colores podría estar vinculado a su entrada, pero un efecto de circunvolución no será.

## <a name="built-in-effect-behavior"></a>Comportamiento de efectos integrados

Muchos efectos integrados pueden producir colores fuera del \[ intervalo de 0, 1 \] en el espacio de colores unpremultiplied, incluso cuando sus colores de entrada están dentro de ese intervalo. Cuando esto sucede, estos colores pueden estar sujetos al recorte numérico. Tenga en cuenta que es importante tener en cuenta el intervalo de colores en el espacio de unpremultiplied, aunque los efectos integrados normalmente generan colores en el espacio premultiplicado. Esto garantiza que los colores permanecen dentro del alcance, incluso si otros efectos unpremultiply posteriormente.

Algunos de los efectos que pueden emitir estos colores fuera del intervalo ofrecen una propiedad "ClampOutput". Entre ellas se incluyen las siguientes:

-   [Matriz de colores](color-matrix.md)
-   [Compuesto aritmético](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Efectos de transferencia](built-in-effects.md)

El establecimiento de la propiedad ClampOutput en TRUE en estos efectos garantiza que se logre un resultado coherente, independientemente de factores como la vinculación del sombreador. Tenga en cuenta que la compresión se produce en el espacio de unpremultiplied.

Otros efectos integrados también pueden producir colores de salida más allá del \[ intervalo de 0, 1 \] en el espacio de unpremultiplied, incluso cuando sus colores son píxeles (y propiedades de "color", si los hay) dentro de ese intervalo. Entre ellas se incluyen las siguientes:

-   [Transformación y escalado de efectos](built-in-effects.md) (cuando la propiedad modo de interpolación es cúbica o cúbica de alta calidad)
-   [Efectos de iluminación](built-in-effects.md)
-   [Detección perimetral](edge-detection-effect.md) (cuando la propiedad bordes superpuesto es true)
-   [Exposiciones](exposure-effect.md)
-   [Composite](composite.md) (cuando la propiedad de modo es Plus)
-   [Temperatura y matiz](temperature-and-tint-effect.md)
-   [Sepia](sepia-effect.md)
-   [Saturación](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forzar el recorte numérico dentro de un gráfico de efectos

Aunque el uso de los efectos mostrados anteriormente no tienen una propiedad ClampOutput, las aplicaciones deben considerar la posibilidad de aplicar la fijación numérica. Esto se puede hacer insertando un efecto adicional en el gráfico que corsujete sus píxeles. Se puede usar un efecto de matriz de colores, con su propiedad ' ClampOutput ' establecida en TRUE y saliendo de la propiedad ' ColorMatrix ' como valor predeterminado (de paso a través).

Una segunda opción para lograr resultados coherentes es solicitar que Direct2D use texturas intermedias con mayor precisión. Esto se describe a continuación.

## <a name="controlling-precision-of-intermediate-textures"></a>Controlar la precisión de las texturas intermedias

Direct2D proporciona varias maneras de controlar la precisión de un gráfico. Antes de usar los formatos de alta precisión en Direct2D, las aplicaciones deben asegurarse de que son suficientemente compatibles con la GPU. Para comprobarlo, use [**ID2D1DeviceContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Las aplicaciones pueden crear un dispositivo Direct3D mediante WARP (emulación de software) para garantizar que todas las precisiones de búfer se admiten independientemente del hardware de GPU real en el dispositivo. Esto se recomienda en escenarios como aplicar efectos a una fotografía mientras se guardan en el disco. Aunque Direct2D admita formatos de búfer de alta precisión en la GPU, se recomienda usar WARP en este escenario en GPU de nivel de característica 9. X, debido a la precisión limitada de la aritmética del sombreador y el muestreo en algunas GPU móviles de baja energía.

En cada caso siguiente, la precisión solicitada es realmente la precisión mínima que usará Direct2D. Se puede usar una precisión mayor si no se requieren intermedios. Direct2D también puede compartir texturas intermedias para distintas partes del mismo gráfico o de gráficos diferentes. En este caso, Direct2D usa la precisión máxima solicitada para todas las operaciones implicadas.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Selección de precisión desde ID2D1DeviceContext:: SetRenderingControls

La manera más sencilla de controlar la precisión de las texturas intermedias de Direct2d es usar [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Controla la precisión de todas las texturas intermedias, siempre que una precisión no se establezca también manualmente en efectos o transformaciones directamente.


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



### <a name="precision-selection-from-inputs-and-render-targets"></a>Selección de precisión de destinos de entrada y representación

Las aplicaciones también pueden basarse en la precisión de las entradas en un gráfico de efectos para controlar la precisión de las texturas intermedias. Esto es así siempre que no se especifique una precisión de búfer mediante [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))y no se establezca manualmente en efectos y transformación directamente.

Las precisiones de las entradas a efectos se propagan a través del gráfico para seleccionar la precisión de los intermedios de nivel inferior. Cuando se cumplen las distintas ramas del gráfico de efectos, se usa la mayor precisión de cualquier entrada.

La precisión seleccionada en función de un mapa de bits de Direct2D se determina a partir de su formato de píxel. La precisión seleccionada para un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) se determina a partir del formato de píxel de WIC del IWICBitmapSource subyacente que se usa para crear el **ID2D1ImageSource**. Tenga en cuenta que Direct2D no permite la creación de orígenes de imagen con orígenes de WIC mediante el uso de precisión no compatible con Direct2D y la GPU.

Es posible que Direct2D no pueda asignar un efecto a una precisión en función de sus entradas. Esto sucede cuando un efecto no tiene ninguna entrada o cuando se usa un [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) , que no tiene ninguna precisión específica. En este caso, la precisión de las texturas intermedias se determina a partir del conjunto de mapas de bits como destino de representación actual del contexto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Selección de precisión directamente en el efecto y las transformaciones

La precisión mínima para las texturas intermedias también se puede establecer en ubicaciones explícitas dentro de un gráfico de efectos. Esto solo se recomienda para escenarios avanzados.

La precisión mínima se puede establecer mediante una propiedad en un efecto como se indica a continuación:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Dentro de una implementación de efecto, la precisión mínima se puede establecer mediante ID2D1RenderInfo:: SetOutputPrecision de la siguiente manera:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Tenga en cuenta que el conjunto de precisión de un efecto se propagará a efectos descendentes en el mismo gráfico de efecto, a menos que se establezca una precisión diferente en esos efectos de nivel inferior. La precisión establecida en una transformación dentro de un efecto no afecta a la precisión de los nodos de transformación de nivel inferior.

A continuación se muestra la lógica recursiva completa que se usa para determinar la precisión mínima de un búfer intermedio que almacena la salida de un nodo de transformación determinado:

![Lógica de precisión mínima de búfer intermedio](images/precision-and-clipping-4.png)

 

 