---
title: Obtención de buenos resultados con el códec de Windows Media Video 9
description: Obtención de buenos resultados con el códec de Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows SDK de formato multimedia, códec Windows media video 9 screen
- Formato de sistemas avanzados (ASF), códec Windows Media Video 9 Screen
- ASF (formato de sistemas avanzados), códec Windows Media Video 9 Screen
- codecs,Windows Media Video 9 Screen
- Windows Códec de pantalla de Vídeo multimedia 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657cde745f6bfbabe00fe123b493e2eae2afb20ddf40206f781822770a4386f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110435"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Obtención de buenos resultados con el códec de Windows Media Video 9

El códec Windows Media Video 9 Screen está diseñado para generar vídeo muy comprimido para la captura de pantalla. Dado que la mayor parte de la necesidad de captura de pantalla implica imágenes bastante simples y estáticas, los altos niveles de compresión alcanzados no suelen significar un gran esfuerzo en la calidad de la imagen. Sin embargo, cada captura de pantalla es diferente y la calidad de la imagen resultante puede variar considerablemente en función de las circunstancias.

La mejor manera de determinar la configuración del perfil para una sesión de códec de pantalla es codificar un archivo de prueba mediante una secuencia de velocidad de bits variable basada en la calidad. Establezca la calidad en el valor que desee y codificar una captura de pantalla como si estuviera grabando el archivo final. Cuando se escribe el archivo, reprodújalo mediante el objeto de lector asincrónico, realizando llamadas periódicas a [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). Al supervisar el valor del **miembro dwBandwidth** de la estructura [**WM READER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada llamada, puede determinar la velocidad de bits aproximada necesaria para lograr la calidad que desea. A continuación, puede usar esa velocidad de bits para la codificación de velocidad de bits constante.

Si descubre que la calidad que desea requiere una velocidad de bits mayor de la que puede usar para el escenario de entrega, puede probar las técnicas siguientes para obtener más eficacia del códec.

-   Use una resolución más pequeña para la captura de pantalla. Capturar una resolución de pantalla mayor de la que necesita también puede crear confusión para el visor al presentar más información de la necesaria.
-   Use menos gráficos en la captura de pantalla. El códec Windows Media Video 9 Screen está optimizado para codificar Windows primitivos y texto con alta calidad. Normalmente se producen problemas debido a gráficos con mapa de bits, que a menudo contienen miles de colores individuales. Mientras menos mapas de bits haya en la pantalla al capturar, mejores serán los resultados. Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que tiene un mapa de bits en la calidad de la imagen:
    -   Reduzca el tamaño del gráfico.
    -   Reduzca el número de gráficos individuales que aparecen en la pantalla simultáneamente.
    -   Reduzca la cantidad de movimiento del gráfico. Por ejemplo, si el gráfico está en una ventana, mantenga la ventana lo más estaciona posible.
    -   Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.
-   Use una velocidad de [*fotogramas más lenta.*](wmformat-glossary.md) Las capturas de pantalla a menudo pueden ser eficaces a velocidades de fotograma muy bajas (a veces tan bajas como 4 o 5 fotogramas por segundo).
-   Reduzca la velocidad de bits del audio que lo acompaña.

Además, el códec no admite el cambio de tamaño del rectángulo de vídeo. En otras palabras, si intenta usar el códec para codificar una pantalla de 800 x 600 hacia abajo en un rectángulo de vídeo de 640 x 480, el vídeo resultante tendrá artefactos significativos que pueden hacer que gran parte del texto de la pantalla sea ilegible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de la captura de pantalla Secuencias**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




