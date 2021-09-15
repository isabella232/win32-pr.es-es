---
title: Lectura Secuencias con píxeles no cuadrados
description: Lectura Secuencias con píxeles no cuadrados
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows SDK de formato multimedia, lectura de secuencias de vídeo
- Windows SDK de formato multimedia, secuencias de vídeo
- Windows SDK de formato multimedia, píxeles no cuadrados
- Windows SDK de formato multimedia, píxeles (no cuadrados)
- Formato de sistemas avanzados (ASF), lectura de secuencias de vídeo
- ASF (formato de sistemas avanzados), lectura de secuencias de vídeo
- Formato de sistemas avanzados (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Formato de sistemas avanzados (ASF), píxeles no cuadrados
- ASF (formato de sistemas avanzados), píxeles no cuadrados
- Formato de sistemas avanzados (ASF), píxeles (no cuadrados)
- ASF (formato de sistemas avanzados), píxeles (no cuadrados)
- lectura de secuencias de vídeo
- secuencias de vídeo, lectura
- secuencias de vídeo, píxeles no cuadrados
- píxeles no cuadrados
- píxeles (no cuadrados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466662"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lectura Secuencias con píxeles no cuadrados

Las aplicaciones de lector que necesitan controlar correctamente los píxeles no cuadrados deben examinar los atributos de nivel de flujo en el encabezado ASF y las extensiones de unidad de datos de cada ejemplo. Hay dos casos en los que el rectángulo de salida debe ajustarse para compensar los píxeles no cuadrados.

Cuando el contenido de origen se ha capturado desde un dispositivo como una cámara DV (vídeo digital) con píxeles no cuadrados en su CCD, una aplicación lectora debe ajustar su rectángulo de salida de vídeo para que la imagen se muestre correctamente en un monitor de equipo con píxeles cuadrados.

Cuando la aplicación lectora genera vídeo que se reproducirá en un televisor XEL, por ejemplo a través de una conexión de salida de S-Video en la tarjeta de vídeo, debe ajustar el rectángulo de vídeo para que la imagen se muestre correctamente en los píxeles no cuadrados de la televisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para leer y escribir vídeos Secuencias píxeles no cuadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




