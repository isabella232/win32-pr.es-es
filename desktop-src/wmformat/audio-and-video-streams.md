---
title: Audio y vídeo Secuencias
description: Audio y vídeo Secuencias
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows SDK de formato multimedia, secuencias de audio
- Formato de sistemas avanzados (ASF), secuencias de audio
- ASF (formato de sistemas avanzados), secuencias de audio
- Windows SDK de formato multimedia, secuencias de vídeo
- Formato de sistemas avanzados (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- secuencias de audio, acerca de
- secuencias de vídeo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bb1836540a8de3b0834d271c1aeb97ba2869fa5acfcd221d03071b32ec94e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705229"
---
# <a name="audio-and-video-streams"></a>Audio y vídeo Secuencias

Los tipos más comunes de secuencias que se usan en los archivos creados mediante Windows SDK de formato multimedia son secuencias de audio y vídeo. Las representaciones digitales de datos de audio y vídeo son complejas y toman grandes cantidades de memoria. En la mayoría de los casos, tanto el audio como el vídeo se comprimen antes de agregarse a un archivo ASF. La compresión se realiza mediante un descomprimidor/descomprimidor (códec).

Varios Windows códecs multimedia se incluyen con este SDK y proporcionan una compresión de calidad excelente para los medios digitales. Para obtener más información sobre los códecs Windows multimedia, vea [Características del códec](codec-features.md). Muchos otros códecs están disponibles en varios orígenes. Puede usar los códecs que quiera al crear archivos ASF, pero solo los códecs Windows Media son compatibles directamente con los objetos de este SDK. Para usar otros códecs, debe comprimir muestras y pasarlas al objeto de escritor como datos arbitrarios.

La distinción más importante entre secuencias de audio o vídeo y secuencias arbitrarias es que las secuencias que contienen datos de audio o vídeo multimedia de Windows se validan mediante los objetos del SDK de formato multimedia de Windows. Los flujos de datos arbitrarios no se validan automáticamente y la aplicación debe comprobar su integridad.

Las propiedades de una secuencia de audio o vídeo se describen en el perfil usado para crear el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Datos arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




