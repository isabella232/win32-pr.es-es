---
description: Acerca de Transcode API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Acerca de Transcode API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449784"
---
# <a name="about-the-transcode-api"></a>Acerca de Transcode API

En el diagrama siguiente se muestra cómo se relaciona la API de transcodificación con el resto de la Media Foundation de codificación.

![diagrama que muestra la API de transcodificación.](images/encoding08.png)

La canalización de codificación contiene los siguientes objetos de procesamiento de datos:

-   Origen multimedia
-   Descodificador
-   Cambiador de tamaño de vídeo o remuestreo de audio
-   Codificador
-   Receptor multimedia

El cambio de tamaño del vídeo solo es necesario si el tamaño del vídeo de salida difiere del origen. El resampler de audio solo es necesario si es necesario volver a muestrear el audio antes de la codificación. El par descodificador/codificador es necesario para la transcodificación, pero no para volver a realizar la experiencia.

La topología *de codificación* es el conjunto de objetos de canalización (origen, descodificador, cambio de tamaño, remuestreador, codificador y receptor multimedia), además de los puntos de conexión entre ellos. Para obtener más información sobre las topologías, vea [Topologías](topologies.md).

Los distintos componentes son responsables de crear los distintos objetos de canalización:

-   Normalmente, la aplicación usa el [solucionador de origen](source-resolver.md) para crear el origen multimedia.
-   La [sesión multimedia](media-session.md) carga y configura el descodificador, el cambiador de tamaño de vídeo y el remuestreo de audio. Internamente, usa el cargador de topologías para hacer esto (consulte [**LATOPOLoader).**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
-   La API de transcodificación carga y configura el codificador y el receptor multimedia.

Las aplicaciones avanzadas pueden configurar el codificador y el receptor multimedia directamente, en lugar de usar la API de transcodificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[Uso de Transcode API](fast-transcode-objects.md)
</dt> </dl>

 

 



