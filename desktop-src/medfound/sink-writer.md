---
description: El escritor de receptor es un componente para la codificación de archivos de audio o de vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360476"
---
# <a name="sink-writer"></a>Escritor de receptor

El escritor de receptor es un componente para la codificación de archivos de audio o de vídeo.

En el diagrama siguiente se muestra, en un nivel alto, cómo una aplicación utiliza el escritor de receptor para codificar y el archivo de audio o vídeo.

![diagrama que muestra el escritor del receptor.](images/encoding09.png)

El escritor de receptor hospeda un receptor de medios y, opcionalmente, uno o más codificadores. Los codificadores convierten datos de audio o vídeo sin comprimir en bitstreams codificados. El receptor de medios envía el bitstreams a un archivo. El escritor del receptor realiza las siguientes tareas:

-   Carga el receptor de medios.
-   Busca y carga los codificadores.
-   Administra el flujo de datos a los codificadores y al receptor de medios.

La aplicación pasa datos de audio o vídeo al escritor de receptor como entrada. No importa el modo en que la aplicación obtiene o genera los datos de entrada. Una opción es usar el [lector de origen](source-reader.md), tal y como se muestra en el diagrama siguiente. Sin embargo, el escritor del receptor no requiere el uso del lector de origen. Estos dos componentes son independientes.

![diagrama que muestra el lector de origen y el escritor del receptor.](images/encoding02.png)

## <a name="in-this-section"></a>En esta sección

-   [Uso del escritor de receptor](using-the-sink-writer.md)
-   [Tutorial: uso del escritor de receptores para codificar vídeo](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Información general de la codificación en Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



