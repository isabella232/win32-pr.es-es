---
description: Acerca de la API de Transcode
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Acerca de la API de Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569156"
---
# <a name="about-the-transcode-api"></a>Acerca de la API de Transcode

En el diagrama siguiente se muestra cómo se relaciona la API de Transcode con el resto de la canalización de codificación de Media Foundation.

![un diagrama que muestra la API de transcodificación.](images/encoding08.png)

La canalización de codificación contiene los siguientes objetos de procesamiento de datos:

-   Origen de medios
-   Descodificador
-   Remuestreador de audio y ajuste de vídeo
-   Codificador
-   Receptor de medios

El ajuste de tamaño de vídeo solo es necesario si el tamaño del vídeo de salida difiere del origen. El remuestreador de audio solo es necesario si es necesario volver a muestrear el audio antes de la codificación. El par descodificador/codificador es necesario para la transcodificación, pero no para remuxing.

La *topología* de codificación es el conjunto de objetos de canalización (origen, descodificador, tamaño, remuestreador, codificador y receptor de medios), además de los puntos de conexión entre ellos. Para obtener más información sobre las topologías, vea [topologías](topologies.md).

Los distintos componentes son responsables de crear los distintos objetos de canalización:

-   Normalmente, la aplicación usa la [resolución de origen](source-resolver.md) para crear el origen de medios.
-   La [sesión multimedia](media-session.md) carga y configura el descodificador, el tamaño de vídeo y el remuestreador de audio. Internamente, usa el cargador de topología para hacerlo (consulte [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   La API de Transcode carga y configura el codificador y el receptor de medios.

Las aplicaciones avanzadas pueden configurar el codificador y el receptor multimedia directamente, en lugar de usar la API de Transcode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de transcodificación](transcode-api.md)
</dt> <dt>

[Uso de la API de Transcode](fast-transcode-objects.md)
</dt> </dl>

 

 



