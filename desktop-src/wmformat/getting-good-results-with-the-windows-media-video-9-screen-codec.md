---
title: Obtener buenos resultados con el códec de pantalla de Windows Media Video 9
description: Obtener buenos resultados con el códec de pantalla de Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Códec de pantalla de Windows Media Format, Windows Media Video 9
- Códec Advanced Systems Format (ASF), Windows Media Video 9 Screen Codec
- ASF (formato de sistemas avanzados), códec de pantalla de Windows Media Video 9
- códecs, pantalla de Windows Media Video 9
- Códec de pantalla de Windows Media Video 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994964"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Obtener buenos resultados con el códec de pantalla de Windows Media Video 9

El códec de pantalla de Windows Media Video 9 está diseñado para generar vídeo muy comprimido para la captura de pantalla. Dado que la mayoría de las necesidades de captura de pantalla implican imágenes bastante simples y estáticas, los altos niveles de compresión que se alcanzan no suelen significar un gran sacrificio de la calidad de la imagen. Sin embargo, cada captura de pantalla es diferente y la calidad de la imagen resultante puede variar considerablemente en función de las circunstancias.

La mejor manera de determinar la configuración de perfil para una sesión de códec de pantalla es codificar un archivo de prueba mediante un flujo de velocidad de bits variable basado en la calidad. Establezca la calidad en el valor que desee y codifique una captura de pantalla como si estuviera grabando el archivo final. Cuando se escribe el archivo, reproduzca el uso del objeto lector asincrónico y realice llamadas regulares a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). Al supervisar el valor del miembro **dwBandwidth** de la estructura [**de \_ \_ estadísticas del lector de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada llamada, puede determinar la velocidad de bits aproximada necesaria para lograr la calidad deseada. Después, puede usar esa velocidad de bits para la codificación de velocidad de bits constante.

Si descubre que la calidad deseada requiere una velocidad de bits superior a la que puede usar para el escenario de entrega, puede probar las siguientes técnicas para obtener una mayor eficacia del códec.

-   Use una resolución más pequeña para la captura de pantalla. La captura de una resolución de pantalla mayor que la que necesita también puede crear confusión en el visor presentando más información de la necesaria.
-   Use menos gráficos en la captura de pantalla. El códec de pantalla de Windows Media Video 9 está optimizado para codificar texto y primitivas de Windows con alta calidad. Normalmente, los problemas se producen debido a los gráficos de mapa Dete, que a menudo contienen miles de colores individuales. Cuantos menos mapas de bits haya en la pantalla al capturar, mejor serán los resultados. Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que tiene un mapa de bits en la calidad de la imagen:
    -   Reduzca el tamaño del gráfico.
    -   Reducir el número de gráficos individuales que aparecen en la pantalla al mismo tiempo.
    -   Reduzca la cantidad de movimiento del gráfico. Por ejemplo, si el gráfico está en una ventana, mantenga la ventana como estacional como sea posible.
    -   Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.
-   Usar una [*velocidad de fotogramas*](wmformat-glossary.md)más lenta. A menudo, las capturas de pantalla pueden ser eficaces a velocidades de fotogramas muy bajas (a veces, como mínimo, 4 o 5 fotogramas por segundo).
-   Reduzca la velocidad de bits del audio que lo acompaña.

Además, el códec no admite el cambio de tamaño del rectángulo de vídeo. En otras palabras, si intenta usar el códec para codificar una pantalla de 800 x 600 en un rectángulo de vídeo de 640 x 480, el vídeo resultante tendrá artefactos significativos que pueden hacer que la gran parte del texto de la pantalla sea ilegible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configurar secuencias de captura de pantalla**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




