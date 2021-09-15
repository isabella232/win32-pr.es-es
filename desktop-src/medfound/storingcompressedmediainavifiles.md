---
description: Describe cómo almacenar datos Windows multimedia en un archivo AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Almacenamiento de medios comprimidos en archivos AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580228"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Almacenamiento de medios comprimidos en archivos AVI (Microsoft Media Foundation)

Cualquiera de los contenidos que comprima con los códecs Windows Media Audio y Video deben colocarse en algún formato de contenedor. Uno de los formatos más populares es Audio Video Interleave o AVI. Puede usar Microsoft Video para Windows (VfW) o Microsoft DirectShow para crear archivos AVI. Para obtener más información sobre el uso de Video Windows o DirectShow, consulte la documentación del producto en MSDN.

Los códecs Windows Media Audio y Video se han desarrollado para usar las propiedades del formato de sistemas avanzados (ASF), que es el contenedor que usa Windows Media. Dado que AVI y ASF almacenan contenido de forma diferente, surgen algunas dificultades al almacenar contenido comprimido con los códecs de audio y vídeo multimedia Windows en un archivo AVI.

Los códecs Windows Media Audio comprimen el contenido de audio de forma que no se pueda descomprimir correctamente sin marcas de tiempo para las muestras individuales. Esto permite cierta optimización en los medios comprimidos. Dado que el contenedor de ASF mantiene marcas de tiempo con todas las muestras, esta característica de los algoritmos de audio siempre ha funcionado bien.

Sin embargo, los archivos AVI no mantienen marcas de tiempo con ejemplos. Esto significa que Windows contenido de Audio multimedia no se puede descomprimir correctamente cuando se almacena en un archivo AVI. Windows El contenido de Vídeo multimedia no tiene esta limitación y se puede incluir en archivos AVI. Para codificar Windows contenido de Media Video en un archivo AVI con sonido sincronizado, debe usar otro códec de audio.

El otro problema con el uso de un archivo AVI como contenedor para Windows Media se refiere al vídeo de baja velocidad de bits. Una de las formas en que los códecs Windows Media Video generan contenido de vídeo para velocidades de bits bajas es mediante la colocación de fotogramas duplicados. Si desea colocar el contenido de Windows Media Video en un archivo ASF, debe establecer el codificador para que entregue fotogramas ficticios para fotogramas duplicados (establezca [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en VARIANT TRUE) para que cada fotograma se represente en el \_ archivo. Los fotogramas ficticios generados por el códec tienen un tamaño de 8 bytes. Sin embargo, el marco escrito en el archivo por el multiplexor AVI puede tener cientos de bytes más grandes y rellenarse con datos aleatorios. Un archivo AVI realizado de esta manera todavía se podrá reproducir, pero será mucho mayor de lo esperado. Puede evitar este problema mediante el uso de velocidades de bits más altas al codificar vídeo para el almacenamiento en archivos AVI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



