---
description: Uso del códec de pantalla Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Uso del códec de pantalla Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363654"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Uso del códec de pantalla Windows Media Video 9 (Microsoft Media Foundation)

El códec Windows Media Video 9 Screen está optimizado para comprimir el vídeo de la *aplicación,* que consta de capturas de pantalla consecutivas para una pantalla del equipo. El códec aprovecha la simplicidad típica de la imagen (relativamente pocos colores, muchas líneas rectas, entre otras) y la falta relativa de movimiento para lograr una relación de compresión muy alta. La desventaja de esta optimización es que el vídeo que no se ajusta a las características esperadas del vídeo de la aplicación puede ser difícil de comprimir con un nivel de calidad aceptable.

El codificador Windows Media Video 9 Screen se identifica mediante el identificador de clase CLSID CMSSEncMediaObject2 y el descodificador se identifica con el identificador de clase \_ \_ CLSID CMSSDecMediaObject. El valor FOURCC para los tipos de medios que usan este códec es "MSS2".

## <a name="configuring-the-encoder"></a>Configuración del codificador

El codificador del códec Windows Media Video 9 Screen se configura de la misma manera que el descodificador de vídeo estándar.

> [!Note]  
> El codificador de pantalla solo admite la codificación de un paso. Puede establecer la propiedad [ \_ MFPKEY PASSESUSED](mfpkey-passesusedproperty.md) en 2 y procesar las entradas dos veces sin errores, pero no tiene ninguna ventaja hacerlo. Se trata de un problema conocido y se puede corregir en futuras versiones.

 

## <a name="getting-the-best-results"></a>Obtención de los mejores resultados

Si descubre que la calidad que desea en el contenido de captura de pantalla requiere una velocidad de bits mayor de la que puede usar para el escenario de entrega, puede probar las técnicas siguientes para obtener más eficacia del códec:

-   Use una resolución más pequeña para la captura de pantalla. La captura de una resolución de pantalla mayor de la necesaria puede confundir al visor mediante la presentación de información innecesaria.
-   Use una velocidad de fotogramas más lenta. Las capturas de pantalla a menudo pueden ser eficaces a velocidades de fotogramas muy bajas (a veces tan bajas como 4 o 5 fotogramas por segundo).
-   Use menos gráficos en la captura de pantalla. El códec Windows Media Video 9 Screen está optimizado para codificar Windows primitivos y texto con alta calidad. Normalmente se producen problemas debido a gráficos con mapa de bits, que a menudo contienen miles de colores individuales. Mientras menos mapas de bits haya en la pantalla al capturar, mejores serán los resultados. Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que un mapa de bits tiene en la calidad de la imagen:
    -   Reduzca el tamaño del gráfico.
    -   Reduzca el número de gráficos individuales que aparecen en la pantalla al mismo tiempo.
    -   Reduzca la cantidad de movimiento del gráfico. Por ejemplo, si el gráfico está en una ventana, mantenga la ventana lo más estaciona posible.
    -   Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para la decodificación de vídeo de captura de pantalla. Sin embargo, como con todos los códecs Windows Media Video 9, el descodificador de captura de pantalla no puede descomprimir correctamente el contenido codificado sin los datos privados del códec.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de vídeo](configuringvideoencoding.md)
</dt> <dt>

[Uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Windows Codificador de pantalla de Vídeo multimedia 9](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



