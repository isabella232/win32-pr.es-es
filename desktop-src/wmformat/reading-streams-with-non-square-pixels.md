---
title: Lectura de secuencias con píxeles no cuadrados
description: Lectura de secuencias con píxeles no cuadrados
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- SDK de Windows Media Format, lectura de secuencias de vídeo
- SDK de Windows Media Format, secuencias de vídeo
- SDK de Windows Media Format, píxeles no cuadrados
- Windows Media Format SDK, píxeles (no cuadrado)
- Advanced Systems Format (ASF), lectura de secuencias de vídeo
- ASF (formato de sistemas avanzados), lectura de secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Advanced Systems Format (ASF), píxeles no cuadrados
- ASF (formato de sistemas avanzados), píxeles no cuadrados
- Advanced Systems Format (ASF), píxeles (no cuadrados)
- ASF (formato de sistemas avanzados), píxeles (no cuadrados)
- lectura de secuencias de vídeo
- secuencias de vídeo, lectura
- secuencias de vídeo, píxeles no cuadrados
- píxeles no cuadrados
- píxeles (no cuadrados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704819"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lectura de secuencias con píxeles no cuadrados

Las aplicaciones de lector que necesitan administrar correctamente píxeles no cuadrados deben examinar los atributos de nivel de secuencia del encabezado ASF y las extensiones de unidad de datos de cada ejemplo. Hay dos casos en los que el rectángulo de salida debe ajustarse para compensar los píxeles no cuadrados.

Cuando el contenido de origen se ha capturado desde un dispositivo, como una cámara de vídeo digital con píxeles no cuadrados en el CCD, una aplicación de lector debe ajustar su rectángulo de salida de vídeo para que la imagen se muestre correctamente en un monitor de equipo con píxeles cuadrados.

Cuando la aplicación lector emite vídeo que se reproducirá en una televisión NTSC, por ejemplo, a través de una conexión de S-vídeo de salida en la tarjeta de vídeo, debe ajustar el rectángulo del vídeo para que la imagen se muestre correctamente en píxeles no cuadrados de la televisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para leer y escribir secuencias de vídeo con píxeles no cuadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




