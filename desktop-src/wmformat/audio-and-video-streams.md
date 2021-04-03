---
title: Secuencias de audio y vídeo
description: Secuencias de audio y vídeo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- SDK de Windows Media Format, secuencias de audio
- Advanced Systems Format (ASF), secuencias de audio
- ASF (formato de sistemas avanzados), secuencias de audio
- SDK de Windows Media Format, secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- secuencias de audio, acerca de
- secuencias de vídeo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075653"
---
# <a name="audio-and-video-streams"></a>Secuencias de audio y vídeo

Los tipos de secuencias más comunes que se usan en los archivos creados con el SDK de Windows Media Format son secuencias de audio y vídeo. Las representaciones digitales de los datos de audio y vídeo son complejas y ocupan grandes cantidades de memoria. En la mayoría de los casos, el audio y el vídeo se comprimen antes de agregarse a un archivo ASF. La compresión se realiza mediante un compresor/descompresor (códec).

Con este SDK se incluyen varios códecs de Windows Media, que proporcionan una compresión de calidad excelente para los medios digitales. Para obtener más información acerca de los códecs de Windows Media, consulte [características de códec](codec-features.md). Muchos otros códecs están disponibles desde diversos orígenes. Puede usar cualquier códec que desee al crear archivos ASF, pero solo los objetos de este SDK admiten directamente los códecs de Windows Media. Para usar otros códecs, debe comprimir los ejemplos y pasarlos al objeto escritor como datos arbitrarios.

La diferencia más importante entre las secuencias de audio o vídeo y las secuencias arbitrarias es que los objetos del SDK de Windows Media Format validan las secuencias que contienen datos de audio o vídeo de Windows Media. Los flujos de datos arbitrarios no se validan automáticamente, por lo que la aplicación debe comprobar su integridad.

Las propiedades de una secuencia de audio o de vídeo se describen en el perfil que se usa para crear el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos arbitrarios**](arbitrary-streams.md)
</dt> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




