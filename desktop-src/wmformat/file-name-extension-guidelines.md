---
title: Instrucciones de extensión de nombre de archivo
description: Instrucciones de extensión de nombre de archivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- SDK de Windows Media Format, extensiones de nombre de archivo
- Advanced Systems Format (ASF), extensiones de nombre de archivo
- ASF (formato de sistemas avanzados), extensiones de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994182"
---
# <a name="file-name-extension-guidelines"></a>Instrucciones de extensión de nombre de archivo

Una extensión de nombre de archivo proporciona a un fabricante de software independiente información sobre los requisitos de representación de una aplicación que utiliza esa extensión concreta.

La extensión de nombre de archivo que se debe usar para un archivo creado por una aplicación basada en el SDK de Windows Media Format viene determinada por el tipo de contenido del archivo. Use la siguiente lógica para determinar la extensión de nombre de archivo que debe usar.

Si el archivo contiene secuencias codificadas con códecs de terceros o datos sin comprimir no admitidos (incluidos los datos arbitrarios), el archivo debe utilizar la extensión. ASF.

Si el archivo no contiene secuencias no compatibles y contiene una o varias secuencias de vídeo descomprimidas o codificadas con un códec de vídeo de Windows Media, el archivo debe usar la extensión. wmv. Estos archivos también pueden incluir secuencias de audio PCM, secuencias de audio codificadas con cualquier códec de audio de Windows Media, secuencias de scripts y secuencias Web.

Si el archivo no contiene secuencias no compatibles y no hay secuencias de vídeo compatibles, y contiene una o varias secuencias de audio descomprimidos PCM o codificadas con cualquier códec de audio de Windows Media, el archivo debe usar la extensión. WMA. Estos archivos también pueden contener secuencias de scripts y secuencias Web.

Si el archivo solo contiene flujos que no son audio ni vídeo, debe utilizar la extensión. ASF.

Los tipos de vídeo sin comprimir admitidos son RGB8, RGB565, RGB555, RGB24, RGB32, i420, IYUV, YV12, YUY2, UYVY, YVYU y YVU9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Consideraciones del proyecto**](project-considerations.md)
</dt> </dl>

 

 




