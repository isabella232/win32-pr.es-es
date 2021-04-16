---
title: Cambio de tamaño de vídeo
description: Cambio de tamaño de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- SDK de Windows Media Format, cambio de tamaño de vídeo
- SDK de Windows Media Format, cambiar tamaño de vídeo
- Advanced Systems Format (ASF), cambio de tamaño de vídeo
- ASF (formato de sistemas avanzados), cambio de tamaño de vídeo
- Advanced Systems Format (ASF), cambiar el tamaño de vídeo
- ASF (formato de sistemas avanzados), cambiar el tamaño del vídeo
- cambio de tamaño de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268553"
---
# <a name="video-resizing"></a>Cambio de tamaño de vídeo

Al definir la configuración de un flujo de vídeo, debe especificar un ancho y un alto para los fotogramas de vídeo. Este tamaño de vídeo determina el tamaño de los fotogramas de vídeo codificados en la sección de datos del archivo. Sin embargo, el tamaño de vídeo de un perfil no determina, o limita, el tamaño del medio de entrada que se entrega al escritor o el tamaño de los medios de salida que se reciben del lector. El escritor puede cambiar el tamaño de los fotogramas de vídeo para que se adapten a las necesidades de la aplicación.

El tamaño de la imagen de vídeo se puede considerar en tres fases: tamaño del vídeo de entrada, tamaño de vídeo de flujo y tamaño de vídeo de salida.

El tamaño del vídeo de entrada es el tamaño de los fotogramas que se pasan como muestras al objeto escritor. Este tamaño se define como una de las propiedades de entrada de vídeo necesarias. Para obtener más información sobre las propiedades de entrada, consulte [para enumerar los formatos de entrada](to-enumerate-input-formats.md).

El tamaño de vídeo de Stream es el tamaño de los marcos de la sección de datos del archivo ASF. Este tamaño se define como uno de los valores de configuración de secuencia necesarios en el perfil. Si está escribiendo un archivo y el tamaño del vídeo de entrada es diferente del tamaño del vídeo de flujo, el escritor cambia el tamaño de los fotogramas durante la codificación. Para obtener más información sobre las propiedades de secuencias de vídeo, consulte [configuración de secuencias de vídeo](configuring-video-streams.md).

El tamaño del vídeo de salida es el tamaño de los fotogramas entregados por el lector o el lector sincrónico. Este tamaño se define como una de las propiedades de salida de vídeo necesarias. Si está leyendo un archivo y el tamaño del vídeo de salida es diferente del tamaño del vídeo de flujo, el lector cambia el tamaño de los fotogramas durante la descodificación.

No se puede establecer un tamaño de vídeo de flujo en un número impar de píxeles de ancho. Si establece el ancho de una secuencia de vídeo en un valor impar, el escritor no aceptará el perfil, o bien el vídeo resultante se codificará con una línea negra hacia abajo para componer la diferencia.

Debe tener cuidado al cambiar el tamaño del vídeo. Las imágenes tienden a ser más adecuadas en su resolución original. A menudo, el cambio de tamaño de las imágenes puede producir distorsiones y convertir el texto en ilegible. Si comprime vídeo a una velocidad de bits baja, también encontrará que el cambio de tamaño de las distorsiones puede conducir a artefactos de compresión graves.

El códec de pantalla de Windows Media Video 9 no admite el cambio de tamaño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




