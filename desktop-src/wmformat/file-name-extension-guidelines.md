---
title: Instrucciones de extensión de nombre de archivo
description: Instrucciones de extensión de nombre de archivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows SDK de formato multimedia, extensiones de nombre de archivo
- Formato de sistemas avanzados (ASF), extensiones de nombre de archivo
- ASF (formato de sistemas avanzados), extensiones de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256317"
---
# <a name="file-name-extension-guidelines"></a>Instrucciones de extensión de nombre de archivo

Una extensión de nombre de archivo proporciona a un proveedor de software independiente información sobre los requisitos de representación de una aplicación que usa esa extensión determinada.

La extensión de nombre de archivo que debe usar para un archivo creado por una aplicación basada en el SDK de formato multimedia de Windows viene determinada por el tipo de contenido del archivo. Use la siguiente lógica para determinar la extensión de nombre de archivo que debe usar.

Si el archivo contiene secuencias codificadas con códecs de terceros o datos no comprimidos no admitidos (incluidos datos arbitrarios), el archivo debe usar la extensión .asf.

Si el archivo no contiene secuencias no admitidas y contiene una o varias secuencias de vídeo sin comprimir o codificadas con cualquier códec de vídeo multimedia de Windows, el archivo debe usar la extensión .wmv. Estos archivos también pueden incluir secuencias de audio PCM, secuencia Windows s de audio codificadas con cualquier códec de audio multimedia, secuencias de script y secuencias web.

Si el archivo no contiene secuencias no admitidas ni secuencias de vídeo admitidas, y contiene una o varias secuencias de audio PCM sin comprimir o codificadas con cualquier códec de audio multimedia de Windows, el archivo debe usar la extensión .wma. Estos archivos también pueden contener secuencias de script y secuencias web.

Si el archivo solo contiene secuencias que no son audio ni vídeo, debe usar la extensión .asf.

Entre los tipos de vídeo no comprimidos admitidos se incluyen RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU y YVU9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Project Consideraciones**](project-considerations.md)
</dt> </dl>

 

 




