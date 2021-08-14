---
title: Imagen Secuencias
description: Imagen Secuencias
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows SDK de formato multimedia, secuencias de imagen
- Advanced Systems Format (ASF),image streams
- ASF (formato de sistemas avanzados), secuencias de imágenes
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- secuencias de imágenes, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702869"
---
# <a name="image-streams"></a>Imagen Secuencias

Un flujo de imagen es un tipo especial de secuencia que contiene imágenes fijas asignadas a los tiempos de presentación. Una aplicación puede mostrar las imágenes en una secuencia de imágenes según sea necesario, pero la implementación típica es mostrar cada imagen hasta que se entregue la siguiente imagen, como una presentación de diapositivas. Normalmente, una secuencia de imágenes se codifica en un archivo con una secuencia de audio para generar una presentación sencilla de imágenes sincronizadas con música o voz.

Las secuencias de imagen son como secuencias de vídeo en que se crean a partir de muestras sin comprimir que se comprimen como parte del proceso de escritura de archivos, pero también son como secuencias arbitrarias porque debe asignar una velocidad de bits y una ventana de búfer adecuadas para el contenido sin depender de propiedades asignadas por códec.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Datos arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Audio y vídeo Secuencias**](audio-and-video-streams.md)
</dt> <dt>

[**Escribir imágenes Secuencias**](writing-image-streams.md)
</dt> </dl>

 

 




