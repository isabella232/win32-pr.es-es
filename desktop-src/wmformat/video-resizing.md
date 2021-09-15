---
title: Tamaño de vídeo
description: Tamaño de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows SDK de formato multimedia, tamaño de vídeo
- Windows SDK de formato multimedia, volver a tamaño de vídeo
- Formato de sistemas avanzados (ASF), tamaño de vídeo
- ASF (formato de sistemas avanzados), tamaño de vídeo
- Formato de sistemas avanzados (ASF), vídeo de redimensionamiento
- ASF (formato de sistemas avanzados), vídeo de redimensionamiento
- tamaño de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572129"
---
# <a name="video-resizing"></a>Tamaño de vídeo

Al definir la configuración de una secuencia de vídeo, debe especificar un ancho y un alto para los fotogramas de vídeo. Este tamaño de vídeo determina el tamaño de los fotogramas de vídeo codificados en la sección de datos del archivo. Sin embargo, el tamaño de vídeo de un perfil no determina ni limita el tamaño del medio de entrada que se entrega al escritor ni el tamaño del medio de salida que recibe del lector. El escritor puede cambiar el tamaño de los fotogramas de vídeo para satisfacer las necesidades de la aplicación.

El tamaño de la imagen de vídeo se puede pensar que pasa por tres fases: tamaño de vídeo de entrada, tamaño de vídeo de secuencia y tamaño de vídeo de salida.

El tamaño del vídeo de entrada es el tamaño de los fotogramas que se pasan como ejemplos al objeto de escritor. Este tamaño se define como una de las propiedades de entrada de vídeo necesarias. Para obtener más información sobre las propiedades de entrada, vea [Para enumerar formatos de entrada.](to-enumerate-input-formats.md)

El tamaño del vídeo de secuencia es el tamaño de los fotogramas de la sección de datos del archivo ASF. Este tamaño se define como una de las opciones de configuración de flujo necesarias en el perfil. Si va a escribir un archivo y el tamaño del vídeo de entrada es diferente del tamaño del vídeo de secuencia, el escritor cambia el tamaño de los fotogramas durante la codificación. Para obtener más información sobre las propiedades de la secuencia de vídeo, vea [Configuring Video Secuencias](configuring-video-streams.md).

El tamaño del vídeo de salida es el tamaño de los fotogramas entregados por el lector o el lector sincrónico. Este tamaño se define como una de las propiedades de salida de vídeo necesarias. Si está leyendo un archivo y el tamaño del vídeo de salida es diferente del tamaño del vídeo de secuencia, el lector cambia el tamaño de los fotogramas durante la decodificación.

No se puede establecer un tamaño de vídeo de secuencia en un número impar de píxeles de ancho. Si establece el ancho de una secuencia de vídeo en un valor impar, el escritor no aceptará el perfil o el vídeo resultante se codificará con una línea negra hacia abajo un lado para crear la diferencia.

Debe tener cuidado al redimensionar el vídeo. Las imágenes tienden a verse mejor en su resolución original. Cambiar el tamaño de las imágenes a menudo puede provocar distorsión y hacer que el texto sea ilegible. Si va a comprimir vídeo a una velocidad de bits baja, también verá que cambiar el tamaño de las distorsión puede provocar artefactos de compresión graves.

El códec Windows Media Video 9 Screen no admite el cambio de tamaño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




