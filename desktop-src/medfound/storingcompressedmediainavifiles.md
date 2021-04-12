---
description: Describe cómo almacenar datos de Windows Media en un archivo AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Almacenar medios comprimidos en archivos AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361898"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Almacenar medios comprimidos en archivos AVI (Microsoft Media Foundation)

Cualquier contenido que se comprime con los códecs de Windows Media Audio y vídeo debe colocarse en un formato de contenedor. Uno de los formatos más populares es audio de vídeo entrelazado o AVI. Puede usar Microsoft vídeo para Windows (VfW) o Microsoft DirectShow para crear archivos AVI. Para obtener más información acerca del uso de vídeo para Windows o DirectShow, consulte la documentación del producto en MSDN.

Los códecs de Windows Media Audio y vídeo se han desarrollado para usar las propiedades de Advanced Systems Format (ASF), que es el contenedor que usa Windows Media. Debido a que AVI y ASF almacenan el contenido de forma diferente, surgen algunas dificultades al almacenar el contenido comprimido con los códecs de vídeo y Windows Media Audio en un archivo AVI.

Los códecs Windows Media Audio comprimen el contenido de audio de forma que no se pueda descomprimir correctamente sin las marcas de tiempo de los ejemplos individuales. Esto habilita algunas optimizaciones en los medios comprimidos. Dado que el contenedor ASF mantiene marcas de tiempo con todas las muestras, esta característica de los algoritmos de audio siempre ha funcionado bien.

Sin embargo, los archivos AVI no conservan las marcas de tiempo con ejemplos. Esto significa que Windows Media Audio contenido no se puede descomprimir correctamente cuando se almacena en un archivo AVI. Windows Media Video contenido no tiene esta limitación y se puede incluir en archivos AVI. Para codificar Windows Media Video contenido en un archivo AVI con sonido sincronizado, debe usar otro códec de audio.

El otro problema con el uso de un archivo AVI como contenedor para Windows Media se refiere al vídeo de velocidad de bits bajo. Una de las formas en que los códecs Windows Media Video producen el contenido de vídeo para velocidades de bits bajas es quitando fotogramas duplicados. Si desea colocar Windows Media Video contenido en un archivo ASF, debe configurar el codificador para proporcionar tramas ficticias para fotogramas duplicados (establezca [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en Variant \_ true) de modo que cada fotograma se represente en el archivo. Los fotogramas ficticios generados por el códec tienen un tamaño de 8 bytes. Sin embargo, el marco escrito en el archivo por el multiplexor de AVI puede ser de cientos de bytes mayor y rellenarse con datos aleatorios. Un archivo AVI creado de esta manera se podrá reproducir, pero será mucho mayor de lo esperado. Puede evitar este problema si usa velocidades de bits más altas al codificar vídeo para el almacenamiento en archivos AVI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



