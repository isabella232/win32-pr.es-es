---
description: Usar el códec de pantalla de Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Usar el códec de pantalla de Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689618"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Usar el códec de pantalla de Windows Media Video 9 (Microsoft Media Foundation)

El códec de pantalla de Windows Media Video 9 está optimizado para comprimir el vídeo de la *aplicación*, que consta de capturas de pantalla consecutivas para una pantalla del equipo. El códec aprovecha la simplicidad de imagen típica (relativamente pocos colores, muchas líneas rectas, etc.) y la falta de movimiento relativo para lograr una relación de compresión muy alta. El inconveniente de esta optimización es que el vídeo que no se ajusta a las características esperadas del vídeo de la aplicación puede ser difícil de comprimir con un nivel de calidad aceptable.

El codificador de pantalla de Windows Media Video 9 se identifica mediante el identificador de clase CLSID \_ CMSSEncMediaObject2 y el descodificador identifica el identificador de clase CLSID \_ CMSSDecMediaObject. El valor FOURCC para los tipos de medios que usan este códec es "MSS2".

## <a name="configuring-the-encoder"></a>Configurar el codificador

El codificador del códec de pantalla de Windows Media Video 9 se configura de la misma manera que el descodificador de vídeo estándar.

> [!Note]  
> El codificador de pantalla solo admite la codificación de un paso. Puede establecer la propiedad [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) en 2 y procesar las entradas dos veces sin errores, pero no hay ninguna ventaja para hacerlo. Se trata de un problema conocido y puede corregirse en futuras versiones.

 

## <a name="getting-the-best-results"></a>Obtener los mejores resultados

Si descubre que la calidad que desea en el contenido de captura de pantalla requiere una velocidad de bits superior a la que puede usar para el escenario de entrega, puede probar las siguientes técnicas para obtener una mayor eficacia del códec:

-   Use una resolución más pequeña para la captura de pantalla. La captura de una resolución de pantalla mayor que la necesaria puede confundir al visor presentando información innecesaria.
-   Usar una velocidad de fotogramas más lenta. A menudo, las capturas de pantalla pueden ser eficaces a velocidades de fotogramas muy bajas (a veces, como mínimo, 4 o 5 fotogramas por segundo).
-   Use menos gráficos en la captura de pantalla. El códec de pantalla de Windows Media Video 9 está optimizado para codificar texto y primitivas de Windows con alta calidad. Normalmente, los problemas se producen debido a los gráficos de mapa Dete, que a menudo contienen miles de colores individuales. Cuantos menos mapas de bits haya en la pantalla al capturar, mejor serán los resultados. Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que tiene un mapa de bits en la calidad de la imagen:
    -   Reduzca el tamaño del gráfico.
    -   Reducir el número de gráficos individuales que aparecen en la pantalla al mismo tiempo.
    -   Reduzca la cantidad de movimiento del gráfico. Por ejemplo, si el gráfico está en una ventana, mantenga la ventana como estacional como sea posible.
    -   Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para descodificar el vídeo de captura de pantalla. Sin embargo, al igual que con todos los códecs de Windows Media Video 9, el descodificador de captura de pantalla no puede descomprimir correctamente el contenido codificado sin los datos privados del códec.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de vídeo](configuringvideoencoding.md)
</dt> <dt>

[Uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Codificador de pantalla de Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



