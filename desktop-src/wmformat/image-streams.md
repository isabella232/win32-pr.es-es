---
title: Flujos de imagen
description: Flujos de imagen
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- SDK de Windows Media Format, flujos de imagen
- Advanced Systems Format (ASF), stream Image
- ASF (formato de sistemas avanzados), flujos de imagen
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos de imagen, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357505"
---
# <a name="image-streams"></a>Flujos de imagen

Un flujo de imagen es un tipo especial de flujo que contiene imágenes fijas asignadas a los tiempos de presentación. Una aplicación puede mostrar las imágenes en una secuencia de imágenes como se desea, pero la implementación típica es mostrar cada imagen hasta que se entregue la siguiente imagen, como una presentación. Normalmente, una secuencia de imágenes se codifica en un archivo con una secuencia de audio para generar una presentación simple de imágenes sincronizadas con música o voz.

Los flujos de imágenes son similares a las secuencias de vídeo en que se crean a partir de muestras sin comprimir que se comprimen como parte del proceso de escritura de archivos, pero también son como secuencias arbitrarias porque debe asignar una velocidad de bits y una ventana de búfer adecuados para el contenido sin depender de las propiedades asignadas por códecs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos arbitrarios**](arbitrary-streams.md)
</dt> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Secuencias de audio y vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Escribir secuencias de imagen**](writing-image-streams.md)
</dt> </dl>

 

 




